Raspberry Pi Power Hat
======================

WORK IN PROGRESS - Not tested!

A Hat for the Raspberry Pi to supply 5V though the 40pin header from a 7-36V DC source rather than using the USB plug.

When using the 7" Pi Display the voltage drop across the USB cable (esp. if long) may be too much for the Pi. This hat allows a higher voltage to be dropped 
right as it is needed and distributed to the Pi and the display so reducing the voltage drop.

Rather than design and source a buck switching supply this hat uses one of the many cheap "eBay" buck converts that have the 
standard 7805 footprint (Don't use an actual 7805!).

e.g. a PM-5033-1 36 V In, 5V 2.5A Out buck converter. http://www.ebay.co.uk/itm/262241859833

The PCB also includes:
* INA219 to measure the power via a current sense resistor (R4 - value to be determined)
* The normal Pi HAT EEprom
* DS18B20 - SOIC 8 footprint by the converter to monitor PCB temperature.
* DS18B20 - TO-92 (3 Pin) to measure ambient temperature
* 3 Pin Molex header for off-board DB18B20's
* 4 Pin Molex header for Pi 7" display (GND, 5V, I2C connections).


Pi Hat original schema/PCB (connector, shape, EEprom) but Ivan Zilic (http://www.flyfish-tech.com)
Source: 
https://www.raspberrypi.org/forums/viewtopic.php?f=100&t=82618
http://www.flyfish-tech.com/pub/RasPi-BplusHAT.zip

Component Libraries:
SparkFun - https://github.com/sparkfun/SparkFun-Eagle-Libraries
DS18B20-SOIC - ??
INA219 - Farnell

See https://github.com/Tinamous/OctoPrint-PiPower for an OctoPrint plugin to monitor and control.

