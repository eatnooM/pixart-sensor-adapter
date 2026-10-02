# pixart-sensor-adapter

![Picture of an assembled board](https://github.com/user-attachments/assets/043c7a50-4f18-4311-9e13-b482321dc8dc)

License: CC BY-SA 4.0

Allows interfacing with a Wiimote camera over I2C for GUN4IR.

Variants are present to allow use of the module either socketed as you'd find it on the Wiimote, or unsocketed for more compact installs.

I've only clocked a few hours actually _using_ these, so run this off at your own risk.

## Inline board

The inline board should be ordered in 0.8mm thickness, otherwise you won't be able to solder to the pads on the camera!
If ordering from OSHPark, I'd recommend the panelised version as they tend to put panel tabs on the edge connectors which can make for annoying cleanup before the boards are usable.

It's a pain to solder the camera module directly to the board, so I'd strongly recommend using the jig from RetroMidget's shell (see below) to aid with this, or running off [the standalone camera module jig](inline/printables/Wii-IR-camera-solder-guideGun4IR-v7.stl) graciously provided by Gzus348.

### Shell

If you're using the inline board, I would strongly recommend you check out [RetroMidget's camera enclosure](https://github.com/slikvik55/Lightgun3DParts/tree/main/WiiCamEnclosure). This 3D-printable enclosure is currently verified to fit the v1.0 board (but also fit the v1.2 board as long as you omit the rear cover) and enables you to install directly (such as in a GunCon 1) by simply tightening the nuts to hold it in place in the shell, or using prints such as JayBee's Gun4IR GunCon mounts ([GunCon 1](https://www.gun4ir.com/products/copy-of-gun4ir-diy-cam-and-rumble-holder-sets), [GunCon 2](https://www.gun4ir.com/products/gc1-gun4ir-diy-cam-and-rumble-holders)) to secure the camera and a fish-eye lens for use closer to your display.

I have a project to make a shell for the newer versions of this board that make use of the slimmer profile to fit in some tighter places (such as the barrel of a Blaze Scorpion 2, which is slightly too narrow for the DFRobot Gravity camera), but sit tight for news on this.

### IR Pass Filter

To prevent the camera from picking up visible-light sources as well as the infrared from your emitters, it is recommended to add an IR pass filter in front of the camera. This cuts down on camera erroneously detecting bright lights instead of your IR points.

If salvaging from whole Wii remotes including the shell, you'll already have the IR pass filter - this is the black-coloured plastic in the front of the shell. If you got hold of a job lot of bare boards, however, you will need to purchase some filter. I've been using the filter found in [this eBay listing](https://www.ebay.co.uk/itm/397673945348) - it's nice and thin, making it easier to cut down to size and fit in a build, and 100mm x 100mm will serve for a lot of builds if you're efficient at cutting them out. If this listing isn't available for you, there are similar listings [on Aliexpress](https://www.aliexpress.com/w/wholesale-infrared-pass-filter-940nm.html). The most important aspect of the filter is that it passes 940nm wavelength your emitters (presumably) use, and ideally blocks as much of everything else as possible.

To cut the filter, I'd recommend a rotary tool. If you have particularly sharp flush cutters, these can do the job if you're careful but I've had these split the plastic in inconvenient places so it's not my first choice. You can repeatedly score the plastic with a sharp knife to get a square of roughly the right size and then file into the desired shape, but this may take a while. You'll then need to attach this in front of the camera:

- The simplest way to attach the filter is to cut a circle of the filter to the same diameter as your shell, apply a little hot glue to the front of the shell you're using and stick it in place. If it's good enough for DFRobot, it's good enough for us. If you've dabbled in phone repair before, T7000/B7000 or similar glues will also do a great job. Just be sure to keep the glue away from the part directly in front of the camera.
- If you're using [RetroMidget's shell](https://github.com/slikvik55/Lightgun3DParts/tree/main/WiiCamEnclosure), there's a smaller circular window so you can save on a little material and only cover this area up with the filter. 

If using a wide angle or fish eye lens, there are some other convenient places to stick the filter:

- The wide angle lens adapters in the printables section all have a taper that's pretty forgiving to glue the filter into as long as you can cut it into a rough circle so there aren't big gaps for unfiltered light to pass through.
- There's a lip on the inside of the lens too - you can fit a thin filter in here.


## Ordering

Either download the gerbers from [the current release](https://github.com/eatnooM/pixart-sensor-adapter/releases/latest) or run off directly from OSHPark ([Inline](https://oshpark.com/shared_projects/reO6OkLE) / [Socketed](https://oshpark.com/shared_projects/FovxzPdv).
See below for the Bill of Materials - these can be purchased from your preferred electronic component distributor but I've provided LCSC and Mouser links for convenience.

## BOM

| Reference | Value | Link |
|-----------|-------|------|
| C1 | 0.1uF | [LCSC - YAGEO CC0603KRX7R9BB104](https://www.lcsc.com/product-detail/_YAGEO-_C14663.html) / [Mouser - KYOCERA 06035C104KAT4A](https://www.mouser.com/ProductDetail/KYOCERA-AVX/06035C104KAT4A?qs=wQ3bP3iXTzYfFzAFm7vUeQ%3D%3D) |
| C2, C3 | 1uF | [LCSC - YAGEO CC0603JRX7R7BB105](https://www.lcsc.com/product-detail/_YAGEO-_C519560.html) / [Mouser - KYOCERA 06035C105KAT2A](https://www.mouser.com/ProductDetail/KYOCERA-AVX/06035C105KAT2A?qs=%252BdQmOuGyFcGCdIIWh6fU7Q%3D%3D)|
| R1, R2 | 2.7KΩ | [LCSC - YAGEO RC0603FR-072K7L](https://www.lcsc.com/product-detail/_YAGEO-_C114612.html) / [Mouser - Panasonic ERJ-3GEYJ272V](https://www.mouser.com/ProductDetail/Panasonic/ERJ-3GEYJ272V?qs=sGAEpiMZZMvdGkrng054tw5%2FFYq5P%2FDo1QNxauZrLUw%3D) |
| R3 | 33KΩ | [LCSC - VISHAY CRCW060333K0FKEA](https://www.lcsc.com/product-detail/C844778.html) / [Mouser - Panasonic ERJ-3GEYJ333V](https://www.mouser.com/ProductDetail/Panasonic/ERJ-3GEYJ333V?qs=JjxTDIFmKPQB8Hd2hIsG7w%3D%3D) |
| U1 | Wiimote camera module – salvaged from official wiimote | Salvaged |
| U2 | AP2112-3.3V | [LCSC](https://www.lcsc.com/product-detail/_Diodes-Incorporated-_C51118.html) / [Mouser](https://www.mouser.com/productdetail/Diodes-Incorporated/AP2112K-3.3TRG1?qs=x6A8l6qLYDDPYHosCdzh%2FA%3D%3D) |
| X1 | 24-25MHz SMD3225 active crystal oscillator | [LCSC - YXC OT2EL4C4JI-111OLP-24M](https://www.lcsc.com/product-detail/Oscillators_YXC-OT2EL4C4JI-111OLP-24M_C5203548.html) / [Mouser - KYOCERA KC3225K24.0000C1GE00](https://www.mouser.com/ProductDetail/KYOCERA-AVX/KC3225K24.0000C1GE00?qs=rfsXwfL%252BOM9DBu9I0fBoew%3D%3D) |

When using with OpenFIRE, the following amendments can be made:
- As VCC is already 3.3V, U2, C2, and C3 can be omitted (and JP1 should be bridged to connect VCC straight to the camera)
- OpenFIRE supports generating the 24MHz clock signal from the RP2040 directly, meaning you can wire this to the CLK and omit X1 and C1.

## Credits

[JayBee](https://www.gun4ir.com/) - creator of Gun4IR - sharing the schematic

Gzus348 - creating the camera jig

[RetroMidget](https://github.com/slikvik55) - creator of the lovely shell for the inline boards
