# Macropad

A compact 9-key macropad with 2 rotary encoders, programmed with QMK firmware. I built this project to challenge myself and gain hands-on experience with PCB design, firmware configuration, and hardware assembly, serving as a foundation for more advanced future projects, such as designing a miniature fan in the shape of a plane engine.

The macropad is designed as a programmable input device suitable for shortcuts, media control, and custom workflows.

---

## Overview

<img width="1403" height="752" alt="Overall Macropad" src="https://github.com/user-attachments/assets/bd975700-22de-424c-b6b9-601b1c683ee5" />

---

## Schematic

The schematic shows the wiring between the Seeed XIAO RP2040 microcontroller, the 3×3 switch matrix with 1N4148 diodes, and the two EC11 rotary encoders.

<img width="740" height="544" alt="Schematic" src="https://github.com/user-attachments/assets/fdaebf5a-4f3d-4aa6-bb35-eb7b61c48b46" />

---

## PCB Design

The PCB is a custom 2-layer board designed in KiCad. The switch matrix is arranged in a 3×3 grid with diodes for each key to prevent ghosting. The two rotary encoders are mounted at the top of the board on either side of the XIAO.

<img width="530" height="635" alt="PCB Layout" src="https://github.com/user-attachments/assets/7c2ae1f0-64a9-421b-a9ad-0e8531b41517" />

Front copper layer:

<img width="358" height="436" alt="PCB Front" src="https://github.com/user-attachments/assets/f0cc5a3a-8cf3-4234-9356-3f56e48857bd" />

Back copper layer:

<img width="367" height="425" alt="PCB Back" src="https://github.com/user-attachments/assets/e5b77eed-1798-4334-8eb7-646d7df41e5b" />

---

## Case Assembly

The enclosure is a 3D-printed case secured with M3 brass heat-set inserts and M3 × 16 mm screws. The case is designed to hold the PCB snugly while keeping the switches and encoders accessible from the top.

<img width="677" height="404" alt="Case Top View" src="https://github.com/user-attachments/assets/49652a7a-4671-4cbd-9522-f0a8ada79590" />

<img width="701" height="365" alt="Case Side View" src="https://github.com/user-attachments/assets/88e080a1-73fc-4d79-8488-70b42afe4589" />

<img width="508" height="315" alt="Case Assembly" src="https://github.com/user-attachments/assets/372f8bc0-0d40-411c-a41f-00483a975cf3" />

---

## Bill of Materials

| Component | Quantity | Part |
|---|---|---|
| Microcontroller | 1x | Seeed XIAO RP2040 |
| Mechanical Switches | 9x | MX-style switches |
| Keycaps | 9x | ABS Keycaps |
| Rotary Encoder | 2x | EC11 |
| Diodes | 9x | 1N4148 |
| Brass Heat-Set Inserts | 4x | M3 |
| Screws | 4x | M3 × 16 mm |
| PCB | 1x | Custom 2-layer PCB |
| Case | 1x | 3D-printed enclosure |

---

## Firmware

This macropad runs [QMK Firmware](https://qmk.fm/). The default keymap assigns keys 1–9 to the switch matrix. The left encoder controls page up/down and the right encoder controls volume up/down.

To flash the firmware:
1. Hold the **BOOT** button on the XIAO and plug it into your computer via USB
2. A drive called **RPI-RP2** will appear
3. Drag and drop `firmware.uf2` onto that drive
4. The drive will disappear and the macropad will reboot with the new firmware
