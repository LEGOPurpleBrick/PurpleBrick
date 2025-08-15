# PurpleBrick
PurpleBrick aims to be the must-have speedrun practice tool for the mainline TT Games made LEGO Games.

<img width="1050" height="600" alt="Image of the current version of PurpleBrick" src="https://github.com/user-attachments/assets/9c665f70-4cbc-4fdc-84b3-5b033d0946bf" />

# Features
* Viewing and changing player coordinates.
* Loading into map files.
* A custom Door Finder which allows you to see the properties of any GizDoor.
* A toggle switch to enable the effects of the N0CUT5 code.
* A toggle switch to enable the debug Streaming Display option, which displays what maps are loaded into memory.*
* Custom hotkey system to allow for faster execution of some features.

This is an early release and the program is still actively in development, therefore not every feature is supported in every game yet, please refer to the Supported Games section of this description to avoid confusion.

*This debug feature was removed after LEGO Pirates of the Caribbean, therefore it will only be available for a few games.

# Supported Games
**Fully supported games:**
* LEGO Harry Potter: Years 1-4
* LEGO Star Wars III: The Clone Wars
* LEGO Pirates of the Caribbean The Video Game

**Games with almost full support (no map loading):**
* LEGO Harry Potter: Years 5-7

**Games with minimal support (player coordinates, hotkeys, N0CUT5):**
* LEGO Batman 2: DC Super Heroes
* LEGO The Lord of the Rings
* LEGO City Undercover
* LEGO Marvel Super Heroes
* The LEGO Movie Videogame
* LEGO The Hobbit
* LEGO Batman 3: Beyond Gotham (DX11)
* LEGO Jurassic World (DX11)
* LEGO Marvel's Avengers (DX11)
* LEGO Star Wars: The Force Awakens (DX11)
* The LEGO Ninjago Movie Video Game (DX11)
* LEGO Marvel Super Heroes 2
* LEGO The Incredibles
* LEGO DC Super-Villains
* The LEGO Movie 2 Videogame

**Unsupported games:**
* LEGO Star Wars: The Video Game
* LEGO Star Wars II: The Original Trilogy
* LEGO Star Wars: The Complete Saga*
* LEGO Indiana Jones: The Original Adventures*
* LEGO Batman: The Videogame*
* LEGO Indiana Jones 2: The Adventure Continues
* LEGO Dimensions
* LEGO Star Wars: The Skywalker Saga
* Any DX9 variant of a game that has (DX11) next to it's name

*For these games, it's highly recommended to use [Brickbench](https://github.com/BrickBench/BrickBench) instead.

PurpleBrick will only support the current newest version of each game, however in addition to this it also supports:
* QA versions of LEGO The Lord of the Rings, LEGO Marvel Super Heroes, LEGO Star Wars: The Force Awakens.
* The oldest version of LEGO Star Wars: The Force Awakens (29 June 2016).

As the development of PurpleBrick progresses, more and more games will be better supported by it. Even if a game is currently completely unsupported, that might change in the future.

