HX711-multi
=====

This is a modification of Compugician's (https://github.com/compugician/HX711-multi) HX711 library for the Avia Semiconductor HX711 24-Bit Analog-to-Digital Converter for scales (load cells) (ADC / LCA) [Datasheet: http://www.dfrobot.com/image/data/SEN0160/hx711_english.pdf]

# My modifications
Added timeout for the reading od multi HX711. If one of the load cell goes to power down mode / ganddout, it will wait foe the set timeout for reseting all the load cell.

# Future updates
Only the HX711 that powered down will be reseted, maybe taht will decrese the delay of resetting them all.

# Tested
I am using Teensy 3.5 as the microcontroller and SparkFun's HX711 [https://www.sparkfun.com/products/13879] modifed to 80SPS
I personally tested this package with 8 HX711 and 8 load cell and it works fine for me with about 78Hz.


# Advantages of this library
In its current form, it is stripped of a lot of functionality (like tare, unit conversion, etc.) though this functionality is easy to implement outside the library if neccessary, and will be added to this library in the future.

The main difference this library introduces is the ability to sample multiple HX711 units simultaneously. 
It is optimized for intoducing minimal (effectively zero) overhead.

# Wiring
Connect all HX711 units to share a single clock line, and plug each data line from the HX711 to a different pin on the Arduino 

# How to use
See the examples section for usage, as well as some useful tools for evaluating your setup.
