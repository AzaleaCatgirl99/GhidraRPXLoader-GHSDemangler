# Ghidra RPX/RPL loader

This is a (WIP) simple extension to open .rpx and .rpl files with Ghidra.

# Dependencies

This loader uses the Gekko/Broadway processor definitions for Ghidra if found - it is recommended that this should be installed prior to using the loader.

https://github.com/aldelaro5/ghidra-gekko-broadway-lang

The loader will fallback to the default PowerPC processor if the Gekko/Broadway language is not found, but do not expect good results if the program uses any paired single instructions.

# Usage

Install the extension using the `Install Extensions` option inside Ghidra.

Once the extension is installed, you can import a .rpx/.rpl file via `File->Import File...`.

# Building

```
cd /path/to/extension
export GHIDRA_INSTALL_DIR=/path/to/ghidra 
gradle 
```

Output goes into `dist`

# Eclipse

To be able open this module in eclipse, you need to create a new Ghidra Module and copy the `.classpath`, `.project` and `.settings` to copy of this repository.

# Credits

Based on https://github.com/Relys/rpl2elf