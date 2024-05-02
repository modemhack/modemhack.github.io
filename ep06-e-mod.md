Quectel EP06-E 基於 Qualcomm X12 Modem，但其基線較舊。

在弱訊號地區，將TX Power提升至超過 Power Class 3 (23dBm) 將會對可用性有大幅提升。

在 EP06-E 上，最高能將 LTE 的發射功率調整至 25.5 dBm。

相關 AT command 如下：
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
