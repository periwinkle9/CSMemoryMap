# Cave Story memory addresses

These files aim to provide a comprehensive listing of hopefully every relevant
memory address in Cave Story that anybody will ever need.
It's still in a bit of a raw state right now, so any contributions in the form
of corrections, new information, better documentation, cleaner
presentation/better searchability, etc. would be much appreciated!

There are two main goals of this project:
1. To provide a better understanding of the memory that is accessible via OOB
   flags and other OOB memory tricks;
2. To provide a stepping stone for creating a better framework (or at least a
   better guide) for creating DLL mods.

More information about each file in this repo is given below.

## Static/Global Variable List

This file lists pretty much every interesting variable found in the `.data`
segment of the game's memory. This covers the memory addresses from 0x48F000
to 0x4BE048. Most variables related to the game state are located here (thank
Pixel for declaring most of his variables as global).

The data types are taken from CSE2 and/or debugging information found in the
64-bit Linux port, but any data structures outside of C++ fundamental data
types and Windows API names (which you can find documented on MSDN) are
expanded to describe their layout, so prior knowledge or access to CSE2 files
is not necessary and not assumed.

Additionally, I have tried to stay clear of giving specific variable or struct
member names from CSE2, although this may or may not change in the future for
easier reference by those who do have the CSE2 files.
(Note, some undocumented variables still remain which currently list their CSE2
names as placeholders; help with properly documenting these variables would be
appreciated.)

## Function Address List

For now, this is simply a direct copy of the `/devilution/comparer-config.toml`
file from the CSE2-accurate branch.
Much of this is already documented elsewhere, but not a lot of people know that
this exists so that's why I've copied it here.

In the future, this file may be fleshed out to include parameter lists and
return types, or possibly even be replaced with a C/C++ header file that can
be `#include`d for use in DLL mods.
