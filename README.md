# BomboPad

BomboPad is an open-source, versatile 12-key macropad featuring dual rotary encoders and display support. Designed with
a focus on flexibility, it supports both wired and wireless configurations.

This repository contains the hardware design files, including electrical schematics and PCB layouts.

## Key Features

The current hardware version (**v0.3**) includes:

- **12 keys**: Designed for Kailh Choc v1 low-profile switches.
- **Dual Rotary Encoders**: Supports EC11 or EVQWGD001 encoders.
- **Display Support**: Compatible with SSD1306 128x32 OLED or Nice!View displays.
- **Microcontroller Compatibility**:
    - **Pro Micro** (or compatible) for wired builds.
    - **Nice!Nano** (or compatible) for wireless Bluetooth builds.
- **Battery Management**: Optional Li-Po battery and dedicated power switch for wireless operation.

## Getting Started (v0.3)

To build your own BomboPad, follow these steps:

### 1. Hardware Requirements

- **PCB**: You can order the PCB using the provided [Gerber files](./gerbers/v0.3).
- **Components**: Refer to the **[Bill of Materials (BOM)](./schematics/v0.3/BOM.md)** for a complete list of required
  parts (switches, encoders, diodes, etc.).
- **Microcontroller**: Pro Micro or Nice!Nano.

### 2. Assembly

The electrical schematics and PCB layout files are available in the **[schematics/](./schematics/v0.3)** directory (
KiCad format).

### 3. Firmware

Choose the firmware that best fits your needs:

- **[QMK Firmware](https://github.com/bombo82/qmk_bombopad)**: Best for wired builds using a Pro Micro. Supports
  advanced features and optionally VIAL for real-time configuration.
- **[ZMK Firmware](https://github.com/bombo82/zmk-bombopad)**: Recommended for wireless builds using a Nice!Nano.

## Project Structure

- **`gerbers/`**: Production-ready Gerber files for PCB manufacturing.
- **`schematics/`**: KiCad project files, including schematics and PCB layout.
- **`BOM.md`**: Detailed Bill of Materials for the current hardware version.

## Version History

Summary of hardware evolution:

- **v0.3 (current)**
    - First version with PCB
    - Wired build using ProMicro compatible microcontroller with QMK or VIAL firmware
    - Wireless build using Nice!Nano compatible microcontroller with ZMK firmware
    - Kailh Choc v1 low-profile switch
    - EC11 rotary encoders or EVQWGD001 encoders
    - Optional display: SSD1306 128x32 on ProMicro microcontroller or Nice!View on Nice!Nano
    - Optional Lipo battery and power switch, depends on microcontroller capabilities
- **v0.2 (not compatible with QMK)**
    - Prototype on a solderless breadboard and a stripboard
    - Use expensive microcontroller and display
    - Bluetooth module and battery management module are integrate inside microcontroller
    - Shares the switch and encoders stripboard with v0.0
    - Disassembled to reuse some parts (microcontroller and display) to my own build of v0.3
- **v0.1 (never built)**
    - Scrapped at the design stage and never built
- **v0.0**
    - Initial prototype on a solderless breadboard and a stripboard
    - Low cost compoments
    - MX switch, EC11 rotary encoders, SSD1306 OLED 128x64 Pixel I2C
    - External HC-06 Bluetooth serial UART module

## Help & Contributions

Bug reports, suggestions, and contributions are welcome! Please
use [GitHub Issues](https://github.com/bombo82/bombopad/issues)
and [Discussions](https://github.com/bombo82/bombopad/discussions) for any feedback.

## Authors

- **Gianni Bombelli (bombo82)** - [GitHub Profile](https://github.com/bombo82)

## Licenses

Documentation are licensed under GNU Free Documentation License as published by the Free Software Foundation, either
version 1.3 of the License, or (at your option) any later version.

Source code are licensed under GNU General Public License as published by the Free Software Foundation, either version 3
of the License, or (at your option) any later version.

Hardware design and all related things are licensed under CERN Open Hardware Licence as published by the CERN, either
version 2 of the Licence, or (at your option) any later version.

## License Disclaimer

Copyright (C) 2024-2025 Gianni Bombelli <bombo82@giannibombelli.it>

Permission is granted to copy, distribute and/or modify this document
under the terms of the GNU Free Documentation License, Version 1.3
or any later version published by the Free Software Foundation;
with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.

You should have received a copy of the GNU Free Documentation License
along with this program. If not, see <https://www.gnu.org/licenses/fdl-1.3.html>.

## Acknowledgements

Special thanks to [Arialdo](https://github.com/arialdomartini) for introducing me to the world of custom mechanical
keyboards.
