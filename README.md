# YAAM Inception
YAAM is a simple asset manager add-on for [Blender 3D](https://www.blender.org). I'm currently working on an [open movie project](https://www.openmovie.org). It's an animated series which is developed in the open, similar to open source software. People can elect to contribute their talent to the project. I'm currently in the Research and Development phase; trying to build the 10K view of the work needed. I decided to make an approximately thirty second animated sequence with multiple shots to work out the kinks from my pipeline. The first hurdle I faced to keep this minor project organized is an asset manager. This is how YAAM was born. Yet Another Asset Manager. 

# Blender 2.8 Compatible
YAAM supports Blender 2.8. It does not work with previous versions of Blender.

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
In Browse mode, assets can be browsed and imported into the scene. An obj, image or blend files can be imported into the scene by clicking on the "import" button.
A blend asset can be appended or linked into the current scene. The following items are available to be appended or linked:
* Collections
* Objects
* Textures
* Materials
* Scenes

## Manage
In Manage mode, new assets can be created and added via YAAM to the asset directory specified above.
The image of an asset file can be updated by selecting it, and then clicking on the "snap image" button. To update a specific asset, open the asset file and preform the "snap image" operation.

# Graphical User Interface
## Manage GUI
![YAAM Manage Mode](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI.jpg)

## Browse GUI
![YAAM Browse Mode](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI2.jpg)

## Blend Import Specifics
![Blend Import](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI3.jpg)

# YAAM Organize
YAAM provides a way to organize existing assets in order to be managed by YAAM. In the "YAAM Organize" section enter the following information
* Path to the Blender 3D executable. If not specified, then it's assumed to be in the default executable path.
* Source asset directory. The directory you wish YAAM to manage
* Destination asset directory. The YAAM Managed asset directory. The top level directory must already be created. YAAM can create the rest of the subdirectories.

The operation doesn't touch the source asset directory. It's up to the user to remove it.

## YAAM Organize GUI
![Blend Import](https://github.com/amirpavlo/YAAM/blob/master/Docs/YAAM_GUI4.jpg)

# Possible Future Improvements
I wrote this add-on to help me organize the assets I download or build. As I was building a larger scene, I realized how difficult it is to have to go to the file browser every time I needed to import an asset. It really slowed down my progress. Having said that, obviously, this is not intended to be a heavy weight, fully blown digital asset manager; not at its inception anyway.

Moving forward some improvements that can be added:

* use a backend database to store references to assets
* use a version manager, like GIT, to keep track of the revisions on each asset
* support editing of assets within a blender instance. 
* support publishing of assets
* support network access
