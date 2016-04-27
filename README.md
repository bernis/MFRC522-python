MFRC522-python (modified for the PIGPIO IO library / SPI1)
==========================================================

A small class to interface with the NFC reader Module MFRC522 on the Raspberry Pi.

Using the PIGPIO library this fork of mxgxw's MFRC522 library is able to access the alternative SPI bus (SPI1) on Raspberry PIs with the 40 pin IO header. This is usefull if you have something else (a SPI display in my case) connected to the SPI0 port.

This is a Python port of the example code for the NFC module MF522-AN.

##Requirements
This code requires you to have PIGPIO installed:
http://abyz.co.uk/rpi/pigpio/
And its deamon pigpiod started (as root)

##Examples
This repository includes a couple of examples showing how to read, write, and dump data from a chip. They are thoroughly commented, and should be easy to understand.

## Pins
Your reader should be connected to the SPI1 port

| Name | Pin #   | Pin name   |
|------|---------|------------|
| SDA  | 36      | GPIO16     |
| SCK  | 40      | GPIO21     |
| MOSI | 38      | GPIO20     |
| MISO | 35      | GPIO19     |
| IRQ  | None    | None       |
| GND  | any (39)| Any Ground |
| RST  | 37      | GPIO26     |
| 3.3V | 17 or 1 | 3V3        |

##Usage
Import the class by importing MFRC522 in the top of your script. For more info see the examples.
