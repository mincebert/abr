ABR Utility
===========

This utility allows the locking and unlocking of an ABR (Advanced
Battery-Backed RAM) cartridge from Retro Hardware for the Acorn Electron or
BBC Master.

There are utilities to manage this built into the Plus 1 Support ROM
(https://mdfs.net/Software/BBC/SROM/Plus1/) but this is useful when that's not
available (such as on a BBC Master).


Versions
--------

`ABRE` is the version for the Electron.  `ABRM` is for the Master.

Typically you pick the version for your hardware and copy it somewhere (e.g.
the Library directory) and name it `ABR`.

The only difference between the versions is that the Electron one runs from
&0900 and the Master one &DD00.  The Electron one will, however, still detect
it's running on a Master and handle setting/restoring ACCCON.


Usage
-----

Syntax is available by running the program without any arguments:

  `ABR (M)U/L (<rom>)`

An optional `M` at the beginning forces BBC Master mode, which is useful when
running a non-native OS on Master hardware with a ROM switcher (as the utility
uses OSBYTE 0 to detect running on a Master).

The nexti argument must be `U` or `L` to unlock or lock the RAM.

The second argument is optional and and specify the ROM number to unlock or
lock, or can be omitted to affect all ROMs.

Note that the protocol only allows selection between all even or all odd ROMs;
any number can be entered but it will affect all the ROMs of that type.
