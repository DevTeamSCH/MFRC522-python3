MFRC522-python
==============

A small class to interface with the NFC reader Module MFRC522 via SPI.

This is a Python port of the example code for the NFC module MF522-AN.

Updated by @brettcvz to be a bit more generic, and be importable into other projects

##Installation
Run the following command:
```
pip install git+https://github.com/DevTeamSCH/MFRC522-python3.git --process-dependency-links
```
Note that the depency link command is required for CHIP support, because the CHIP_IO repo is not on PyPI

##Examples
This repository includes a couple of examples showing how to read, write, and dump data from a chip. They are thoroughly commented, and should be easy to understand.

## Pins and setup
In the general case, you need to hook up the MFRC522 via SPI and drive the RST pin HIGH when you would like to read or write RFID chips.

For Rasperry Pi in specific, you can use [this](http://i.imgur.com/y7Fnvhq.png) image for reference.

| Name | Pin # | Pin name   |
|------|-------|------------|
| SDA  | 24    | GPIO8      |
| SCK  | 23    | GPIO11     |
| MOSI | 19    | GPIO10     |
| MISO | 21    | GPIO9      |
| IRQ  | None  | None       |
| GND  | Any   | Any Ground |
| RST  | 22    | GPIO25     |
| 3.3V | 1     | 3V3        |

##Usage
Import the class by importing MFRC522 in the top of your script. For more info see the examples.
