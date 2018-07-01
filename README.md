# TD-pixelMappingLEDs-2D

Pixel mapping with arbitrary 2D Geometric arrangements.
Uses a TOP texture to control colors.

This is a visualizer (with 3 approaches CHOP, SOP and GLSL) but also has the ability to send the rgb color data out to your led controller.

![screenshot](/img.png)

The SOP geometry determines the addressing for your leds.

For example this circular arrangement has 20 strips of 30 leds each.

![screenshot](/addressing.png)

There's a CHOP named LEDRGBData. This has all the rgb data sequenced in one long channel. So the first 3 samples of this, correspond to the RGB data of the led address of 0. The second 3 samples are the RGB data for the address 1, and so on.

![screenshot](/ledPixelData.png)

This CHOP data can then go directly out to your led controller.
