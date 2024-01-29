# pusheenz40
An experimental ultraportable keyboard that uses SMD mouse switches (EVQP0N02B) to achieve a compact form factor (8mm thick) while still being viable as a daily use keyboard (85+ wpm). Entire PCBA can be produced by JLCPCB. Uses 3D printed keycaps.

![a photo of a pusheenz40](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20240128_191510082.jpg)

# Status
v0.0 PCBs are working! A pcb produced from the files should work.

Disclaimer is that this design has very low tolerances for its key switches. You will likely need a 3D printer such as a Bambu Lab A1/A1 mini/P1P/P1S and set the slicing layer resolution to 0.08mm. Printers like the Prusa i3/mini may also work, but have not been tested.

# About
I hit the limit as how small I could go with choc switches. I found that kailh mute switches are an ideal small form factor alternative in terms of their size, durability, and actuation force. To make this board more accessible to build at home, it uses a rp2040-zero board that can be soldered on.

More details about my research on mouse switches and experience with the pusheenz40 can be found here: https://chrischrislolo.github.io/orthoLabLogs/pusheenz40.html

Case files include STLs, STEP files, as well as source OpenSCAD files that can be modified. The OpenSCAD models do not have fillets on them

![a pusheenz40](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20240128_191100052.jpg)


# Case
The case files can be found in the `case` directory. The particular files you'll want are the `case_holes` file for the top part of the case, and the `case_holes_floor` file for the bottom part. CNC and 3DP works with the top part of the case, and I chose to 3DP my case bottom.

3D printed cases can and should use the finest resolution possible on your printer, and ideally should use a higher end printer due to it's low tolerances. The models have been tested to work with the Bambu lab A1 and P1S at a layer height and detail setting of 0.08mm (extra fine). More details can be found in the BOM.

## PCB
You can find the PCB source files in the `pcb` folder. The BOM files can be found in this folder.

![pusheenz40 pcb](https://raw.githubusercontent.com/ChrisChrisLoLo/pusheenz40/main/photos/PXL_20231229_164239394.jpg)

## Directory Structure
- `case`
    You can find the files you need in this folder to print out a case for the keyboard
- `drafts`
    Stores any ergogen or intermediate information used in making the case
- `pcb`
    Kicad project relating to the project. Contains the BOM, placement files, and gerbers
   
## BOM
- 1 PCBA
  - The PCB will include all electrical parts required, including switches.
- 1 Aluminum CNC upper case or 3DP upper case
  - There is either the inverted rails or simple rails model. The simple rails model can be cnc'd, but has a tendency to have the buttons stick when pressed at a weird angle. The inverted rails model has less of this issue, but cannot be cnc'd due to its sharp edges.
- 40 3D printed buttons
- 8 3mm M1.6 screws (go for flathead for a more flush fit, though other head types should also work)
- 4-8 (ideally 8) 1-2mm bumpons (something like Sj5302 is a good place to start)

## Assembly
Pop the 3D printed buttons/keycaps into the case, and make sure they don't stick and can freely move up and down. If 

## Firmware
QMK Firmware can be found here
https://github.com/ChrisChrisLoLo/vial-qmk/tree/sporewoh/keyboards/sporewoh/pusheenz40
