# Diablo Style Loot for Elden Ring
A WIP loot generator for Elden Ring, to be used with DSMapStudio.

How to Create Custom Itemlot Sets for DSL4ER - https://github.com/CornflakeWoof/Diablo-Style-Loot-for-Elden-Ring/wiki/Creating-a-Custom-Itemlot-Set

## Required Programs
* DSMSPortable - https://github.com/mountlover/DSMSPortable/releases/tag/v1.4.7 - Download DSMSPortable, unzip this .bat file - https://github.com/CornflakeWoof/Diablo-Style-Loot-for-Elden-Ring/files/10529609/ImportIntoDiabloLootER_release.zip - into its folder, edit the variables at the top so that the paths requested are accurate to your system, and run the .bat after generating loot to implement it into your game!
* ModEngine 2 - https://github.com/soulsmods/ModEngine2/releases

## How To Use

1) Download and extract DSL4ER to a location of your choosing.
2) When you open DSL4ER, press "OPEN EXPORT DIRECTORY"
3) Copy and paste everything in the "PLACE_INTO_USER_DATA_FOLDER" zip file into this directory.
4) Restart DSL4ER to load the new data sets.
5) Enter your desired seed into the box just under "RANDOM SEED" and click "GENERATE DIABLO LOOT" to put DSL4ER to work.
6) Once it's finished, click "OPEN EXPORT DIRECTORY" and navigate into the "output -> [Your Seed Text]" folder. You should see a number of CSV and .json files.
7) Extract ModEngine 2 somewhere of your choosing - I recommend putting it in a folder named "ModEngine2" in the ...steamapps/common/ELDEN RING/ folder.
8) Follow the DSMSPortable instructions above!
9) Head into your ModEngine folder, open "config_eldenring.toml" in a text editor, add this line at the top of your mod list:' { enabled = true, name = "diabloloot", path = "diabloloot_er" }, then save it.
10) Run "launchmod_eldenring.bat" and (hopefully) enjoy your new custom DSL4ER-enhanced game!

## Source Code

DSL4ER was written in Godot Engine 3.5.1's GDScript language. You can grab the required version of Godot from https://godotengine.org/download/windows

* Please be aware that the source code is a bit of a mess at the moment, with unused functions and incomplete new features.
* Most of the generation logic is found in Weapon_Generator.gd. 
* LootBank.gd defines where the generated loot is stored so it can be easily referenced
* Weapon/ArmorBank.gd covers loading EquipParamWeapon and EquipParamProtector values from the text files provided in the "PLACE_INTO_USER_DATA_FOLDER" folder.

## Credits

* Massive thanks to Kehom's Forge for their fantastic Godot 3 addons pack, particularly the Database addon - http://kehomsforge.com/tutorials/multi/GodotAddonPack/part07 - which made a lot of things about this project much easier to manage.
