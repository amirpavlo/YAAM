# YAAM
A blender Asset Manager developed as part of the open movie project (openmovie.org)

# YAAM Inception
YAAM is a simple asset manager add-on for [Blender 3D](https://www.blender.org). I'm currently working on an [open movie project](https://www.openmovie.org). It's an animated series which is developed in the open, similar to open source software. People can elect to contribute their talent to the project. I'm currently in the Research and Development phase; trying to build the 10K view of the work needed. I decided to make an approximately thirty second animated sequence with multiple shots to work out the kinks from my pipeline. The first hurdle I faced to keep this minor project organized is an asset manager. This is how YAAM was born. Yet Another Asset Manager. 

# Asset Directory Structure
There is an Asset directory, which gets installed along with the add-on, if installed from the .zip file. However, the add-on can be used to manage multiple asset directories. The list of asset directories can be stored in favourites and selected at any point in time.

The asset root directory can be arbitrary named. However all first level subdirectories must be named as indicated below. As will be highlighted later, YAAM can be used to create the asset directory structure as assets are added. However, if there are already a group of assets available, they can be copied in their corresponding subdirectory.

## The Structure
* Top_level_directory
  * 3ds
  * Blend
  * Fbx
  * Obj
  * Textures
  * DefIcons
  * Trash

### 3ds
3ds subdirectory contains a tree of 3DS files. This version of YAAM doesn't have support for importing and exporting 3DS files. Support will be added in future releases

### Blend
Blend subdirectory contains a tree of blend libraries.

### Fbx
Fbx subdirectory contains a tree of Fbx files.

### Obj
Obj subdirectory contains a tree of Obj files.

### Textures
Textures subdirectory contains a tree of images, which can be loaded into the scene. Currently supported formats are *.jpg, *.png, *.svg, and *.bmp

### DefIcons
Deficons subdirectory is a special subdirectory which should not be touched. It contains default icons used by the add-on.
TODO: This should be moved into its own folder and not included in the Assets directory

### Trash
Trash subdirectory is another special directory. It is created by the add-on when an asset is removed. For safety purposes when the add-on is used to remove an asset, it is moved to the 'Trash' subdirectory. This can be cleaned by the user at a later point.

Each subdirectory contains the corresponding asset category. The top level subdirectories out lined above can have multiple arbitrary subdirectories below it, to further organize the assets

# YAAM Modes
YAAM operates in two modes
* Browse
* Manage

## Browse
In Browse mode, assets can be browsed and imported into the scene

## Manage
In Manage mode, new assets can be created and added via YAAM to the asset directory specified above.

# Graphical User Interface
## Manage GUI
![YAAM Manage Mode](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI.jpg)

## Browse GUI
![YAAM Browse Mode](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI2.jpg)

## Blend Import Specifics
![Blend Import](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI3.jpg)
