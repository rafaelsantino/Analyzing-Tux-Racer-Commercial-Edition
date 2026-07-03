# Note:

1.0.002 wasnt found yet so this could be incomplete and have errors

# Analyzing Tux-Racer (Commercial Edition)
i just wanted to analyze tux racer commercial edition for fun

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

# technical OpenGL information

by default, the game uses display lists for mostly everything, by using an opengl wrapper that doesnt support displaylists,
it reveals that it doesnt use display lists for terrain.

![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/UHM%20why%20it%20looks%20like%20that.png)

so tux racer only uses display lists to optimize .obj.strip models.

# Key Shortcuts

when pressing = the game changes the current player camera to another player camera, by doing this on Enter an Event
it lets you see the bots internal name ( example: ai_0 )

and when pressing ¿ it does screenshots, in 1.1 it makes screenshots in .bmp format, but in 1.0.001 it does in .ppm format

# internal game files names

in samuels character folder the texture file names are sammy instead of being samuel
which could mean that it was originally supposed to be sammy

same happens with neva, the texture file names are gown instead of neva.

# E3 Teaser Trailer

looking at the E3 Teaser Trailer of tux racer, is it possible to notice differences such as: 

only playable character yet was Tux, leading to other players/bots being Tux.

invididual cup lighting .tcl files didnt exist yet, instead it was using the default weather lighting .tcl files from tux racer 0.61, 
the background files used on those .tcl files is still on tux racer 1.1

rock1 texture differences:

E3 version
![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/tux%20racer%20e3%20rock%20differences.png)

Final 1.0.001 version
![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/tux%20racer%20final%20version%201.0001%20rock%20differences.png)

# Unknown (yet?) build

as seen in the manual screenshots it is noticeable that the course previews show debug info (normal debug info such as FPS and Tris) and the lighting used in the E3 version

![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/practice_select.png)
