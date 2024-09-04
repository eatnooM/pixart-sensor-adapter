# pixart-sensor-adapter

![Picture of an assembled board](https://github.com/eatnooM/pixart-sensor-adapter/assets/1300835/742e38c2-cac4-4380-a321-d081cb5f061d)

License: CC BY-NC 4.0

Allows interfacing with a Wiimote camera over I2C for GUN4IR.

Variants are present to allow use of the module either socketed as you'd find it on the Wiimote, or unsocketed for more compact installs.

I've only done minimal testing on this at the moment, so run this off at your own risk.

## Inline board

The inline board should be ordered in 0.8mm thickness, otherwise you won't be able to solder to the pads on the camera!
If ordering from OSHPark, I'd recommend the panelised version as they tend to put panel tabs on the edge connectors which can make for annoying cleanup before the boards are usable.

It's a pain to solder the camera module directly to the board, so I'd strongly recommend running off [the camera module jig](inline/Wii-IR-camera-solder-guideGun4IR-v7.stl) graciously provided by Gzus348.

## Ordering

Either download the gerbers from [the latest release](https://github.com/eatnooM/pixart-sensor-adapter/releases/latest) or run off directly from OSHPark ([Inline](https://oshpark.com/shared_projects/kioBCUHh) / [Socketed](https://oshpark.com/shared_projects/FovxzPdv).
See below for the Bill of Materials - these can be purchased from your preferred electronic component distributor but I've provided LCSC and Mouser links for convenience.

## BOM

| Reference | Value | Link |
|-----------|-------|------|
| C1 | 0.1uF | [LCSC - YAGEO CC0603KRX7R9BB104](https://www.lcsc.com/product-detail/_YAGEO-_C14663.html) / [Mouser - KYOCERA 06035C104KAT4A](https://www.mouser.com/ProductDetail/KYOCERA-AVX/06035C104KAT4A?qs=wQ3bP3iXTzYfFzAFm7vUeQ%3D%3D) |
| C2, C3 | 1uF | [LCSC - YAGEO CC0603JRX7R7BB105](https://www.lcsc.com/product-detail/_YAGEO-_C519560.html) / [Mouser - KYOCERA 06035C105KAT2A](https://www.mouser.com/ProductDetail/KYOCERA-AVX/06035C105KAT2A?qs=%252BdQmOuGyFcGCdIIWh6fU7Q%3D%3D)|
| R1, R2 | 2.7KΩ | [LCSC - YAGEO RC0603FR-072K7L](https://www.lcsc.com/product-detail/_YAGEO-_C114612.html) / [Mouser - Panasonic ERJ-3GEYJ272V](https://www.mouser.com/ProductDetail/Panasonic/ERJ-3GEYJ272V?qs=sGAEpiMZZMvdGkrng054tw5%2FFYq5P%2FDo1QNxauZrLUw%3D) |
| R3 | 33KΩ | [LCSC - YAGEO RC0603FR-0733KL](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_YAGEO-RC0603FR-0733KL_C126359.html) / [Mouser - Panasonic ERJ-3GEYJ333V](https://www.mouser.com/ProductDetail/Panasonic/ERJ-3GEYJ333V?qs=JjxTDIFmKPQB8Hd2hIsG7w%3D%3D) |
| U1 | Wiimote camera module – salvaged from official wiimote | Salvaged |
| U2 | AP2112-3.3V | [LCSC](https://www.lcsc.com/product-detail/_Diodes-Incorporated-_C51118.html) / [Mouser](https://www.mouser.com/productdetail/Diodes-Incorporated/AP2112K-3.3TRG1?qs=x6A8l6qLYDDPYHosCdzh%2FA%3D%3D) |
| X1 | 24-25MHz SMD3225 active crystal oscillator | [LCSC - YXC OT2EL4C4JI-111OLP-24M](https://www.lcsc.com/product-detail/Oscillators_YXC-OT2EL4C4JI-111OLP-24M_C5203548.html) / [Mouser - KYOCERA KC3225K24.0000C1GE00](https://www.mouser.com/ProductDetail/KYOCERA-AVX/KC3225K24.0000C1GE00?qs=rfsXwfL%252BOM9DBu9I0fBoew%3D%3D) |

## Credits

[JayBee](https://www.gun4ir.com/) - creator of Gun4IR - sharing the schematic

Gzus348 - creating the camera jig