# Installation
In order to install PurpleBrick, head to the [releases](https://github.com/Siedemnastek/PurpleBrick/releases) and download the installer from the latest release.
Once it gets downloaded, open the installer and follow the instructions on screen to install the program.

Upon finishing installation, a shortcut for PurpleBrick will be placed on Your Desktop, as well as the Programs Menu.

PurpleBrick has a built-in update checker, when a new version is available, you will be notified upon opening the program.

Please note: PurpleBrick only works for Windows Systems.

# Troubleshooting
.NET 8.0 is required to run PurpleBrick, it should install itself during the installation process of PurpleBrick, in case it doesn't, you can find it [here](https://dotnet.microsoft.com/en-us/download/dotnet/8.0).

If PurpleBrick fails to hook into a supported game, or some features that should be operational are not, please ensure:
* The name of the executable of the game is what it should be (example: doesn't have "unpacked" next to it's name if Steamless was used).
* You are running an un-modded version of the game.
* You are running the newest available version of the game.

In the event of any program crashes, bugs or other glaring issues, please contact Siedemnastek on Discord.

# Feature Documentation
This section is dedicated to explaining how each feature of PurpleBrick works and how to use it.

The first step upon launching PurpleBrick is always to press the **Hook into LEGO** button, this will connect the program to the currently open LEGO game and will allow the rest of the features to be usable.
Once this button is clicked, a **Stop hook** button will replace it, which when clicked will stop PurpleBrick from interacting with the game.

The left panel has the following checkboxes:
* **Enable hotkeys** - this enables PurpleBrick's custom hotkey functions, aach of the hotkey is described next to it's relevant function.
* **N0CUT5** - this enables the effects of the N0CUT5 code without needing to put it in manually. The code makes cutscenes skippable from new game.
* **Streaming Display** - this enables the debug feature of the same name, which will display when a map file is being dynamically loaded into the memory. This feature is mostly for fun, it does not serve a bigger purpose other than being able to find out in more detail how the streaming system works. The code from this debug feature was seemingly accidentally removed from games past LEGO Pirates of the Caribbean, meaning PurpleBrick also cannot enable this feature for games that came out after that.
              <img width="343" height="35" alt="Streaming Display Example" src="https://github.com/user-attachments/assets/54a5cee7-7c9c-4ef2-b15f-6d9c4e6ec2ac" />

In addition to this, the left panel has a button **Customize hotkeys**, clicking it will open up a seperate window, where you are able to change which button on your keyboard you want to do each function listed there.

**Player 1 and Player 2 panels:**

* Will display your player coordinates, depending on what players you currently have dropped in. 
* Each player coordinate has a field next to it accompanied by a **Change** button, typing a number next to a coordinate, then pressing it's respective **Change** button will change that coordinate to whatever was inputted in the field. The same effect as pressing the **Change** button can also be achieved by pressing your Teleport Player hotkey (T by default), however only if none of the coordinate fields are selected.
* In addition to changing your coordinates by typing values, you can also change each of them by +0.1 and -0.1 by using the custom hotkeys (1, 2, 3, 4, 5, 6 by default). This quick coordinate changing feature can very easily be used to clip through walls or speed up your movement. There is 2 more hotkeys that also affect player coordinates - Increase Y by 4 (9 by default), which can be used to quickly teleport very high into the air; and Lift Player (L by default), which is similiar to what Increase Y by 0.1 does, however Lift Player also resets your velocity, meaning it can be used to stay in the air forever.

Note: In LEGO games, the Y coordinate is the height, while X/Z are forwards/backwards/left/right, this is dependent on how the camera behaves in the map you are in, in the case of a static forward facing camera - the Z coordinate is usually forwards/backwards. 

**Game Manager**

This panel currently only has map loading. In order to use it (for games that currently support it), all you need to do is select a map you want to load from the dropdown list, then click the **Load Map** button or press your Load Map hotkey (F12 by default). You can also find a checkbox **Reset level on map load** below, when this is disabled, you will be able to seemlessy load between the maps in the **same level** and keep all of your progress in that level (studs, minikits), when the checkbox is enabled, the level progress will always reset when a map is loaded. 

Note: If the **Reset level on map load** checkbox is disabled, and you attempt to load into a map you are currently in, PurpleBrick will act as if that checkbox is enabled. This is not a bug and works this way to avoid a certain game crash that would otherwise happen, the cause of why this causes the game to crash is currently unknown, and a workaround hasn't been found. For the same reason, this checkbox is always enabled and cannot be disabled in LEGO Harry Potter: Years 1-4, as the problem is more severe in that game.

**Door Finder**

This panel is for getting information on every GizDoor in the game. The first dropdown list can be used to select the level, the second to select the map in the level, the third to select the actual door.
After selecting a door from the list, you will see all the available information on it. Here is how to use this information:
* If the name of the door has an arrow pointing to a different map name, this means hitting this door will take you to that map, if the arrow isn't present, the door will place you somewhere on the same map.
* The Door Finder will display 2 numbers for each X/Y/Z coordinate, these are essentially the minimum and maximum values of the door.
* More likely than not, one of the coordinates will not be 2 different values, instead it will show the same for both minimum and maximum, this means the door is placed on that axis.
* Below the coordinates, there is a **Hit:** field, this will tell you what direction you need to go towards to hit the door - for example if it says Hit: Z Down, this means the door can only be hit when you are going in a direction that makes you Z coordinate decrease.
* For some doors, below the **Hit:** field there will also be a note on the door, if there is a note saying the door is **Inactive** this means attempting to hit it will not result in anything, if a note says **Inactive until.../Active after**, this means a condition neeeds to be reached for the door to be hittable, there is also some other notes, however those should be self-explanatory.
  
In order to actually hit a door based on this information, all of your coordinates need to be in range of what the Door Finder displays for the door, and then you need to hit in the correct direction. Using the image below, assuming your X coordinate is between 16.68 and 17.18, your Y coordinate is between 2.15 and 2.65, you then need to make your Z coordinate close to 22.44, and then go in the Z Up direction to hit the door.

<img width="375" height="355" alt="image" src="https://github.com/user-attachments/assets/af8bb468-c814-4200-b119-7d347d7d7441" />

To help with practicing hitting doors, you can enable the **Track for P1/P2** checkboxes, this will make each coordinate red when it's not in range of the door, and green when it is in range.

<img width="376" height="147" alt="image" src="https://github.com/user-attachments/assets/3b12e335-d06a-4c8b-b98f-4ddee6d571e6" />
 
