### Steam VR Template ###

Instruction guide [found in the onedrive]https://1drv.ms/f/s!AhConHxqM4Nisn-TFO1AtRNCJWhn

Disclaimer: The goal of this template is to put together a noob-proof SteamVR pawn to drop in your scene. However, one size for all solutions will not answer to all specific implementations, but it can gives you a head start. The template will be updated regularly with Unreal forum contributors suggestions. 

My eternal thanks to (but not only) @mitchemmc for input maps and controllers mapping and @PenguinTD for amongst many functions , teleportation method #2 and Ultraman.

Thanks to @mordentral for the grabbing fantastic plugin.

All assets are whether homemade, from the public domain or from Epic demos (you can use them freely in UE4 projects).

I remind everyone that any contribution is welcome. The commercial/fun value of VR projects is definitively not on who can use the Vive, who cannot. It's in the whole experience, the universe you are creating, the feeling, the originality and the user experience.

Have fun!

Mat, at Proteus VR


External credits:
* VRExpansion Plugin and functionnalities: @mordentral
* Vive Controller inputs image: @mitchemmc
* Teleport function #2, UltraMan: @PenguinTD

For questions,s see the forum thread: https://forums.unrealengine.com/showthread.php?106609-Steam-VR-Template 

# Version 1.12 – UE4.12.5: August 1, 2016 #

Changelog

* Fixed a missing folder preventing packaging project
* Added player snapshot inside the playground when teleporting
* Added a “legacy” teleportation method (select 1 and check “legacy teleport”)
* Fixed some bugs found in all pawns
* Added a FPS counter in front of the player
* Now using more features from mordentral’s plugin


#Features#

* Basic pawn with controllers meshes, trackpads, face
* Animated triggers and hands in both controllers
* Mapping of all buttons/trackpad on controllers
* Force feedback
* Selectable controllers’ skins & opacity
* Select alternate meshes for controllers
* Adjustable "safe" value to teleport on uneven surfaces
* Locomotion
* Teleport with trackpad and rotate playground with camera position
* Teleport with trigger
* Ghost Move
* Grab function
* #Additional functions#
* Go/No go teleportation zones with camera fade out
* Toggle on/off debugging squares of controllers and/or base stations
* Toggle on/off debugging meshes of base stations
* Triggerable poles at the 4 chaperone corners
* Basic vehicle functions
* Moving platform for testing purpose, by simple actor move (embark by triggering overlap volume or teleportation; disembark by teleportation) and matinee (embark/disembark with controller input)
* “UltraMan” mode
* Settings
* Basic settings
* Scalability settings
* Pawn settings
* Toybox
* 4 objects with skeletal sockets: the sword, the gun, the baton, the lightsaber; 1 object with mesh socket: the book; 1 object without sockets: the hat
* Multiplayer
* Multiplayer ready (missing: 3D widget interaction: soon!)

#Setup#
Files can be found [on OneDrive] https://1drv.ms/f/s!AhConHxqM4Nisn-TFO1AtRNCJWhn
GitHub version at https://github.com/ProteusVR/SteamVR_Template (you need to be logged to Github to open the link) 

To install as a template, just unzip into the appropriate templates directory like C:\Program Files\Unreal Engine[Version]\Templates for launcher version or[ForkLocation]\UE4\Templates for source version. 

Launch a new project, and you'll find it in the blueprint section.

To install as a project file, unzip in your usual projects folder. Then, delete the file SteamVR_x-x/Config/TemplateDefs.ini and you’re ready to go.

# IMPORTANT: If you open it like a regular project without deleting the .ini file, you’ll get errors messages.

To package your project:
Don’t forget to File/New C++ class, None, Create Class before packaging, if not the plugin won’t follow. Be sure to have a working copy of Visual Studio 2015 enabled.