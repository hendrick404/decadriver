# DecaDriver

Zephyr drivers for the Decawave DWM1001-dev board bundled as a library for PlatformIO.

The source code comes from [Decawave](https://github.com/Decawave) and [RTLOC](https://github.com/RT-LOC) and was taken from this specific [repository](https://github.com/foldedtoad/dwm1001).

## Prerequisites

There are two things necesary to succesfully build this library with Zephyr and PlatformIO:
- The library uses Devicetree macros that are not included in the official Zephyr board definition for the DWM1001-dev. Add the `decawave_dwm1001_dev.overlay` to your Zephyr board definition.
- Platformio does not support the DWM1001 with Zepbyr yet. I worked around this, by taking the board definition from PlatformIO, rename it to `decawave_dwm1001_dev` and adding `"zephyr"` to the `"frameworks"` entry.
  
Both files can be found in the extra directory.
