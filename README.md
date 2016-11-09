Welcome to the open waveblaster

this content is the same as wiki page

open design for convert [waveblaster](https://en.wikipedia.org/wiki/Creative_Wave_Blaster) daughter board to external midi 

# Hardware Requirement
## Waveblaster compatible daughter board
* Roland SCB-55 or 
* Yamaha DB60XG (or NEC)
* Korg (or Topwave 32)

### USB to MIDI adapter
e.g. http://www.esi-audio.com/products/midimate/

## PCB board for wiring all components together
* PCB
* 2 line LCD for display mode and channel
* switch/jumper for switch GM/XG mode
* LED

# Power supply design
## 5v: I recycle a AC -> 5V DC wall charger
## +/-12V: 
### design 1 I recycle a old Epson Printer Powe Supply [PA6509](https://goo.gl/photos/XxPtHDL55Mse3U8P7) which has 3 pins, the offset of voltage from the highest to the middle and the middle to lowest is around 16.6 ~ 17v
parts  
* 1* 7812
* 1* 7912
* 1* 500mA fuse
* 4* 0.01uF
* 2* 10uF (C5,6)
* 2* 1000uF (C1,2)  C1,C2,C5 and C6 must be rated at least 50V.

### design 2
use [this circuit](http://www.circuitstoday.com/regulated-dual-power-supply-circuit) 
extra parts 
* 4* 1n4007

### design 3
Muffsy Hifi Dual Power Supply
https://hackaday.io/project/5676-muffsy-hifi-dual-power-supply

* 1× LM317T Texas Instruments Power Management ICs / Linear Voltage Regulators and LDOs
* 1× LM337T Texas Instruments Power Management ICs / Linear Voltage Regulators and LDOs
* 7× 1N4004 Discrete Semiconductors / Diodes and Rectifiers
* 2× 300 ohm 0.25W metal film resistors, 1% tolerance
* 3× 3300 ohm 0.25W metal film resistors, 1% tolerance
* 2× 4.7 ohm 1W resistor
* 5× 0.1 uF (100 nF) Ceramic disc capacitor
* 2× 10 uF Electrolytic capacitor, 35 volts or higher
* 1× 220 uF Electrolytic capacitor, 35 volts or higher
* 4× 2200 uF Electrolytic capacitor, 35 volts or higher
* 1× 16VAC wallwart adapter (15 to 18VAC can be used) Single AC, 15-18V, with 2.1 mm female connector. See the project details for sources
* 1× 2.1 mm male power connector
* 1× DG301 - 2 positions Screw terminal
* 1× DG301 - 3 positions Screw terminal



# Reference

## general 
* https://forums.dearhoney.idv.tw/viewtopic.php?f=1&t=54984
* https://www.pjrc.com/teensy/td_libs_MIDI.html

## power supply
* [12 Volt Dual Power Supply circuit](http://www.circuitdiagramworld.com/power_supply_circuit_diagram/12_Volt_Dual_Power_Supply_circuit_12579.html)
* http://www.circuitstoday.com/regulated-dual-power-supply-circuit
* [Wall Wart Power Supply (+/-9V to +/-15V)](http://www.musicfromouterspace.com/analogsynth_new/WALLWARTSUPPLY/WALLWARTSUPPLY.php)
* [Muffsy Hifi Dual Power Supply](https://hackaday.io/project/5676-muffsy-hifi-dual-power-supply)


## waveblaster pin out
* spdif out

### USB to MIDI 
* Using Arduino [MIDI] (https://github.com/FortySevenEffects/arduino_midi_library/) or similar AVR chips
* Robert Lang's The [Midi-Nator](http://www.nutsvolts.com/media-files/215/MIDI-NATOR.zip)
* off the shelf SB MIDI Input Output Cable , [such as] (http://www.amazon.com/Input-Output-Cable-Converter-Notebook/dp/B001HPL8B2/ref=sr_1_3?ie=UTF8&s=miscellaneous&qid=1259723275&sr=8-3)

### i2S
*  off the shelf PCM5102 DAC Decoder I2S Player Board ~$7.91 on ebay 
or [Pimoroni pHAT DAC] (https://www.adafruit.com/product/30160) for Raspberry Pi Zero 
* testing via raspberry Pi
* TDA1543A

### spdif out
* [http://www.ne.jp/asahi/fa/efu/sc88p/sc88p.html archive] (http://web.archive.org/web/20090206030813/http://www.ne.jp/asahi/fa/efu/sc88p/sc88p.html)
* [http://www.yk.rim.or.jp/~okkun/dtm/sc_kai/index.html archive](http://web.archive.org/web/20081012131906/http://www.yk.rim.or.jp/~okkun/dtm/sc_kai/index.html)
* [http://www.uyouyo.com/special/soundcrd/sc88.htm archive](http://web.archive.org/web/20110829070958/http://www.uyouyo.com/special/soundcrd/sc88.htm)
* http://www3.big.or.jp/~fujikko/sc88vl/index.html
