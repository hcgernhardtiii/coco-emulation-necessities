# FujiNet-PC Executables
This repository contains TRS-80 Color Computer FujiNet-PC executables for:
- Microsoft Windows 10/11, 64-bit Intel
- Ubuntu Linux, x86-64 (should work on just about any other x86-64 Linux flavor)

Please note that, though I have tested these binaries on other machines, I can't guarantee they'll work for you.  If they fail feel free to file a bug report along with any error messages you may be receiving (a screenshot will be helpful here).

## To run FujiNet-PC:
- Copy the appropriate folder somewhere onto your machine.
- Open the new folder
- Double-click the appropriate `run-fujinet` script for your environment (this'll be either the `.bat` or `.ps1` file on a Windows box)

## To *use* FujiNet-PC:
- Make sure the ROM files are installed in the appropriate paths for your emulator of choice.
- If you're using MAME:
  - run MAME with `-ext fdc,bios=hdbk12` for CoCo 2, or `-ext fdc,bios=hdbk3` for CoCo3.
  - If the emulator hangs, you'll need to activate the Becker port in the Machine Settings menu and restart MAME.
- If you're using XRoar:
  - run XRoar with `-cart-rom hdbdw3bck.rom -becker` for CoCo 1/2, or `-cart-rom hdbdw3bc3.rom -becker` for CoCo 3.

If `CONFIG` doesn't autoload, restart FujiNet-PC and try your emulator again.