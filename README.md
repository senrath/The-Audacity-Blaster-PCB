# The Audacity PCB for Brushless Nerf Blasters
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

## Features
- RP2040-Zero MCU
- Easy connections to most of the GPIO pins
- Buck converter to power the RP2040 directly from battery (3S or 4S)
- Jumper on the 5V power line to alternatively allow the RP2040 to be powered by USB for debugging
- MOSFET for solenoid control
- Rapid decay circuit for solenoid
- Voltage divider for voltage sensing

## Important Notes
- THERE HAS BEEN SOME CONCERN THAT ATTEMPTING TO RUN A HIGH ENOUGH LOAD THROUGH THE ESCS MAY DAMAGE THE BOARD. While I have not damaged the board in my testing, if you are concerned about this you may either reinforce the connection between POWER1 and ESCPOWER1 or simply not use ESCPOWER1 at all.
- The current iteration of the board is 50mmx50mm.
- The components were chosen specifically with JLCPCB's basic and extended basic libraries in mind, when at all possible. If you end up using a different service other comparable components may be cheaper.
- The included BOM and PickAndPlace xlsx files only include the non-RP2040 SMD components.
- The EasyEDA Pro project file is included if you wish to make changes (such as including the through hole components in the automated assembly).
- Because they were not intended to be part of the automated assembly through hole components were only selected for their footprint and may or may not be part of basic and extended basic, if you include them in assembly you may wish to swap them out.
- While the schematic calls for 100uF electrolytic capacitors I have been using 47uF in my testing (because they're what I had on hand) with no issues.
- The three power connections (POWER1, ESCPOWER1, SOLENOID1) are intended to be empty holes for wires to be inserted through and then soldered, there are no components that go there.
- While the RP2040-Zero can be soldered with an iron it is much easier to do a with a hot plate or reflow oven.

## Components To Be Hand Soldered
- 1x RP2040-Zero
- 2x 100uF electrolytic capacitors
- 2x 2x9P 2.54mm Pin Headers
- 1x 2x5P 2.54mm Pin Header
- 1x 1x2P 2.54mm Pin Header
- 16AWG wire and connectors as appropriate for your battery, ESC, and solenoid.

# Licensing
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg