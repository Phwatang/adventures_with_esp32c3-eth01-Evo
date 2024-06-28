# adventures_with_esp32c3-eth01-Evo
Short journal of my experience with the esp32c3-eth01-evo and its accompanying PoE daughter board.

## Flashing
I decided to flash the base version of ESPHome using the [ESPHome web flasher](https://web.esphome.io/).

### Equipment
Equipment used during the flashing process was:
 - CH340G USB to TTL module
 - Female to female dupont wires

### Wire/Pin setup
The wire connection between the usb flasher and etho01-evo was as follows:
| CH340G USB | esp32c3-etho01-evo |
|------------|--------------------|
| 5V         | 5V                 |
| RXD        | TXD0               |
| TXD        | RXD0               |
| GND        | GND                |

Also on the eth01-evo, **IO09 and GND were jumpered together**.

## PoE
Board successfully powered up when connected to an active PoE switch.
 - Passive PoE injection has not been tested.

### Power consumption
When connected to a Ubiquiti US-8-60W switch with a 5m ethernet cable, the switch reported a power use of 0.65-0.69W (with the board running ESPHome).