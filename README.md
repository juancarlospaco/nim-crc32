# CRC32

CRC32 for Nim, 2 proc.
Its just a `proc` so no much to document about it, just pass the thingy you want to do CRC.

- Works with `--gc:arc`, `--gc:orc`, `--panics:on`, `--experimental:strictFuncs`, C, C++, JavaScript.
- Uses `system.nim` only, does not import anything from stdlib. Works in-place, can out-place using `sugar.dup`.


# Use

```nim
from std/sugar import dup  # Optional, to out-place.

var x = "The quick brown fox jumps over the lazy dog."
crc32(x)  ## In-Place.
doAssert x == "519025E9"
doAssert "The quick brown fox jumps over the lazy dog.".dup(crc32) == "519025E9"  ## Out-Place.

var e = " "
crc32(e)  ## In-Place.
doAssert e == "E96CCF45"
doAssert " ".dup(crc32) == "E96CCF45"  ## Out-Place.

var z = ""
crc32(z)   ## In-Place.
doAssert z == "00000000"
doAssert "".dup(crc32) == "00000000"  ## Out-Place.

var f = "crc32.nim"
crc32FromFile(f)  ## In-Place.
echo f
echo "crc32.nim".dup(crc32FromFile)  ## Out-Place.
```


# Install

```
nimble install crc32
```


# Stars

![](https://starchart.cc/juancarlospaco/nim-crc32.svg)
:star: [@juancarlospaco](https://github.com/juancarlospaco '2022-02-16')	
:star: [@adokitkat](https://github.com/adokitkat '2022-07-05')	
