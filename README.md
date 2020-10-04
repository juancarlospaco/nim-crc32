# CRC32

CRC32 for Nim, 2 proc, based from RosettaCode.
Its just a `proc` so no much to document about it, just pass the thingy you want to do CRC.

- Works with `--gc:arc`, `--gc:orc`, `--panics:on`, `--experimental:strictFuncs`, C, C++, JavaScript.
- Uses `system.nim` only, does not import anything from stdlib.


# Use

```nim
assert $crc32("The quick brown fox jumps over the lazy dog.") == "519025E9"
```


# Install

```
nimble install crc32
```


# Requisites

- [Nim](https://nim-lang.org)
