ATMEGA8 (Int. Clock 8 Mhz)
==========================

Sometimes I need to develop project from scratch with atmega8 chip onboard using 16 Mhz Ext. Oscillator but sometimes using 8 Mhz Int. Oscillator

With Internal oscillator, so we have PB6 and PB7 as I/O PIN. To make these pin available with arduino IDE we need to modify pins_arduino.h

  (oscl)<br>
  /    \<br>
PB6    PB7

  Newly available pins are mapped as:
  
  PB6 = Arduino Pin 20
  PB7 = Arduino Pin 21

Actually pins_arduino.h design for atmega328 but also works with atmega8, pins are same.

include with boards.txt for ATmega8 (Int. 8MHz Clock) board.


CPU Information
===============

Maximum upload size 8192 bytes, 512 bytes EEPROM, 1024 bytes SRAM

Fusebit 8 Mhz Int. Oscillator

low_fuses = 0xE4<br>
high_fuses = 0xD9<br>
unlock_bits = 0x3F<br>
lock_bits = 0x0F

Power Consumption at 4Mhz, 3V, 25C
- Active: 3.6mA
- Idle Mode: 1.0mA
- Power-down Mode: 0.5 uA