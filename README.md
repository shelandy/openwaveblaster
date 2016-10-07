Welcome to the open waveblaster

this content is the same as wiki page

open design for convert [waveblaster](https://en.wikipedia.org/wiki/Creative_Wave_Blaster) daughter board to external midi 

# Hardware Requirement
## Waveblaster compatible daughter board
* Roland SCB-55 or 
* Yamaha DB60XG (or NEC)
* Korg (or Topwave 32)

## Power supply 
5v
+-12V 
3.7~4.2v (18650) *3 =11.1~12.6V

### USB to MIDI adapter
e.g. http://www.esi-audio.com/products/midimate/

## PCB board for wiring all components together
* PCB
* 2 line LCD for display mode and channel
* switch/jumper for switch GM/XG mode
* LED

# Reference

## general 
* https://forums.dearhoney.idv.tw/viewtopic.php?f=1&t=54984
* https://www.pjrc.com/teensy/td_libs_MIDI.html

## power supply

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
