# PIXO
![Uploading 3D_PCB1_2026-09-28 (2).png…]()

PIXO is a little ATmega328P board I've made myself, kind of an Arduino Uno with my own spin on it – no USB-B, no extra modules required,
CH340 onboard so it works straight out of the box with a plain old cable, and all pins separated for easy use with a breadboard.
## Main Controller
 
Went with the **ATmega328P** since it's cheap, well supported, and I didn't need anything more powerful for what this board is meant to do. 
It's running off a 16MHz crystal so it behaves exactly like a standard Arduino as far as timing and bootloaders go.
 
I made this to have something simple to play around with that wouldn't need me to constantly drag along my Arduino Uno.

## Features
- ATmega328P-AU as the main MCU (Arduino-compatible)
- USB Type-C input
- CH340C onboard for USB-to-serial, so uploading sketches is plug-and-play
- Onboard 5V and 3.3V regulation (AMS1117 regulators)
- 6-pin ISP header for programming/flashing
- Physical reset button
- Power and status LEDs, including an op-amp buffered LED stage
- Full pinout broken out — digital IO, analog, I2C, SPI, plus dedicated power pins
- 16MHz crystal for standard Arduino timing

  ## USB & Programming
 
Instead of relying on an external USB-to-serial adapter, I put a **CH340C** right on the board, wired to a USB-C connector. 
This means you can just plug it into your laptop and upload code straight from the Arduino IDE (or whatever toolchain you're using) — no extra hardware needed.
There's also a proper 6-pin ISP header broken out (MISO, MOSI, SCK, RESET) for anyone who wants to flash a bootloader directly or program it with an external programmer instead of going through serial.
## Why I Did It That Way

Frankly speaking, I grew tired of having to use an adapter or some particular cable each time I wanted to test my ideas quickly. Placing the CH340 and USB-C connections right on the board made this possible, and including every pin makes sure that I do not have to invent anything by using jumper wires each time I want to add an extra analog input. And that’s how this board is supposed to be used.

## Credits

Designed and developed by Omer Ruknuddin
 
PCB Design: EasyEDA Pro
