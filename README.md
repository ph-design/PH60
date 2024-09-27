# PH60
A 60% ISO/ANSI Keyboard.
An ISO/IEC 9995 60% layout Keyboard.

## Specification

1. Fully 3D-printed Case that can be printed on any 3D printer which has a build plate larger than 250mm*250mm
2. Gasket Mount
3. Raspberry Pi RP2040 MCU
4. Open-Source QMK firmware with VIA support (by json)
5. Separate daughter board for USB-C plug

## Assembling

1. Print all components, ensuring that the plate should be divided into two parts for printing. Alternatively, consider finding a manufacturer to produce a version in FR-4 or other materials.
2. Align the two upper cover rails and press them firmly until the surfaces are flush.
3. Use the same method to install the bottom cases on both sides.
4. Stick Poron foam around the edges of the mounting plate on both sides.
5. Place the daughter board into the central clip and secure it firmly. Lift the cover of the Molex connector, insert the FFC cable, and press the cover down tightly.
6. Insert several key switches around the corners and in the center of the alignment plate. Flip the plate over and press the PCB firmly against it. Remember to align the switch pins and hotswap socket to avoid bended pins.
7. Flip the PCB, install all the stabilizers, and perform a test.
8. Install all the swiches.
9. Connect the FFC cable to the PCB.
10. Place the plate and PCB into the bottom case. Hook the front edge of the upper cover into the groove of the bottom case on the user-facing side, then firmly press down on the other side of the upper cover until it is flush with the bottom.
11. Lock the clips in place.
12. Install all the keycaps.

## Caution

If you are soldering PCB by hand, avoid using Sn42Bi58 low-temperature solder paste. That will cause loose contact between the PCB and the hotswap socket under tough usage.
