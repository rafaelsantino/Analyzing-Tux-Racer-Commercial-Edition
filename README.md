# Note:

1.0.002 and 1.0.004 (proof of existence: mentioned on the tux racer original forums, although needs to be checked) werent found yet so this could be incomplete and have errors

# Analyzing Tux-Racer (Commercial Edition)
i just wanted to analyze tux racer commercial edition for fun

anyways

heres some things i found:

the directory of the tux racer source code is "E:\users\jfpatry\tuxracer\tuxracer-msvc\tuxracer-cvs\src\", found in the windows build of tux racer 1.1

some minimal source code of tux racer 1.1: 

![Screenshot](https://raw.githubusercontent.com/spielerkapitan/Analyzing-Tux-Racer-1.1/refs/heads/main/The%20Secret%20Uncovered.png)

after "Expression:" thats the minimal source code

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

its from 3DS Max texture library. (but i couldnt find that texture library for some reason)


# Unused Content

in the folder courses in older versions than 1.1, you can find a cup called "antarctic"

the courses are still there, but these dont have any items.tcl, which i guess they originally had one.

and also theres objects with their respective .obj.strip!

based on the objects.tcl of the cup, it seems like the courses originally had a lot of objects.

screenshot of what the trophy looks:
![Screenshot](https://github.com/spielerkapitan/Analyzing-Tux-Racer-Commercial-Edition/blob/main/antartic%20cup%20trophy.png?raw=true)

# EULA.txt in different versions of Tux Racer

in 1.0.001 and 1.0.003 there was a different EULA.txt version.

by reading it you can find out that there could be an level editor included "The Program may also contain a Level Editor (the “Editor”) that allows you to create custom levels or other materials for your personal use in connection with the Program (“New Materials”)." so maybe the image called pallete.png is a part of the editor. (no it isnt after all...)

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

# Software used in development

Sound Forge 4.5 - Audio

Maya 4.0 - Character Animations

Adobe ImageReady - Some Textures


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

# Arcade Edition

in april 2 2026, tux racer arcade got archived, so i will analyze it too.

it seems to include the course editor, which i got to run on wish tcl interpreter:

![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/tux%20racer%20editor%20working%20on%20wish%20yay.png)
(image is small cause i couldnt get anything else working, need to get tk and tix loaded correctly on tux racer to get further)

also it includes the .sh files to compile the source code

checking leftover config files it is possible to say that the directory where the source code of tux racer arcade edition is "/home/jasbahr/Projects/roxor-tuxracer/"

in the beginner cup folder a bunnyhill.zip file can be found, inside of it there seems to be an early version of beginner1 course (early because theres a trees.png file which is not used on tux racer 1.1 and there arent ticket-related objects in the items.tcl)

beginner1-v2 and beginner1-orig seems to be a duplicate of whats inside bunnyhill.zip

there are also Thumbs.db files in specific folders (apparently this reveals roxor games employees used windows xp), they dont have anything special (like deleted images) but they have different modification dates

in courses folder there is a course_idx.demo.tcl, it is very similar to the course_idx.tcl from tux racer demo but instead of having artic cup courses it would have mountain cup courses

there are also unused fish types (their textures never get loaded):

![Screenshot](https://raw.githubusercontent.com/rafaelsantino/Analyzing-Tux-Racer-Commercial-Edition/refs/heads/main/unused%20fish%20in%20tux%20racer%20arcade%20edition.png)
