**Enhanced Super Mario Bros.**, a ROM hack by Dintonen Inc. (not associated with Nintendo Co., Ltd.)

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

*and more...*

# How to compile
## Step 0
Download the repo or clone it with `git`. This is self-explanatory.
## Step 1
Download CC65.
### Linux/WSL
Click [here](https://github.com/cc65/cc65/releases/latest) or `git clone https://github.com/cc65/cc65.git` and download the source code.  
Follow the instructions in the README to compile CC65.

### Windows
Download the latest Windows snapshot [here](https://sourceforge.net/projects/cc65/files/cc65-snapshot-win32.zip). Extract the executables `ca65.exe` and `ld65.exe` from within the `bin` folder. Copy them to the root of the repo folder.

## Step 2
Execute these two commands in a terminal:
```
ca65 -t nes enhanced-smb1.asm -o enhanced-smb1.o
ld65 -C nrom.cfg -o enhanced-smb1.nes enhanced-smb1.o
```
If no errors happen, a file named `enhanced-smb1.nes` will be created. You can use [Lunar IPS](https://www.romhacking.net/utilities/240/) (Windows) or the [Linux IPS Tool](https://github.com/kylon/Lipx) (Linux/WSL) along with a clean SMB1 ROM to create an IPS file.

# Credits
Thanks to MrWint and doppelganger for providing the disassembly of Super Mario Bros. If not, this project would not have been possible.

CHR extracted with [NesExtract](https://github.com/X-death25/Nes-Extract) and edited with [Tile Layer Pro](https://www.romhacking.net/utilities/108/) (graphics) and [SMB Title Editor](https://www.romhacking.net/utilities/1513/) (title screen)

Sources:  
[MrWint's modified SMB1 disassembly (+ PAL version)](https://github.com/MrWint/smb-dis)  
[doppelganger's original SMB1 disassembly](https://gist.github.com/1wErt3r/4048722)
