# Analyzing Tux-Racer (Commercial Edition)
i just wanted to analyze tux racer commercial edition for fun

# Note:

1.0.002 wasnt found yet so this could be incomplete and have errors

anyways

heres some things i found:
some images were made with Software Adobe ImageReady

the directory of the tux racer source code is E:\users\jfpatry\tuxracer\tuxracer-cvs\

some leaked minimal source code of tux racer 1.1: 

![Screenshot](https://raw.githubusercontent.com/spielerkapitan/Analyzing-Tux-Racer-1.1/refs/heads/main/The%20Secret%20Uncovered.png)

after "Expression:" thats the minimal leaked source code

this also reveals why it crashes sometimes with the music enabled when you have the original sdl.dll that comes included with the game itself

i also wonder, why cant we just make somehow the c++ redistributable log the whole source code of tux racer 1.1?

# Less Technical things:

![Screenshot](https://raw.githubusercontent.com/spielerkapitan/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/palette.png)

found this pallete of terrains in versions earlier than 1.1

as you can see, theres an test terrain called "vwall"


also theres a list of objects of tux racer 0.61 ( free version )

# Texture Matching
found texture matching in IcyCobbleStone:

![Screenshot](https://github.com/spielerkapitan/Analyzing-Tux-Racer-1.1/blob/main/icycobblestone.png?raw=true)

The Original Texture:

![Screenshot](https://github.com/spielerkapitan/Analyzing-Tux-Racer-1.1/blob/main/desktop-wallpaper-3ds-max-texture-library.jpg?raw=true)

its from 3ds max texture library.


# Unused Content

in the folder courses in older versions than 1.1, you can find a cup called "antarctic"

the courses are still there, but these dont have any items.tcl, which i guess they originally had one.

and also theres objects with their respective .obj.strip!

based on the objects.tcl of the cup, it seems like the courses originally had a lot of objects.

screenshot of what the trophy looks:
![Screenshot](https://github.com/spielerkapitan/Analyzing-Tux-Racer-Commercial-Edition/blob/main/antartic%20cup%20trophy.png?raw=true)

# EULA.txt in different versions of Tux Racer

in 1.0.001 and 1.0.003 there was a different EULA.txt version.

by reading it you can find out that there could be an level editor included "The Program may also contain a Level Editor (the “Editor”) that allows you to create custom levels or other materials for your personal use in connection with the Program (“New Materials”)." so maybe the image called pallete.png is a part of the editor.

# scrapped bots paths

in 1.1 when you checked the ai-targets folder, you would find a .tcl file with a random number

but in 1.0.001 you can find scrapped ai targets which are probably failed versions

theres also a new.tcl

