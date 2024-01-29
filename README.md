# pusheenz40
An experimental ultraportable keyboard that uses SMD mouse switches to achieve a compact form factor (8mm thick) while still being viable as a daily use keyboard. Entire PCBA can be produced by JLCPCB. Uses 3D printed keycaps.

![a photo of a pusheenz40](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20231127_044255454.jpg)

# Status
v0.0 PCBs are working! Happy to open up this project for others to play with.

Disclaimer is that this design has very low tolerances for its key switches. You will likely need a 3D printer such as a Bambu Lab A1/A1 mini/P1P/P1S and set the slicing layer resolution to 0.08mm. Printers like the Prusa i3/mini may also work, but have not been tested.

# About
I hit the limit as how small I could go with choc switches. I found that kailh mute switches are an ideal small form factor alternative in terms of their size, durability, and actuation force. To make this board more accessible to build at home, it uses a rp2040-zero board that can be soldered on.

More details about my research on mouse switches and experience with the pusheenz40 can be found here: https://chrischrislolo.github.io/orthoLabLogs/pusheenz40.html

Case files include STLs, STEP files, as well as source OpenSCAD files that can be modified. The OpenSCAD models do not have fillets on them

![a pusheenz40](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20231127_025242231.jpg)


# Case
The case files can be found in the `case` directory. The particular files you'll want are the `case_holes` file for the top part of the case, and the `case_holes_floor` file for the bottom part. CNC and 3DP works with the top part of the case, and I chose to 3DP my case bottom.

![pusheenz40 in my hand](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20231125_222231348.jpg)

## PCB
You can find the PCB source files in the `pcb` folder. The BOM files can be found in this folder.

## Directory Structure
- `case`
    You can find the files you need in this folder to print out a case for the keyboard
- `drafts`
    Stores any KLE or intermediate information used in making the case
- `outlines`
    Outlines used to create the case and pcb
- `pcb`
    Kicad project relating to the project
   
## BOM
- 1 PCB
- 1 Aluminum CNC upper case or 3DP upper case
- 1 lower case. I 3D printed mine
- 16 3mm M1.6 screws (go for flathead for a flush fit, though other head types should also work)
- 4-8 (ideally 8) 1-2mm bumpons (something like Sj5302 is a good place to start)
- 1 0.91 inch OLED
- 1 rp2040-zero pcb
- 40 Kailh/Huano 7.3mm mute switches (ideally with some spares)
- 40 LL4148 diodes (ideally with some spares)

## Assembly
Build guide coming soon. For now, hopefully the footprints make it clear as to what should go where. Note that the rp2040-zero should be placed in such a way that the MCU is on "top" of the pcb when the assembly is face up, like such.
![photo of assembly](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20231105_230039555.jpg)

Once all parts have been assembled, the board can be screwed onto the top of the case with 8 screws.

The firmware should then be flashed onto the board.

The bottom of the board can then be screwed to the case. My recommendation is to put two bumpons on each corner of the bottom of the case, one above the screw and one beside the screw. This helps maximize stability.  

## Firmware
QMK Firmware can be found here
https://github.com/ChrisChrisLoLo/vial-qmk/tree/sporewoh/keyboards/sporewoh/pusheenz40