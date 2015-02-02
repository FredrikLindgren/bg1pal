# BG1 Platform-Abstraction Library

This is a resource-name abstraction library for the different versions
of Baldur's Gate. Supported versions are plain Baldur's Gate, Baldur's
Gate Tutu, Baldur's Gate Trilogy and Baldur's Gate: Enhanced Edition.

The BG1 Platform-Abstraction Library converts canonical resource names
into the appropriate form for the current platform via the function
fl#bg1pal, which is available both as an action and a patch
function. All resource names and resource types are supported.

Example:
```
LAF fl#bg1pal STR_VAR file = ar0125.are RET file END // Tutu: fw0125.are; BGT: ar7225.are; BG:EE: no conversion
LAF fl#bg1pal STR_VAR file = black01.wav RET file END // Tutu: _black01.wav; BGT: blackl01.wav; BG:EE: no conversion
LAF fl#bg1pal STR_VAR file = intro.mve RET file END // Tutu: _intro.mve; BGT: bgintro.mve; BG:EE: intro.wbm
```

For more extensive documentation, please refer to the file readme.html.
