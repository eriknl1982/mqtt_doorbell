![Imgur](https://i.imgur.com/4t2Ilsw.png)

This repository contains sample code and eagle/gerber/STL files for the MQTT doorbell board I sell on tindie: https://www.tindie.com/products/ErikLemcke/doorbell-modernizr/

This board that can transfer your ordinary doorbell (running on 8 - 24v ac) to a wifi doorbell. The board works with an ESP12 ESP8266 module that you can program with a FTDI module and (for example) the Arduino IDE. Whenever someone presses your doorbell, the board can execute an action, while leaving the regular doorbell circuit intact, so that if your module crashes for one or another reason, your doorbell will still be working. The assembled version can be used without any programming to send MQTT messages, for example to Home Assistant.

To program the board, make sure you provide it with power, plug in a ftdi module and set the dipswitch to on.

I use the folowing settings for programming:

- Board: Generic EP8266 module
- Flash mode: QIO
- Flash size: 512K (64K SPIFFS)
- Debugging port: Disabled
- Debug level: None
- IwIP variant: V2 lower memory
- reset method: ck
- crystal frequency: 26Mhz
- Flash frequency: 40Mhz
- CPU frequency: 80Mhz
- Builtin led: 2
- Upload speed: 115200
- Erase flash: Only sketch

If you are going to build it yourself, you will need the folowing parts:

#### To assemble this board, you will need the following parts:
- 1x ESP12f module [(sample)](https://www.aliexpress.com/item/ESP8266-Remote-Serial-WIFI-Transceiver-Wireless-Module-Esp-12-AP-STA-TOP/32646271039.html?spm=2114.search0104.3.8.2d866f9bg356HJ&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=2d4aea06-a96e-40a3-a231-87c2b62a80c4-1&algo_pvid=2d4aea06-a96e-40a3-a231-87c2b62a80c4&transAbTest=ae803_2&priceBeautifyAB=0)
- 4x 10k resitor, smd size 1206 [(sample)](https://www.aliexpress.com/item/Free-Shipping-100PCS-1206-10K-10K-OHM-1-smd-resistor/1090806202.html?spm=2114.search0104.3.1.43a21240XRFdDf&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=709525b8-8593-455c-8efa-07c3f3ce8228-0&algo_pvid=709525b8-8593-455c-8efa-07c3f3ce8228&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 10k resitor, thru hole [(sample)](https://www.aliexpress.com/store/product/100pcs-set-1-4W-Resistance-1-Metal-Film-Resistor-Pack-Assorted-Kit-1K-2K-4-7K/1504763_32861819464.html?spm=2114.search0104.3.1.4c0d36baXYxkSz&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10151_10065_10344_10068_10342_10343_10340_10341_10696_10084_10083_10618_10304_10307_10820_10821_10301_10843_10059_100031_10103_10624_10623_10622_10621_10620,searchweb201603_51,ppcSwitch_5&algo_expid=e3fd0740-6222-418d-9183-fe36bdfb2f1d-0&algo_pvid=e3fd0740-6222-418d-9183-fe36bdfb2f1d&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 330r resitor, smd size 1206 [(sample)](https://www.aliexpress.com/item/100Pcs-1206-SMD-resistor-0R-10M-1-2W-0-1-10-100-150-220-330-ohm/32847115923.html?spm=2114.search0104.3.1.4bcc1954MGyEbp&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=03d36d71-9210-4daa-ba6d-0d927a84b877-0&algo_pvid=03d36d71-9210-4daa-ba6d-0d927a84b877&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 1p dip switch [(sample)](https://www.aliexpress.com/item/10PCS-Lot-DIP-Switch-1P-2-54mm-Toggle-Switch-Red-Snap-Switch/32778200806.html?spm=2114.search0104.3.24.1fe1d1a1sUUCAD&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=cc64cbff-a764-4662-8452-5fbc674b3830-3&algo_pvid=cc64cbff-a764-4662-8452-5fbc674b3830&transAbTest=ae803_2&priceBeautifyAB=0)
- 2x tactile switch [(sample)](https://www.aliexpress.com/item/THGS-25pcs-Round-Pushbutton-4-Pins-SMD-SMT-Momentary-Tactile-Switch/32721411394.html?spm=2114.search0104.3.69.24d25580z5KXIm&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=72ad9c0a-894e-4d0d-a650-c844d18cb295-12&algo_pvid=72ad9c0a-894e-4d0d-a650-c844d18cb295&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 470uf capacitor [(sample)](https://www.aliexpress.com/item/SMD-electrolytic-capacitor-470UF-6-3V-6-3-7-7MM-VT-type-chip-polarity-temperature-105/32814865187.html?spm=2114.search0104.3.87.3c9272dblaF34k&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=fa08a327-d750-4922-8d0c-8a368b171ecc-13&algo_pvid=fa08a327-d750-4922-8d0c-8a368b171ecc&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 100nf capacitor, SMD size 1206 [(sample)](https://www.aliexpress.com/item/Free-Shipping-100PCS-1206-104-100NF-0-1UF-1206-SMD-capacitance/1096160798.html?spm=2114.search0104.3.1.71d322c9BiZITD&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=ae9db756-53ad-4fca-853d-d6855f03eda6-0&algo_pvid=ae9db756-53ad-4fca-853d-d6855f03eda6&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 2pin screw terminal [(sample)](https://www.aliexpress.com/item/20-PCS-KF301-5-0-2P-blue-KF301-3P-Pitch-5-0mm-KF301-2P-Straight-Pin/32833138976.html?spm=2114.search0104.3.17.6b284c7ctDJEA2&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=dd191ab4-0937-468a-a91b-19ac53064bd2-2&algo_pvid=dd191ab4-0937-468a-a91b-19ac53064bd2&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 6pin female header [(sample)](https://www.aliexpress.com/item/40pcs-2-54MM-6Pin-11MM-Long-Needle-Female-Header-Strip-Stackable-Header-for-arduino-W5100-6p/32668087711.html?spm=2114.search0104.3.83.154721f6xN5o5u&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=c0a98dbf-f354-486c-be51-a9068dfd1d38-12&algo_pvid=c0a98dbf-f354-486c-be51-a9068dfd1d38&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x HT7333 LDO [(sample)](https://www.aliexpress.com/item/10PCS-HT7333-A-SOT-89-HT7333-1-SOT89-HT7333-7333-1-SMD-7333A-1-new-and/32818420909.html?spm=2114.search0104.3.2.4b9c73ea1CR81c&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=5d51c538-7dd5-42bd-8e93-c66127f056bf-0&algo_pvid=5d51c538-7dd5-42bd-8e93-c66127f056bf&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 1N4148 diode, smd size 1206 [(sample)](https://www.aliexpress.com/item/100pcs-1206-1N4148W-T4-1N4148-SOD-123-Switching-Diode/32354597825.html?spm=2114.search0104.3.1.65002565fkmX0i&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=7cf2de10-d2b9-41eb-a268-300ace100396-0&algo_pvid=7cf2de10-d2b9-41eb-a268-300ace100396&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x PC817 Optocoupler [(sample)](https://www.aliexpress.com/item/100PCS-PC817C-DIP-PC817-C-DIP4-PC817-C-new-and-original-IC-free-shipping/32847601895.html?spm=2114.search0104.3.9.32aa76dfaNDbvv&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=e8d061c3-7004-462e-899c-a522d5885630-1&algo_pvid=e8d061c3-7004-462e-899c-a522d5885630&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 5.5 x 2.1 mm Female DC Power Jack Plug Socket [sample](https://www.aliexpress.com/item/10Pcs-PCB-Mount-5-5-x-2-1-mm-Female-DC-Power-Jack-Plug-Socket-Connector/32813661863.html?spm=2114.search0104.3.181.7aee2436K2nMqV&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=b89433cb-84ea-4f2c-b110-90657c1acf5a-26&algo_pvid=b89433cb-84ea-4f2c-b110-90657c1acf5a&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x 5v power supply [sample](https://www.aliexpress.com/item/1PCS-High-quality-AC-100V-240V-Converter-Switching-power-adapter-DC-5V-2A-2000MA-Supply-EU/32496043021.html?spm=2114.search0104.3.1.61197a5aNbvepX&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10709_10151_10065_10344_10068_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10710_10307_10301_5722715_5711215_10059_308_100031_10103_10624_10623_10622_5711315_5722515_10621_10620,searchweb201603_36,ppcSwitch_5&algo_expid=0f10a11c-3fea-4ce8-9680-a6fa20d2b76d-3&algo_pvid=0f10a11c-3fea-4ce8-9680-a6fa20d2b76d&transAbTest=ae803_2&priceBeautifyAB=0)
- 1x MB6S bridge rectifier [sample](https://www.aliexpress.com/item/Free-shipping-20pcs-600V-0-5A-SOP-4-SMD-rectifier-diode-bridge-mb6s/32336867082.html?spm=2114.search0104.3.1.25d453e0kUU3ZK&ws_ab_test=searchweb0_0,searchweb201602_3_10152_10151_10065_10344_10068_5723115_5722815_10342_10343_10340_5722915_10341_5722615_10696_10084_10083_10618_10304_10307_10820_10301_10821_5722715_10843_10059_100031_10103_10624_10623_10622_5722515_10621_10620,searchweb201603_50,ppcSwitch_5&algo_expid=d8bc8f3c-cd8b-4e61-a706-30cb63aab87a-0&algo_pvid=d8bc8f3c-cd8b-4e61-a706-30cb63aab87a&transAbTest=ae803_2&priceBeautifyAB=0)

