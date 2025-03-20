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
  - I recommend invoking MAME from the command line, as doing so:
    1) allows you to explicitly set MAME's working directory
	2) allows for relatively rapid invocation with all appropriate options selected
	3) requires zero to minimal faffing with .ini files
	Remember that, by default, MAME looks for rom files in `.\roms` under Windows, and `~/mame/roms` under Linux.  You can also use the `-rompath` command-line option to set where MAME looks for its roms.
  - Invoke MAME from the command line using:
    - for a CoCo 1 or CoCo 2: `mame coco -ext fdc,bios=hdbk12`
	- for a CoCo 3: `mame coco -ext fdc,bios=hdbk3`
	- Optionally, you can add these switches:
	  - `-window`: causes MAME to not be full-screen (this is my personal preference)
	  - `-resolution0 <wd>x<ht>`: sets the size of the MAME primary screen device (definitely handy for windowed mode)
	  - `-nomouse`: disables MAME's automatic mouse capture behavior (and relieves a *lot* of headaches)
	  - `-skip_gameinfo`: bypasses the game information splash and goes directly to machine boot
	  - `-debug`: activates the MAME debugger.  The machine comes up in the halted state.  <kdb>F5</kbd> in the debugger window starts the machine running.
  - If the emulator hangs, you'll need to activate the Becker port in the Machine Settings menu and restart MAME:
    1) Either <kbd>Scroll Lock</kbd> (Windows, I think) or <kbd>Insert</kbd> (Linux, I think) should toggle UI active status
	2) With UI active, <kbd>tab</kbd> activates the menu.
	3) Select “Machine Configuration” (should be the second menu entry, simple <kbd>↓<kbd><kbd>Enter</kbd> should do the trick)
	4) Toggle the becker port (should be the first entry, <kbd>Enter</kbd> will do here)
	5) <kdb>↑</kbd><kbd>Enter</kbd> to return to the main UI menu
	6) <kdb>↑</kbd><kdb>↑</kbd><kbd>Enter</kbd> to close the UI menu and save the settings
	7) <kbd>esc</kbd> to close the emulator
	8) re-invoke the emulator using the same command line (In case you didn't know: <kdb>↑</kbd> at the command line brings back the last command you entered, so you can use that here for expediency)
- If you're using XRoar:
  - I recommend invoking XRoar from the command line for much the same reason I do MAME.
  - Invoke XRoar from the command line using:
    - `xroar -machine cocous -cart-rom hdbdw3bck.rom -becker` for CoCo 1/2
	- `xroar -machine cocous -cart-rom hdbdw3bc3.rom -becker` for CoCo 3.
  - XRoar does not require activation of the becker port within its UI.  It should just work.
- If `CONFIG` doesn't autoload, restart FujiNet-PC and restart your emulator.
