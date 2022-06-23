**Enhanced Super Mario Bros.**, a ROM hack by Dintonen Inc. (not associated with Nintendo Co., Ltd.)

v1.0.0 is now released, and now I'm uploading it to [RHDN](https://romhacking.net/) again. I hope the mods will accept it, as now it's not a beta anymore.

![Title Screen](https://raw.githubusercontent.com/gamingwithevets/enhanced-smb1/main/img0.png)
![World 1-2](https://raw.githubusercontent.com/gamingwithevets/enhanced-smb1/main/img1.png)
![World 1-3](https://raw.githubusercontent.com/gamingwithevets/enhanced-smb1/main/img2.png)
![Ending](https://raw.githubusercontent.com/gamingwithevets/enhanced-smb1/main/img3.png)

# Features
- SMB2J graphics
- European (PAL) version bug fixes and changes (except for changes made to compensate FPS difference)
- More bug fixes:
- - Minus World bugfix + scroll unlocker fix by Mike Schiraldi, covered by [Displaced Gamers](https://www.youtube.com/watch?v=61m5MiyC17s) (read more on the [Super Mario Wiki](https://www.mariowiki.com/Minus_World)) (you don't go to Minus World anymore)
- - Wrong warp bugfix in 4-2 and 8-4 (read more on the [Super Mario Wiki](https://www.mariowiki.com/List_of_Super_Mario_Bros._glitches#Wrong_Warp)) (sorry speedrunners)
- - Spiny Egg behavior bugfix (read more on [The Cutting Room Floor](https://tcrf.net/Super_Mario_Bros.#Unused_Spiny_Egg_Behavior)) (TASes will lose to these Spiny Eggs)
- Mushroom jump bugfix (read more on the [Super Mario Wiki](https://www.mariowiki.com/List_of_Super_Mario_Bros._glitches#Mushroom_Jump))
## Not fixed bugs
- Piranha Plant disappearing in the first section of 8-4 ([video of Bismuth explaining the bug](https://youtu.be/U7RzoIEoSMY?t=1316))
- Small Fire Mario
- ~~Missing "0" in high score (accidental bug when modifying title screen)~~ Fixed in v1.0.0

*and more...*

# Download
You can download the latest version of the ROM hack [here](https://github.com/gamingwithevets/enhanced-smb1/releases/latest/download/enhanced-smb1.zip).  
Use [Lunar IPS](https://www.romhacking.net/utilities/240/) (Windows) or the [Linux IPS Tool](https://github.com/kylon/Lipx) (Python) along with a clean, NTSC Super Mario Bros. ROM to apply the hack.
# How to compile
NOTE: You should really use the IPS file above instead of building the ROM from scratch. If you're willing to do this, good luck...
## Step 0
Download the repo or clone it with `git`. This is self-explanatory.
## Step 1
Download CC65.
### Linux/WSL
Click [here](https://github.com/cc65/cc65/releases/latest) or `git clone https://github.com/cc65/cc65.git` and download the source code.  
Follow the instructions in the README to compile CC65. (note: I have not compiled CC65 myself because I use Windows, okay)

### Windows
Download the latest Windows snapshot [here](https://sourceforge.net/projects/cc65/files/cc65-snapshot-win32.zip). Extract the executables `ca65.exe` and `ld65.exe` from within the `bin` folder. Copy them to the root of the repo folder.

## Step 2
Open a terminal and run these commands in the root of the repo folder:
```
ca65 -t nes enhanced-smb1.asm -o enhanced-smb1.o
ld65 -C nrom.cfg -o enhanced-smb1.nes enhanced-smb1.o
```
If no errors happen, a file named `enhanced-smb1.nes` will be created. You can use [Lunar IPS](https://www.romhacking.net/utilities/240/) (Windows) or the [Linux IPS Tool](https://github.com/kylon/Lipx) (Python) along with an NTSC SMB1 ROM to create an IPS file.

# Credits
Thanks to MrWint and doppelganger for providing the disassembly of Super Mario Bros. If not, this project would not have been possible.

CHR extracted with NesExtract and edited with Tile Layer Pro (graphics) and SMB Title Editor (title screen)

## Sources
[MrWint's modified SMB1 disassembly (+ PAL version)](https://github.com/MrWint/smb-dis)  
[doppelganger's original SMB1 disassembly](https://gist.github.com/1wErt3r/4048722)  
[NesExtract](https://github.com/X-death25/Nes-Extract)  
[Tile Layer Pro](https://www.romhacking.net/utilities/108/)  
[SMB Title Editor (English)](https://www.romhacking.net/utilities/1513/)
