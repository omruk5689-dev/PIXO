# PIXO — Design Journal

## Project Summary

| Project Name | Time Taken | Design Tool |
|---|---|---|
| PIXO | ~6 hours 20 minutes | EasyEDA Pro |

## Build Log

### Hour 1 — Getting Parts Onto the Page
Started by dropping in all the main components — the ATmega328P, USB-C connector, CH340C, the regulators, crystal, and the header footprints for the pinout. Nothing wired yet at this point, just getting everything laid out so I could see the whole board at once.

### Hour 2 — Wiring the Core
Started connecting things up — MCU to crystal, power in through USB-C and the DC jack, and getting the CH340C hooked into the USB lines and the MCU's serial pins. This part took a bit of care since the USB-C CC/D+/D- wiring has to be right or nothing enumerates.

### Hour 3 — Finishing the Schematic
Kept going on the wiring — regulators into the power rails, LEDs and the op-amp LED stage, the reset button, and the ISP header. By the end of this hour the schematic was fully connected and double-checked against the datasheets.
<img width="3332" height="2362" alt="SCH_Schematic1_1-P1_2026-09-28" src="https://github.com/user-attachments/assets/d9f343b6-6de6-4504-9bee-ef40086b355e" />

### Hour 4 — PCB Layout
Moved into the PCB view and placed everything — kept the USB-C and CH340 close together, put the regulators near the power input, and arranged the header pins so the pinout would actually make sense to use later.

### Hour 5 — Routing
Routed the whole board — power traces, the USB differential pair, the crystal traces (kept those short like you're supposed to), and all the header connections.
<img width="2160" height="1651" alt="3D_PCB1_2026-09-28 (2)" src="https://github.com/user-attachments/assets/45fa4f31-a711-4a08-985e-2f2e79b9e3bb" />

### Last 1 Hour 20 Minutes — Cleaning Up Errors
Ran the DRC and went through the usual list of issues — a couple of clearance warnings, one unrouted net I'd missed, and a footprint mismatch on one of the headers. Fixed everything up, ran it again to make sure it came back clean, and called it done.

## Notes
- Tool used throughout: **EasyEDA Pro**
- MCU: ATmega328P-AU
