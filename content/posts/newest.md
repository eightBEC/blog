---
title: "ESP8266 on White Aliexpress Break-Out Board"
date: "2016-12-20"
description: "Getting the ESP8266 to work"
categories:
    - "iot"
    - "electronics"
---

## First Heading

Recently I've bought a couple of those super cheap [ESP8266-12E devices](https://de.aliexpress.com/item/5PCS-Esp8266-WiFi-series-of-model-ESP-12-ESP-12F-esp12F-esp12-authenticity-guaranteed/32655304335.html?spm=2114.010208.3.144.EIgPmS&ws_ab_test=searchweb0_0,searchweb201602_2_10065_10068_10084_10083_10080_10082_10081_10060_10061_10062_10056_10055_10054_10059_10099_10078_10079_427_10073_10103_10102_10101_10096_10052_10050_10051,searchweb201603_3&btsid=0101278f-2176-44d3-bb51-a69a912e2603) and the proper white [break-out boards](https://de.aliexpress.com/item/10Pcs-Set-ESP8266-WiFi-Modules-Breakout-Transfer-Board-Adapter-Plate-For-ESP-07-ESP-08-ESP/32655534675.html?spm=2114.010208.3.21.f1wPGl&ws_ab_test=searchweb0_0,searchweb201602_2_10065_10068_10084_10083_10080_10082_10081_10060_10061_10062_10056_10055_10054_10059_10099_10078_10079_427_10073_10103_10102_10101_10096_10052_10050_10051,searchweb201603_3&btsid=ff36fcdd-d486-4eb6-91cb-df975902bc09).


After soldering the ESP8266 on top of the break-board I ran a few tests and tried to get this little IoT device up and running, but I wasn't able to do so.


It took me quite a while to figure out that the VCC pin of the break-board wasn't connected to the VCC pin going to the ESP8266 board. Becuase of the lack of documentation there was no clue that either one has to add a voltage divider or a jumper. Doing the latter fixed the issue and I was able to get the ESP8266 running.
