# 8HP Eurorack Proto Panel

<img width="477" height="1108" alt="image" src="https://github.com/user-attachments/assets/f9c21425-a5b6-41d5-a017-22d7d7b2136f" />

An open-hardware, all-in-one 8HP Eurorack front-panel PCB designed for
solderless breadboard synth prototyping. Front-panel controls (pots, jacks,
switch, button, and LEDs) mount directly to the front of the PCB and break out
to labeled 2.54 mm (0.1 in) female headers on the back for quick jumper-wire
connections to a BusBoard BB400 breadboard.

Designed as the companion panel to the
[BB400 Eurorack Power Breakout](https://github.com/wchrapcynski/bb400-euro-power).

## Status

**v0.1** - Initial PCB revision complete (ERC and DRC clean). Awaiting physical
fabrication and hardware verification.

## Features

- **Standard 8HP Eurorack size:** 40.3 x 128.5 mm with Doepfer A-100 mounting
  holes (`H1`-`H4`)
- **All-in-one PCB faceplate:** No separate aluminum panel required
- **All through-hole (THT) assembly:** Beginner-friendly hand soldering
- **Clean 2-layer layout:** All signal routing on `F.Cu` with an unbroken `GND`
  ground plane on `B.Cu`
- **Labeled rear breakout headers:** `J5`, `J6`, and `J7` clearly marked on the
  back silkscreen so you can patch to a breadboard without checking the
  schematic
- **Breadboard sled mounts:** Two centered M3 holes (`H5`, `H6`) for bolting a
  perpendicular 3D-printed BB400 breadboard sled behind the panel

## Front Panel Controls

- 3x 100kB vertical 9 mm trimmer potentiometers (`RV1`-`RV3`)
- 4x 3.5 mm mono jacks (`J1`-`J4`, Thonkiconn / PJ398SM)
- 1x SPDT slide switch (`SW1`)
- 1x 6 mm momentary tactile push button (`SW2`)
- 2x 3 mm indicator LEDs (`D1`, `D2`) with built-in 2.2k current-limiting
  resistors (`R1`, `R2`) on the back

## Rear Header Pinout (`B.Cu`)

All breakout headers are 2.54 mm pitch vertical female sockets mounted on the
back of the board.

### `J5` (1x9 - Potentiometers)

| Pin | Net  | Description          |
|-----|------|----------------------|
| 1   | P1_1 | RV1 pin 1            |
| 2   | P1_W | RV1 wiper (pin 2)    |
| 3   | P1_3 | RV1 pin 3            |
| 4   | P2_1 | RV2 pin 1            |
| 5   | P2_W | RV2 wiper (pin 2)    |
| 6   | P2_3 | RV2 pin 3            |
| 7   | P3_1 | RV3 pin 1            |
| 8   | P3_W | RV3 wiper (pin 2)    |
| 9   | P3_3 | RV3 pin 3            |

### `J6` (1x7 - Switch, Button, LEDs)

| Pin | Net     | Description                            |
|-----|---------|----------------------------------------|
| 1   | SW1_A   | SPDT switch throw A                    |
| 2   | SW1_C   | SPDT switch common                     |
| 3   | SW1_B   | SPDT switch throw B                    |
| 4   | BTN_1   | Tactile button side 1                  |
| 5   | BTN_2   | Tactile button side 2                  |
| 6   | LED1_IN | LED D1 input (via 2.2k R1 to D1 -> GND)|
| 7   | LED2_IN | LED D2 input (via 2.2k R2 to D2 -> GND)|

### `J7` (1x6 - Jacks and Ground)

| Pin | Net    | Description      |
|-----|--------|------------------|
| 1   | J1_TIP | Jack J1 tip      |
| 2   | J2_TIP | Jack J2 tip      |
| 3   | J3_TIP | Jack J3 tip      |
| 4   | J4_TIP | Jack J4 tip      |
| 5   | GND    | Ground reference |
| 6   | GND    | Ground reference |

## Bill of Materials (BOM)

[Interactive BOM](https://wchrapcynski.github.io/universal-eurorack-proto-panel/bom/ibom.html)

| Ref     | Qty | Value / Part          | Footprint / Notes                                              |
|---------|-----|-----------------------|----------------------------------------------------------------|
| RV1-RV3 | 3   | 100kB                 | 9 mm vertical tall trimmer pot (Bourns PTV09A-1 compatible)    |
| J1-J4   | 4   | 3.5 mm mono jack      | QingPu WQP-PJ398SM (Thonkiconn), vertical                      |
| SW1     | 1   | SPDT slide switch     | C&K OS102011MS2Q (2.0 mm pin pitch, straight THT)              |
| SW2     | 1   | Tactile push button   | 6 x 6 mm standard 4-pin THT push button                        |
| D1, D2  | 2   | 3 mm LED              | Standard 3 mm THT LED (any color)                              |
| R1, R2  | 2   | 2.2k                  | 1/4W axial resistor, 7.62 mm pitch (mounted on back)           |
| J5      | 1   | 1x9 female header     | 2.54 mm vertical pin socket (mounted on back)                  |
| J6      | 1   | 1x7 female header     | 2.54 mm vertical pin socket (mounted on back)                  |
| J7      | 1   | 1x6 female header     | 2.54 mm vertical pin socket (mounted on back)                  |

## Fabrication

- Designed in **KiCad 10**
- 2-layer PCB, 1.6 mm FR-4, 1 oz copper
- Dimensions: 40.3 x 128.5 mm (8HP)
- Can be ordered directly from OSH Park by uploading the `.kicad_pcb` file, or
  fabricated anywhere using standard Gerber + drill exports

## License

Copyright (c) 2026 William Chrapcynski

This hardware design is licensed under the Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International License
(**CC BY-NC-SA 4.0**). See https://creativecommons.org/licenses/by-nc-sa/4.0/
for details.
