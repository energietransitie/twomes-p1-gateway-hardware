# Twomes P1 Gateway Hardware

This repository contains the open hardware design files for the Twomes P1 Gateway device, this is a dedicated device, which can wirelessly receive data from various other Twomes sensor using ESP-Now, and can connect to the P1 port of a Dutch smart energy meter, to receive data.
The Twomes P1 Gateway can send this data to the Twomes Backoffice database using secure HTTPS.
The P1 Gateway is uses an ESP32 Microcontroller and can be powered either directly through the P1 port itself on DSMR version 5.0, or through a seperate USB port on DSMR version 4.x Smart Meters

<img src="./images/front.jpg" height="600" /> <img src="./images/back.jpg" height="600" />

## Table of contents
* [General info](#general-info)
* [Prerequisites](#prerequisites)
* [Producing](#producing)
* [Developing](#developing) 
* [Features](#features)
* [Status](#status)
* [License](#license)
* [Credits](#credits)

## General info
This repository will contain the hardware designs, such as schematics and board layout files for the Twomes P1 Gateway device.

For the associated firmwware that you can run on this device, please see [this repository](https://github.com/energietransitie/twomes-p1-port-logger-gateway).

## Prerequisites
Describe which hardware and software you need to produce and/or develop the hardawre. If the prerequisites are different for users that only wish to produce hardware versus uers that (also) wish to develop new versions of the hardware, you may want to move the prerequisites section as a subsection of each of those sections.

## Producing

The folder [Output_files](https://github.com/energietransitie/twomes-P1-gateway-hardware/tree/main/TwomesGateway/Output_files/FABRICATION) contains the necessary files to manufacture the PCBs. The files have been exported through the requirements of [JLCPCB](https://www.jlcpcb.com).

The folder [Twomes P1 Gateway Enclosures](https://github.com/energietransitie/twomes-P1-gateway-hardware/tree/main/Twomes%20P1%20Gateway%20Enclosures) contains both, Fusion360 source files, and exported STL files for the Twomes P1 enclosures. The STL files can be imported into any slicer and turned into G-Code for a 3D printer.

### Printed Ciruit Board
The fabrication output files can be ordered from JLCPCB, upload the Gerber files in a zip to their [quote page](https://cart.jlcpcb.com/quote)
Select the amount of PCBs and a colour for silkscreen. All other options can be left on default.

if SMT assembly is desired, also select this option before ordering. This will take you to a page where the BOM and POS file can be uploaded. These can be found [here](https://github.com/energietransitie/twomes-P1-gateway-hardware/tree/main/TwomesGateway/Output_files/FABRICATION/BOM_AND_POS) Use the files "BOM_TwomesGatewayJLCPCB.csv" and "TwomesGateway-top-pos.csv"


### Enclosure
The enclosures can be 3D printed. open the STL files with your preferred slicer software and export it with the settings best suited for your printer.
If the printing is handled by an external source, send the STL files to their service.

## Developing
### Developing the PCBs
The PCB files are designed using KiCad, which can be downloaded [here](https://www.kicad.org/download/) for free.
Alternatively the files can sometimes be imported/converted to different EDA tools.

To export the modified PCBs. Consult the webpage of the PCB manufacturer for a guide on how their service prefers the output files.
JLCPCB has a guide on how to export Gerbers [here](https://support.jlcpcb.com/article/149-how-to-generate-gerber-and-drill-files-in-kicad) and on how to export the BOM and POS files [here](https://support.jlcpcb.com/article/84-how-to-generate-the-bom-and-centroid-file-from-kicad)

## Features
The Twomes P1 Gateway contains an ESP32 Microcontroller, an FTDI compatible serial programming header, a USB input for a power supply, and a RJ12 port to connect to the P1 port of a smart meter.

## Status
Project is: _Ready for testing_

## License
The hardware designs in this repository are available under the [CERN-OHL-P v2 license](./LICENSE.md), Copyright 2021 [Research group Energy Transition, Windesheim University of Applied Sciences](https://windesheim.nl/energietransitie)

## Credits
This open hardware design is a collaborative effort of:
* Sjors Smit · [@Shorts1999](https://github.com/Shorts1999)

Thanks also go to:
* Fredrik-Otto Lautenbag ·  [@Fredrik1997](https://github.com/Fredrik1997)
* Gerwin Buma ·  [@GerwinBuma](https://github.com/GerwinBuma) 
* Marco Winkelman · [@MarcoW71](https://github.com/MarcoW71)

Product owner:
* Marco Winkelman · [@MarcoW71](https://github.com/MarcoW71)

We use and gratefully aknowlegde the efforts of the makers of the following designs:
* [KiCad](https://www.kicad.org), licensed under [GNU GPL v3](http://www.gnu.org/licenses/gpl-3.0.en.html)

