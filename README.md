6530 Replacement
================
Replaces the 6530 ICs found on early revision Allied Leisure pinball machines.

Components
----------
Please note these designs and instructions come with absolutely no warranty, implied or otherwise. I write these instructions assuming the builder has experience in assembling electronics.

You will need:
 - x1 27C64 EPROM (or equivalent)
 - x1 28 pin IC socket
 - x2 6532 IC's
 - x2 40 pin IC socket
 - x1 74LS42 IC
 - x1 16 pin IC socket
 - x1 74LS11 IC
 - x2 74LS00 IC
 - x3 14 pin IC socket
 - x6 1N4148 silicon diodes
 - x1 2N7000 transistor
 - x3 1k ohm 1/4W resistors
 - x1 1k x6 resistor network (or alternatively an additional 6 1k ohm 1/4W resistors)
 - x6 100nF 50V monolithic capacitors
 - x100 pin headers to fit the original sockets on the CPU board (5 rows of 20 pins)

To have these boards manufactured, it should be as simple as zipping the 6530-Replacement-Gerber folder and submitting them to a PCB manufacturer. The board dimensions are 100.3 x 100.3mm

ROMs
----
I can not host the ROM image here as they are copyrighted. I have supplied a 1k blank image to assist with generating the required ROM image.

There are three ROM images I was supplied with, one each from the three original 6530's:
 - EE1712_82219_DG_MOS6530_009.bin
 - EE1712_82219_DG_MOS6530_010.bin
 - EE1712_82219_DG_MOS6530_011.bin

To generate a ROM image for the board on Linux or Mac in the terminal:
`cat Blank1k.bin Blank1k.bin Blank1k.bin EE1712_82219_DG_MOS6530_009.bin Blank1k.bin EE1712_82219_DG_MOS6530_010.bin EE1712_82219_DG_MOS6530_011.bin Blank1k.bin > AdaptorROM.bin`

And on the Windows command prompt:
`copy /b Blank1k.bin+Blank1k.bin+Blank1k.bin+EE1712_82219_DG_MOS6530_009.bin+Blank1k.bin+EE1712_82219_DG_MOS6530_010.bin+EE1712_82219_DG_MOS6530_011.bin+Blank1k.bin AdaptorROM.bin`

You will first need to `cd` to the directory the ROMs are in. This will give you an 8kB ROM image ready to burn to a 27C64 or equivalent EPROM.

Construction notes
------------------
Construction should be straight forward, following the usual rules. The only thing to be careful of is the alignment of the pin headers, so they fit in the sockets.

If you are using a resistor network for RN1, the dot needs to align with the square pad.

Good luck!
