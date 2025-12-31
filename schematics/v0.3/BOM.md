# Bill of Materials (BOM) - BomboPad v0.3

This Bill of Materials is compliant with OSHWA (Open Source Hardware Association) specifications.

## Main Components

| Designator | Description                        | Quantity | Footprint              | Manufacturer                | Part Number                |
|------------|------------------------------------|----------|------------------------|-----------------------------|----------------------------|
| D1-D12     | Switching Diode                    | 12       | SOD-123 / Through-hole | Generic                     | 1N4148W                    |
| J1         | Battery Connector 2-pin (Optional) | 1        | Molex PicoBlade 1.25mm | Molex                       | 53048-0210                 |
| J2         | Battery Connector 3-pin (Optional) | 1        | Molex PicoBlade 1.25mm | Molex                       | 53048-0310                 |
| MCU1       | Microcontroller Module             | 1        | Pro Micro / Nice!Nano  | Generic / Nice Technologies | Pro Micro / Nice!Nano      |
| Display    | Display Module (Optional)          | 1        | niceview_headers       | Generic / Nice Technologies | SSD1306 128x32 / Nice!View |
| ROL1, ROL2 | Encoder (Optional)                 | 2        | EVQWGD001              | Panasonic                   | EVQWGD001                  |
| ROT1, ROT2 | Encoder (Optional)                 | 2        | EC11                   | Generic                     | EC11                       |
| S1-S10     | Low Profile Switches               | 10       | Kailh Choc v1 (PG1350) | Kailh                       | PG1350                     |
| S11-S12    | Low Profile Switches (Optional)    | 2        | Kailh Choc v1 (PG1350) | Kailh                       | PG1350                     |
| S13        | Reset Button                       | 1        | 6x6mm Tactile Switch   | Generic                     | SW_Push_1P1T               |
| SW15       | Power Switch (Slide)               | 1        | DPDT Angled            | Generic                     | JS202011AQN                |

## Notes

- **Display**: The OLED (SSD1306 128x32) and Memory Display (Nice!View) are both optional and mutually exclusive
  alternatives. Choose one based on your microcontroller: the OLED is typically used with Pro Micro, while the Nice!View
  is designed for Nice!Nano.
- **Encoders**: The EC11 rotary encoders and EVQWGD001 roller encoders are optional and mutually exclusive
  alternatives. If neither type of encoder is installed, it is recommended to use 2 additional Kailh Choc v1 switches
  (S11 and S12) instead.
- **Switches**: S11 and S12 can be either the integrated push-buttons of the encoders or two standard Kailh Choc v1
  switches if no encoders are used.
- **Microcontroller**:
    - Use a Pro Micro for wired setups (USB-C recommended):
        - MCU with `ATmega32U4` processor is fully tested and regularly used.
        - MCU with `RP2040` processor is verified and works fine, but not exhaustively tested.
    - Use a Nice!Nano compatible for wireless setups:
        - Nice!Nano v2 MCU is fully tested and regularly used.
        - SuperMini NRF52840 MCU is verified and works fine, but not exhaustively tested.
- **Diodes**: Any 1N4148 diode will work. Diodes can be SMD (SOD-123 package) or through-hole.

## License

Copyright (C) 2024-2025 Gianni Bombelli <bombo82@giannibombelli.it>

This document is part of the BomboPad hardware design and is licensed under CERN Open Hardware Licence as published by
the CERN, either version 2 of the Licence, or (at your option) any later version.

You may redistribute and modify this source and make products using it under the terms of the CERN-OHL-S
v2 (https://ohwr.org/cern_ohl_s_v2.txt).
