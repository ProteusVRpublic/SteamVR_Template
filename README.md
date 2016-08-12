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
* Grab Plugin and functionnalities: @mordentral
* Vive Controller inputs image: @mitchemmc
* Teleport function #2, UltraMan: @PenguinTD

For questions,s see the forum thread: https://forums.unrealengine.com/showthread.php?106609-Steam-VR-Template 

# Version 1.10.1 – UE4.12.3: June 15, 2016 #

* Updated to 4.12.3
* Updated grab plugin
* Left and Right grab hands
* New vehicle controls: vehicle rotate with direction
* New environment with interactive consoles
* Chaperone poles spawn fixed
* Less settings; the rest will be in a future 3D menu
* Matinee changed for Sequencer
* Small glitches and crashes fixed
* Vive_Pawn_Complete, with every functions (except vehicle)
* Vive_Pawn_Vehicle, Vive_Pawn_Grab_Plugin (no lightsaber), Vive_Pawn_UltraMan will each do a specific function; only Vive_Pawn_Grab_Plugin uses the plugin; select pawn in Steam_GM
* Fixed chaperons's poles and exit simple platform

The Vive_Pawn_Complete does everything, except vehicle

Following many requests, this is to facilitate the migration of the pawn into another project.

#Features#

* Animated triggers in both controllers
* Map of all buttons/trackpad on controllers
* Toggle on/off debugging squares of controllers and/or base stations
* Toggle on/off debugging meshes of base stations
* 2 different ways to teleport
* Ghost move
* Basic vehicle
* Scalability settings for Vive
* Finger tracking on trackpad
* Trace line with trigger
* Force feedback
* Textures on cubes and sphere to test scalability settings
* Toybox: 4 objects with skeletal sockets: the sword, the gun, the baton, the lightsaber; 1 object with mesh socket: the book; 1 object without sockets: the hat
* Animated "grabbing" mesh left and right hands
* Teleportation with trackpad à la The Lab with cylinder & particles validation
* Go/No go teleportation zones with camera fade out
* Moving platform for testing purpose, by simple actor move (embark by triggering overlap volume or teleportation; disembark by teleportation) and Sequencer (embark/disembark with controller input)
* Triggerable poles at the 4 chaperone corners
* Addition of a cone at the tip of the right trigger -- can be rotated
* “UltraMan” mode
* Standing/seated experience switch
* Grab function

Setup
Files can be found [on OneDrive] https://1drv.ms/f/s!AhConHxqM4Nisn-TFO1AtRNCJWhn

GitHub version at https://github.com/ProteusVR/SteamVR_Template (you need to be logged to Github to open the link) 

To install as a template, just unzip into the appropriate templates directory like C:\Program Files\Unreal Engine[Version]\Templates for launcher version or[ForkLocation]\UE4\Templates for source version. 

Launch a new project, and you'll find it in the blueprint section.

To install as a project file, unzip in your usual projects folder. Then, delete the file SteamVR_x-x/Config/TemplateDefs.ini and you’re ready to go.

# IMPORTANT: If you open it like a regular project without deleting the .ini file, you’ll get errors messages.#

Note 1: To enable the template within an existing project:
To migrate pawn in another project:
Migrate Vive_Pawn_Vehicle, Vive_Pawn_Grab_Plugin, or Vive_Pawn_UltraMan in another project
* For Vive_Pawn_Vehicle, migrate the Vehicle Pawn also; for Vive_Pawn_Grab_Plugin be sure that the objects to grab have the blueprints and 3 interfaces and the the grab plugin is in the plugin folder
* For all pawns, select the right pawn in the Steam_GameMode (GM); copy scalability and initial settings in level blueprint; in project settings set Engine/General Settings at USe Fixed Frame Rate 90, Engine/Rendering/Default Postprocessing settings: Uncheck everything (bloom is optional), choose AA method; Engine/Rendering/VR: Check Instanced Stereo. Put a post-process volume in the level and adjust it accordingly. Be sure that the SteamVR Game Mode (SteamVR_GM) and Steam_player_controller have followed if not recreate them.
You should now easily migrate one of these 3 pawns into another project. More example pawns to follow soon.

Note 2: To package your project:
Don’t forget to File/New C++ class, None, Create Class before packaging, if not the plugin won’t follow. Be sure to have a working copy of Visual Studio 2015 enabled.
