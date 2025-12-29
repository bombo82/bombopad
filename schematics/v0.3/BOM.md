# Bill of Materials (BOM) - BomboPad v0.3

This Bill of Materials is compliant with OSHWA (Open Source Hardware Association) specifications.

## Main Components

| Designator | Description                        | Quantity | Footprint              | Manufacturer                | Part Number                |
|------------|------------------------------------|----------|------------------------|-----------------------------|----------------------------|
| D1-D12     | Switching Diode                    | 12       | SOD-123 / Through-hole | Generic                     | 1N4148W                    |
| J1         | Battery Connector 2-pin (Optional) | 1        | Molex PicoBlade 1.25mm | Molex                       | 53048-0210                 |
| J2         | Battery Connector 3-pin (Optional) | 1        | Molex PicoBlade 1.25mm | Molex                       | 53048-0310                 |
| MCU1       | Microcontroller Module             | 1        | Pro Micro / nice!nano  | Generic / Nice Technologies | Pro Micro / nice!nano      |
| Display    | Display Module (Optional)          | 1        | niceview_headers       | Generic / Nice Technologies | SSD1306 128x32 / nice!view |
| ROL1, ROL2 | Roller Encoder (Optional)          | 2        | EVQWGD001              | Panasonic                   | EVQWGD001                  |
| ROT1, ROT2 | Rotary Encoder (Optional)          | 2        | EC11                   | Generic                     | EC11                       |
| S1-S10     | Low Profile Switches               | 10       | Kailh Choc v1 (PG1350) | Kailh                       | PG1350                     |
| S11-S12    | Low Profile Switches (Optional)    | 2        | Kailh Choc v1 (PG1350) | Kailh                       | PG1350                     |
| S13        | Reset Button                       | 1        | 6x6mm Tactile Switch   | Generic                     | SW_Push_1P1T               |
| SW15       | Power Switch (Slide)               | 1        | DPDT Angled            | Generic                     | JS202011AQN                |

## Notes

- **Display**: The OLED (SSD1306 128x32) and Memory Display (Nice!View) are both optional and mutually exclusive
  alternatives. Choose one based on your microcontroller: the OLED is typically used with Pro Micro, while the Nice!View
  is designed for nice!nano.
- **Encoders**: The EC11 rotary encoders and EVQWGD001 roller encoders are optional and mutually exclusive
  alternatives. If neither type of encoder is installed, it is recommended to use 2 additional Kailh Choc switches
  (S11 and S12) instead.
- **Switches**: S11 and S12 can be either the integrated push-buttons of the encoders or two standard Kailh Choc
  switches if no encoders are used.
- **Microcontroller**: For wired use, use a Pro Micro (USB-C recommended). For wireless use, use a nice!nano.
- **Diodes**: Any 1N4148 diode will work. Diodes can be SMD (SOD-123 package) or through-hole.
