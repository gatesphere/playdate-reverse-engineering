Unofficial Playdate reverse-engineering notes/tools - covers file formats, server API and USB serial commands

> ⚠️ This documentation is unofficial and is not affiliated with Panic. All of the content herein was gleaned from reverse-engineering Playdate tools and game files, and as such there may be mistakes or missing information. 

## Documentation

- **File Formats**
  - **Playdate game formats**
    - [**.pdz**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pdz.md) - Executable file container
    - [**.pda**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pda.md) - Audio file
    - [**.pdi**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pdi.md) - Image file
    - [**.pdt**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pdt.md) - Imagetable file
    - [**.pdv**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pdv.md) - Video file
    - [**.pds**](https://github.com/jaames/playdate-reverse-engineering/blob/main/formats/pds.md) - Strings file
    - **.pft** - Font file (TODO)
  - **Other formats**
    - **.fnt** - Font source file (TODO)
    - **.strings** - Strings source file (TODO)
- **Server**
  - [**Playdate API**](https://github.com/jaames/playdate-reverse-engineering/blob/main/server/api.md) - Main Playdate server API
- **Misc**
  - [**USB**](https://github.com/jaames/playdate-reverse-engineering/blob/main/usb/usb.md) - Playdate USB serial interface

## Tools

- [**`pdz.py`**](https://github.com/jaames/playdate-reverse-engineering/blob/main/tools/pdz.py) - Unpacks all files from a `.pdz` file container
- [**`pdex2elf.py`**](https://github.com/jaames/playdate-reverse-engineering/blob/main/tools/pdex2elf.py) - Converts a `pdex.bin` to an ELF file that can be analysed in a decompilation tool such as Ghidra
- [**`usbeval.py`**](https://github.com/jaames/playdate-reverse-engineering/blob/main/tools/usbeval.py) - Uses the Playdate's USB `eval` command to evaluate a Lua script over USB. Has access to the Lua runtime of the currently loaded game, except for system apps.

## Special Thanks

 - [Simon](https://github.com/simontime) for helping with some ADPCM audio data reverse engineering
 - [Zhuowei](https://github.com/zhuowei) for this [script for unpacking Playdate .pdx executables](https://gist.github.com/zhuowei/666c7e6d21d842dbb8b723e96164d9c3), which was the base for `pdz.py`
 - The folks at [Panic](https://panic.com/) for making such a wonderful and fascinating handheld!

 ----

 2022 James Daniel

 Playdate is © [Panic Inc.](https://panic.com/) - this project isn't affiliated with or endorsed by them in any way.