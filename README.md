![Banner Image](images/diagram_screenres.jpg)
# TAM Umbilical ![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
As the TAM (Twentieth Anniversary Macintosh) grows older, replacement parts for this exceptional quark grow more rare and more expensive. This includes the "bass" station, which incorporates both audio and power supply in one unit. Without the bass station you can neither hear nor use the TAM.

The goal of this document is to provide information on the TAM's umbilical cord pinout and demonstrate a practical alternative for powering up a TAM. Information on accessing your TAM's umbilical is available on [iFixit](https://www.ifixit.com/Teardown/Twentieth+Anniversary+Mac+Teardown/12702) (up to step 9).

### What is an umbilical?
The endearingly titled "umbilical" is the sole coil tethering the Twentieth Anniversary Macintosh to the "bass" station. The bass station provides both audio amplication and power over this connector. 

# J16 - Power Connectivity
<a href="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/TAM_UMBILICAL_J16_POWER.png"><img align="left" width="150" height="150" src="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/TAM_UMBILICAL_J16_POWER.png?raw=true" style="margin-right: 1em"></a>
J16 is the main attraction — and thankfully it's really not a hard act to follow. While the [technical specifications available from Apple](https://support.apple.com/kb/sp408?locale=en_US) are somewhat lacking, the table below clearly shows a standard 12V/5V 100 watt power supply (e.g., Pico PSU) will provide sufficient power.

It's important to note that the original bass unit is rated for 1000 watts. While it's not clear what the additional wattage is used for it should be established that some accessories may not work as intended without sufficient power.  

| Pin | Source | Connections |
| :-------------: | ------------- | ------------- |
| 1  | 12V  | C1(+), C19(+), C20(+), J2 (Sense) |
| 2  | 5V  | C2 |
| 3  | 5V  | C2 |
| 4  | 5V  | C2 |
| 5  | 12V  | C1(+), C19(+), C20(+), J2 (Sense) |
| 6  | GND  | C1, C19, C20, C2, C3, C4(+)* |
| 7  | GND  | C1, C19, C20, C2, C3, C4(+)* |
| 8  | GND  | C1, C19, C20, C2, C3, C4(+)* |

_* The negative connector of C4 is -12V_

# J2 - Audio Connectivity
<a href="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/TAM_UMBILICAL_J2_AUDIO.png"><img align="left" width="150" height="150" src="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/TAM_UMBILICAL_J2_AUDIO.png?raw=true" style="margin-right: 1em; margin-bottom: 1em;"></a>
The second connector on the internal side of the TAM umbilical is dedicated to audio signals. This includes the input for the bass station and the amplified output.

Without further testing, I am inclined to believe this connector can be disregarded if your goal is to provide power.
<br/><br/><br/>

| Pin | Source | Connections |
| :-------------: | ------------- | ------------- |
| 1  | 5V  | J3 Pin 7 (Sense) |
| 2  | 5V  | Trickle to J3 Pin 3, C3(+) |
| 3  | GND  | J3 Pin 4 (Sense) |
| 4  | PFW  | J3 Pin 5 |
| 5  | 12V  | J16 Pin 1,5 (Sense), C1(+), C19(+), C20(+) |
| 6  | -12V  | C4, J3 Pin 1 |
| 7  | AMP OE  | U1 |
| 8  | SPKR LHS | J15 Pin 3 |
| 9  | SPKR LHS RTRN  | R31, J15 Pin 2 |
| 10 | SPKR RHS | J1 Pin 2 |
| 11 | SPKR RHS RTRN | R31, J31 Pin 2 |
| 12 | AMP RTRN | J3 Pin 13, R25 |
| 13 | AMP LHS | J3 Pin 14 |
| 14 | AMP RHS | J3 Pin 12 |
| 15 | NA | — |
| 16 | NA | — |

_LHS, "Left Hand Side". RHS, "Right Hand Side". SPKR, "Speaker". RTRN, "Return"_

# Connector
<a href="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/connector.png"><img align="left" width="150" height="150" src="https://github.com/Stephen-Arsenault/TAM-Umbilical/blob/main/images/connector_screenres.png?raw=true" style="margin-right: 1em; margin-bottom: 1em;"></a>
The TAM's umbilical appears to use a male `Deutsch HDP26-24-23ST` style connector. This connector contains 23 pins and is grounded on the outter ring as well as with a braided sheath. Female versions of this connector are available, and at the time of writing this document I found examples as low as $20 USD.
<br/><br/><br/><br/>
| Pin | Connector | Label |
| :-------------: | ------------- | ------------- |
| 1  | J2 Pin 7 | AMP OE |
| 2  | — | — |
| 3  | J2 Pin 14 | AMP RHS |
| 4  | — | — |
| 5  | J2 Pin 10 | SPKR RHS |
| 6  | J2 Pin 9 | SPKR RTRN |
| 7  | J2 Pin 8 | SPKR LHS |
| 8  | J2 Pin 12 | AMP RTRN |
| 9  | J2 Pin 13 | AMP LHS |
| 10 | J2 Pin 4 | PFW |
| 11 | J2 Pin 6 | -12V |
| 12 | J2 Pin 2 | 5V |
| 13 | J16 Pin 2 | 5V |
| 14 | J16 Pin 6 | GND |
| 15 | J2 Pin 3 | GND |
| 16 | — | — |
| 17 | J2 Pin 1 | 5V |
| 18 | J16 Pin 3 | 5V |
| 19 | J16 Pin 7 | GND |
| 20 | GND | GND |
| 21 | J16 Pin 8 | GND |
| 22 | J16 Pin 1 | 12V |
| 23 | J2 Pin 5 | 12V |

# License ![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
All content in this repo are licensed under CC BY 4.0 ([License](LICENSE.md)) ([Creative Commons](https://creativecommons.org/licenses/by/4.0/)).

![Banner Image](images/cable.png)
