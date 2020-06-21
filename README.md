# DIY-ZigBee-smoke-dektor
Modding a normal smoke detector with an ZigBee module.

Befor it wos popular modding with one ESP8266 for getting HA connction.  
From [belog.flo.cx](https://blog.flo.cx/2018/08/ikea-diy-smart-smoke-detector/).

Using pin 7 from the processer that is normally floating and deliviering 9V in alarm state its a very good thing.  

Xiaomi MCCGQ11LM Aqara door & window contact sensor have a good formfactor and easy to desammbling and aroun 20€ in stores in EU.  

Its have 2 connection point between the detector ement and the antenna marked GND and DI+ [(Photo)](https://fccid.io/2AKIT-MCCGQ11LM/Internal-Photos/Internal-Photos-3246095).  
Its input have very high impedance so was testing with 1 Meg Ohm resistor and its detecting contact closed.  
The smoke detector delivering 9V in alarm state and we need have it to being around 3V. = 1/3.  
So putting one 3 Meg Ohm resistor in serie with pin 7 to DI+ and one around 1 Meg Ohm (smaller its OK but not larger) between DI+ and GND and one wire from GND to the smokedetector GND /  - Battery.  
Then the smoke detector is in normal state (pin 7 its floating) its only 1 Meg Ohm between D1+ and GND = contact closed, in alarm state (9V from pin 7) 9V its going thrue the resistors (3M + 1M) to ground and the ID+ get around 3V = cotact its open. 

Its not so easy soldring on the small pads for the D1+ and GND and its microcomponents near so one alternativ its soldring on or desoldring the detctor element and soldring on its pads that its larger and near the PCB boarder. Taking the D1+ and GND there its the easyest way but must mesuring where side its D1+ and GND or you getting -3V in the ZigBee chip.  

If  having enugh space in the smok detector its only putting it back in the case or only the lower part with the protection for the batery.
If not only wrapping it with somthing protecting tape and putting it inside the smoke detector.  
Dont forget not covering the battery to good then its needs being changed time 2 time.  

One its done and working good for weeks and 2 more its waiting for being modded after next tripp to CyberPort.
