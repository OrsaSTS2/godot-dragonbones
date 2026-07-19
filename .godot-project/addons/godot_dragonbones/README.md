# Godot-DragonBones Plugin

![Icon](img/icon.png)

A GDExtension plugin to add DragonBones to Godot.

Fork of [Daylily-Zeleen/Godot-DragonBones](https://github.com/Daylily-Zeleen/Godot-DragonBones) that adds missing features.

![Example screenshot](img/example.png)

## Support Versions

* Godot 4.2 +
* DragonBones Pro 5.6

## How to use

1. Download the latest version from the [releases page](https://github.com/OrsaSTS2/godot-dragonbones/releases).
2. Drag-and-drop the "addons" folder to the root of your project.
3. Add a `DragonBonesArmatureView` node to your scene and give it a `DragonBonesFactory` created from your files.

## How to compile

1. Clone this repo.
2. Make sure you have Python and Scons installed.
3. Open the project in VSCode and press F5, **OR** navigate to the root of local repo, and run the `scons` command:
   For debug:

   ```shell
   scons target=template_debug debug_symbols=yes
   ```

   For release:

   ```shell
   scons target=template_release
   ```

   More info here: [godot-cpp - Getting started - Compiling](https://docs.godotengine.org/en/stable/tutorials/scripting/cpp/gdextension_cpp_example.html#compiling-the-plugin).

4. Compiled binaries end up in `bin/` and in `.godot-project/addons/godot_dragonbones/bin`