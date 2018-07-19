# Tanuki 40% keyboard
### Materials and Assembly

These are not instructions. Keep in mind that you can change anything you like if you think it will work!

#### Part list pcb
|quantity  | description |
|----------|-------------|
| x42 | diode smd: SOD-123 / SOD-80 (1N4148W / LL4148) or diode tht: DO-35 (1N4148 or similar) |
| x42 | MX style switches |
| x1 | resistor: 0603 500ohm |
| x1 | usb port: molex 54819-0519 |
| x1 | controller: arduino pro micro + headers |
| x5 | underglow led: WS2812B, this can also be a neopixel strip with 5 leds. |
| x1 | reset button: 3x6x2.5mm push button |
| x2 | stabilizer: costar style 2 unit (optional)|
| x1 | usb pigtail: cheap generic microusb cable to cut |

#### Part list case
|quantity  | description |
|----------|-------------|
| x6 | 3M hexagonal nut. 2.4mm height. |
| x6 | 3M bolt. either 16 or 18 mm depending on the thickness of the board. |

#### Keycaps
I recommend using a DSA profile keycap but you can do anything you like. Freestyle man!

|quantity  | description |
|----------|-------------|
| x34 | 1U keycap |
| x2 | 2U keycap |
| x5 | 1.25U keycap |
| x1 | 1.5U keycap |


#### Case parts preparation before assembly

If you want you can paint the upper parts of the keyboard so the underglow only shines through the bottom plate. When picking your spray-paint make sure that the propellant doesn't eat away at the plastic. Some of the propellants can be corrosive.

![paint](https://github.com/SethSenpai/Tanuki/blob/master/Img/assemble2.jpg?raw=true)

The engraving on the front of the plate can be painted after by hand or filled by paint and then scraped off and cleaned off later with some isopropanol.

![paint](https://github.com/SethSenpai/Tanuki/blob/master/Img/assemble1.jpg?raw=true)

If you want you can countersink the holes in top of the plate so the screws will fit on nice and flush later on.

The backplate can be sanded to increase the diffusion of the underglow through the side of the backplate. This makes the glow effect more spread and less like a flashlight.
In order to fit the backplate to the rest of the keyboard you should install some 3mm nuts in the slots on the backplate. You can glue them in place using superglue or epoxy.

![sanding](https://github.com/SethSenpai/Tanuki/blob/master/Img/assemble3.jpg?raw=true)

When you're done it should look something like this: (except it won't be assembled yet)

![assembled](https://github.com/SethSenpai/Tanuki/blob/master/Img/assemble4.jpg?raw=true)


#### Hand wiring

If you decide to handwire a Tanuki just make sure to change the files correctly. If you're lost you can check out the [QMK hand wiring guide](https://docs.qmk.fm/#/hand_wire). The matrix is displayed below.

![matrix](https://github.com/SethSenpai/Tanuki/blob/master/Img/matrix.png?raw=true)


#### PCB assembly

First part to solder to your pcb is the reset switch (if you have one) and the resistor for the led data line. ([this is not needed but **highly** recommended,](https://electronics.stackexchange.com/questions/102050/what-is-the-purpose-of-adding-a-300-ohm-to-500-ohm-resistor-on-the-ws2812b-neopi) in that case just bridge the pads).

![ass1](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba1.jpg?raw=true)

The next step is to put all the diodes on the pcb. Make sure that the cathode (generally indicated by a mark on the diode) is pointing towards the square pad on the pcb.
If you're using through hole diodes it might be a good idea to put some diodes on the other side of the pcb. This makes sure that there is a nice spacer between the plate and the pcb and keeps the switches in place nicely.

![ass2](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba2.jpg?raw=true)

Following this it is time to mount the leds on the pcb. When using the smd WS2812B leds make sure that the indent on one of the corners (the red circle in the picture) is pointing to the bottom right of the pcb.
Also keep in mind that the WS2812B leds are pretty heat sensitive so don't cook them!
If you want to hook up a neopixel strip just attach the wires to the appropriate breakout left of the first led.

![ass3](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba3.jpg?raw=true)

Solder the usb chassis to the board. Make sure it is nice and straight.

![ass4](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba4.jpg?raw=true)

Next are the headers for the pro micro. If you want to make the board slightly less thick you can remove the black standoffs in the header and just solder in the pins themselves. With a bit of dielectric tape on the back of the pro micro this can save you 2 to 3mm of height.

![ass5](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba5.jpg?raw=true)

The next steps are to put the switches into the front plate and solder them to the board. I always mount the 4 corner switches first and then solder in the rest of the switches.
After this solder in the cut up micro usb cable to the breakout points on the board. It is generally helpful to remove the entire rubber outer layer of the cable to make it easier to solder and save on height space.

![ass7](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba7.jpg?raw=true)

The last step is to solder in the pro micro. Make sure the tx0 port on the pro micro aligns with the indicator on the pcb. Plug in the micro usb chassis into the pro micro and the final assembled product looks something like this. Time to upload the [firmware](https://github.com/SethSenpai/Tanuki/tree/master/Firmware) and try it out.

![ass6](https://github.com/SethSenpai/Tanuki/blob/master/Img/pcba6.jpg?raw=true)

