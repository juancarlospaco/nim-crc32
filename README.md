# CRC32

CRC32 for Nim, 2 proc.
Its just a `proc` so no much to document about it, just pass the thingy you want to do CRC.

- Works with `--gc:arc`, `--gc:orc`, `--panics:on`, `--experimental:strictFuncs`, C, C++, JavaScript.
- Uses `system.nim` only, does not import anything from stdlib.
- Works in-place, can out-place using `sugar.dup`.


# Use

```nim
var s = "The quick brown fox jumps over the lazy dog."
crc32(s)
assert s == "519025E9"
```


# Install

```
nimble install crc32
```
