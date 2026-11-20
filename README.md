## Contents
- The document (PDF), licensed CC BY-NC-ND 4.0
- Firmware source code (.txt) for the ATtiny10 (digital circuit)
- Precompiled .HEX files
- .STL files for 3D printing
- Gerber files for PCB ordering (planned)
- Files for home PCB etching (planned)

## HEX files
M19B is the digital circuit powered through a DC-DC converter, M19C is the digital circuit powered through a linear voltage regulator.

| File | Supply | Low-voltage cut-off |
|---|---|---|
| `M19B.hex` | DC-DC converter, input about 0.8-4.5 V (starts from about 0.65 V) | about 0.7 V |
| `M19B_18650.hex` | DC-DC converter, single 18650 Li-ion cell | about 3.1 V |
| `M19C_78L05.hex` | older linear regulator (78L05), 9 V battery | about 7 V |
| `M19C_9V_11V.hex` | linear regulator: with a modern LDO, a 9 V battery or an 11 V LiPo (3S); with an older 78L05-type regulator, an 11 V LiPo only | about 6.1 V (9 V battery) / about 9.3 V (LiPo, 3.1 V per cell) |

For a 9 V battery with an older 78L05-type regulator, use `M19C_78L05.hex` instead.

## Warning
High voltage (about 19 kV) can cause injury. This is not a guide. The firmware, gerber files (planned), files for home PCB etching (planned) and the .STL files are shared as is, without any warranty; incorrect settings can damage image converter tubes or other equipment. See the document for the full terms of use.
