# Emergency Panic Alarm Board

**Student: Mohak Saxena**  
KiCad 10 PCB design project | Revision 1.0

## Overview

A regulated 5 V, momentary push-to-sound alarm. Holding the normally-open panic button activates an internally driven buzzer and a red warning LED. Releasing the button turns both off. There is no latching/reset function.

The supplied brief contained a conflicting water-level-indicator sentence. This project follows its Emergency Panic Alarm Board title, alarm scenario, and listed components.

## Circuit

- **J1:** 2-pin, 5.08 mm power terminal; pin 1 = +5 V and pin 2 = GND.
- **SW1:** Normally-open, 6 mm through-hole push button.
- **BZ1:** CEM-1205-IC or mechanically/electrically compatible **active 5 V** buzzer; a passive transducer is not suitable without an oscillator.
- **R1:** 330 ohms, 0.25 W axial resistor.
- **D1:** Red 5 mm LED. With an assumed 2 V forward voltage, nominal LED current is approximately 9.1 mA.

Board: **50 x 38 mm**, two copper layers, 0.6 mm tracks, through-hole components, no vias.

## Files

| File | Purpose |
| --- | --- |
| `Emergency_Panic_Alarm_Board.kicad_pro` | KiCad project |
| `Emergency_Panic_Alarm_Board.kicad_sch` | Editable schematic |
| `Emergency_Panic_Alarm_Board.kicad_pcb` | Routed PCB |
| `Mohak_Saxena_Emergency_Panic_Alarm_Board_Report.pdf` | Six-page report with schematic, routed footprints, 2D/3D views, BOM and verification |
| `Mohak_Saxena_BOM.csv` | Bill of materials exported from KiCad |
| `Mohak_Saxena_PCB_Routed.png` | PCB Editor capture |
| `Mohak_Saxena_PCB_3D.png` | KiCad 3D Viewer export |
| `Mohak_Saxena_Gerbers.zip` | Gerber layers, job file and Excellon drill files |
| `Mohak_Saxena_KiCad_Project_and_Gerbers.zip` | Downloadable project/report/fabrication package |

Open the `.kicad_pro` file in KiCad 10. Standard KiCad symbol, footprint and 3D model libraries are required. If 3D models are not found on another computer, relink their paths to that computer's KiCad model library; model paths do not affect the copper design.

## Verification

KiCad's Electrical Rules Check reported **0 errors and 0 warnings**. The PCB Design Rules Check reported **0 errors, 0 warnings, 0 unconnected items and 0 schematic/PCB parity issues**, using project/default rule settings. The board was also inspected in KiCad's 3D Viewer.

## Fabrication and testing limits

**Educational prototype only - not a certified emergency or life-safety alarm.**

No physical assembly, bench testing or sound-level measurement has been performed. There is no battery backup, fault supervision, reverse-polarity protection or latched alarm. Before fabrication, confirm the purchased components' pin spacing, polarity, switch pin grouping, voltage/current ratings, enclosure fit and manufacturer capabilities. Use a current-limited regulated 5 V source during initial testing and inspect for shorts before applying power.

The Gerber archive includes front/back copper, solder mask and silkscreen, Edge.Cuts, a Gerber job file, and separate plated/non-plated Excellon drill files. Empty paste layers are included for this through-hole design.

## Reference

[Same Sky CEM-1205-IC manufacturer datasheet](https://www.sameskydevices.com/product/resource/cem-1205-ic.pdf)
