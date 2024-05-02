---
layout: post
title: Quectel EP06-E 修改上傳功率上限及開啟DL 256QAM
---

Quectel EP06-E 基於 Qualcomm X12 Modem，實際上支援3CA，但移遠將其設計為一款2CA的模組。
在弱訊號地區，將TX Power提升至超過 Power Class 3 (23dBm) 將會對可用性有大幅提升。
由由於其軟體基線較舊，在 EP06-E 上最高能將 LTE 的發射功率調整至 25.5 dBm。

# 將 TX Power 調整為 25.5 dBm
此處功率為dB10，因此 FF = 255 = 25.5 dBm，也可以用於降低功率上限
```
# B1
AT+QNVFW="/nv/item_files/rfnv/00020992",0100FF00
# B3
AT+QNVFW="/nv/item_files/rfnv/00020994",0100FF00
# B5
AT+QNVFW="/nv/item_files/rfnv/00020996",0100FF00
# B7
AT+QNVFW="/nv/item_files/rfnv/00020997",0100FF00
# B8
AT+QNVFW="/nv/item_files/rfnv/00020998",0100FF00
# B20
AT+QNVFW="/nv/item_files/rfnv/00021003",0100FF00
# B38
AT+QNVFW="/nv/item_files/rfnv/00021004",0100FF00
# B40
AT+QNVFW="/nv/item_files/rfnv/00021005",0100FF00
# B41
AT+QNVFW="/nv/item_files/rfnv/00021670",0100FF00
# B28
AT+QNVFW="/nv/item_files/rfnv/00025477",0100FF00
```

# 開啟 DL 256QAM
```AT+QCFG="dl_256qam",1```
(需要韌體版本 EP06ELAR04A04M4G 以上才可使用，低版本建議升級或透過修改EFS方式實現)

# 開啟 3CA
TODO
(利用相關工具修改EFS 00028874增加CA組合以開啟3CA)

