# pixart-sensor-adapter

![Picture of an assembled board](https://github.com/eatnooM/pixart-sensor-adapter/assets/1300835/cdcc46df-1f16-41a8-90ac-a6b3eefab124)

License: CC BY-NC 4.0

Allows interfacing with a Wiimote camera over I2C for GUN4IR.

Variants are present to allow use of the module either socketed as you'd find it on the Wiimote, or unsocketed for more compact installs.

I've only done minimal testing on this at the moment, so run this off at your own risk.

## Inline board

The inline board should be ordered in 0.8mm thickness, otherwise you won't be able to solder to the pads on the camera!

It's a pain to solder the camera module directly to the board, so I'd strongly recommend running off [the camera module jig](inline/Wii-IR-camera-solder-guideGun4IR-v7.stl) graciously provided by Gzus348.

## Ordering

Either download the gerbers from [the latest release](https://github.com/eatnooM/pixart-sensor-adapter/releases/latest) or run off directly from OSHPark ([Inline](https://oshpark.com/shared_projects/EPIfHW2C) / [Socketed](https://oshpark.com/shared_projects/FovxzPdv)). See below for the Bill of Materials - these can be purchased from your preferred electronic component distributor but I've provided LCSC links I used for convenience.

## BOM

| Reference | Value | Link |
|-----------|-------|------|
| C1 | 0.1uF | https://www.lcsc.com/product-detail/_YAGEO-_C14663.html |
| C2, C3 | 1uF | https://www.lcsc.com/product-detail/_YAGEO-_C519560.html |
| R1, R2 | 2.7KΩ | https://www.lcsc.com/product-detail/_YAGEO-_C114612.html |
| R3 | 330KΩ | https://www.lcsc.com/product-detail/_YAGEO-_C114618.html |
| U1 | Wiimote camera module – salvaged from official wiimote | Salvage |
| U2 | AP2112-3.3V | https://www.lcsc.com/product-detail/_Diodes-Incorporated-_C51118.html |
| X1 | SG3225CAN 24.0000M-TJGA3 | https://www.lcsc.com/product-detail/_Seiko-Epson-_C32528.html |

## Credits

[JayBee](https://www.gun4ir.com/) - creator of Gun4IR - sharing the schematic

Gzus348 - creating the camera jig
