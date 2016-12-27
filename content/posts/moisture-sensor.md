+++
date = "2016-12-22T23:48:42+01:00"
title = "Cloud-Connected Soil Moisture Sensor Using ESP8266"


+++
* * * *
Today I've built a soil moisture sensor connected to the Internet of Things for less than 5€ using an ESP8266-12E and a cheap moisture sensor.
The idea is to read the moisture value every x hours and put the ESP8266 into deep sleep mode.

1.Materials
---

1x [ESP8266-12E](https://de.aliexpress.com/item/Esp8266-WiFi-series-of-model-ESP-12-ESP-12F-esp12F-esp12-authenticity-guaranteed/32639524010.html?spm=2114.010208.3.75.TaI1vv&ws_ab_test=searchweb0_0,searchweb201602_2_10065_10068_10000009_10084_10083_10080_10082_10081_10060_10061_10062_10056_10055_10037_10054_10059_10032_10099_10078_10079_10077_427_426_10103_10073_10102_10101_10096_10052_10050_10107_10106_10051,searchweb201603_3,afswitch_5&btsid=12d312ef-b28e-4e41-ac0a-ff39da0a68a1)

1x [ESP8266-12E Break-Out Board](https://de.aliexpress.com/item/Serial-WIFI-ESP8266-module-adapter-plate-Full-IO-port-leads-you-can-choose-the-ESP-07/32380914509.html?spm=2114.010208.3.1.Am64ZS&ws_ab_test=searchweb0_0,searchweb201602_2_10065_10068_10000009_10084_10083_10080_10082_10081_10060_10061_10062_10056_10055_10037_10054_10059_10032_10099_10078_10079_10077_427_426_10103_10073_10102_10101_10096_10052_10050_10107_10106_10051,searchweb201603_3,afswitch_5&btsid=12d312ef-b28e-4e41-ac0a-ff39da0a68a1) (optional)

1x [Soil Mositure Sensor](https://de.aliexpress.com/item/5PCS-LOT-FREE-SHIPPING-Soil-moisture-meter-testing-module-soil-humidity-sensor-robot-intelligent-car-for/1625352348.html?spm=2114.010208.8.53.K1kpov)

some wires and resistors for the voltage divider

* * * *

2.Build
-------------

Wire up the components like shown in the following picture. Please make sure to use a voltage divider because the ESP8266's analog in has a range from 0 V - 1 V, but the sensor ranges from 0 V - 3.3 V
![sketch](https://cloud.githubusercontent.com/assets/16187615/21501819/8409f220-cc4b-11e6-86f8-37d96be0e6bd.png)
![prototype esp8266 soil moisture](https://cloud.githubusercontent.com/assets/16187615/21503515/55cb4712-cc58-11e6-97e9-816aecd944f0.jpg)

* * * *
3.Program
-------------

The prototype code can be found on [GitHub](https://github.com/eightBEC/esp8266moisture)

I've been using IBM's IoT Platform to send my data to, but you can use every IoT platform you like to use.
Before uploading the code, adjust the config0.lua file which contains all properties for WIFI and IoT connectivity.
Make sure to upload all .lua files to your device using a tool like LuaLoader.

* * * *
4.Saving A Plant's Life
-------------

![esp8266 plant](https://cloud.githubusercontent.com/assets/16187615/21503516/5725fc92-cc58-11e6-86e6-eba90e7e7466.jpg)

* * * *
5.Next Steps
-------------
In the future I'll add a solar panel, a lithium-ion battery pack and a MOSFET to disconnect the sensor while deep sleep.
