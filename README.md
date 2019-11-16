# Cats Blender Plugin (0.16.0)

A tool designed to shorten steps needed to import and optimize models into VRChat.
Compatible models are: MMD, XNALara, Mixamo, Source Engine, Unreal Engine, DAZ/Poser, Blender Rigify, Sims 2, Motion Builder, 3DS Max and potentially more

With Cats it takes only a few minutes to upload your model into VRChat.
All the hours long processes of fixing your models are compressed into a few functions!

So if you enjoy how this plugin saves you countless hours of work consider supporting us through Patreon.
There are a lot of perks like having your name inside the plugin!

[![](https://i.imgur.com/BFIald5.png)](https://www.patreon.com/catsblenderplugin)

#### Download here: [Cats Blender Plugin](https://github.com/michaeldegroot/cats-blender-plugin/archive/master.zip)

## Features
 - Optimizing model with one click!
 - Creating lip syncing
 - Creating eye tracking
 - Automatic decimation
 - Creating custom models easily
 - Creating texture atlas
 - Creating root bones for Dynamic Bones
 - Optimizing materials
 - Translating shape keys, bones, materials and meshes
 - Merging bone groups to reduce overall bone count
 - Protecting your avatars from game cache ripping
 - Auto updater

*More to come!*

## Discord
Join our Discord to report errors, suggestions and make comments!

**Discord: https://discord.gg/f8yZGnv**

## Requirements
 - Blender **2.79** or **2.80** (run as administrator is recommended)
   - mmd_tools is **no longer required**! Cats comes pre-installed with it!
 - If you have custom Python installed which Blender might use, you need to have Numpy installed

## Installation
 - Download the plugin: [Cats Blender Plugin](https://github.com/michaeldegroot/cats-blender-plugin/archive/master.zip)
 - Install the the addon in blender like so:

![](https://i.imgur.com/eZV1zrs.gif)

 - Check your 3d view and there should be a new menu item called **CATS** ....w00t
   - Since Blender 2.80 the CATS tab is on the right in the menu that opens when pressing 'N'

![](https://i.imgur.com/pJfVsho.png)

 - If you need help figuring out how to use the tool:

[![VRChat - Cat's Blender Plugin Overview](https://img.youtube.com/vi/0gu0kEj2xwA/0.jpg)](https://www.youtube.com/watch?v=0gu0kEj2xwA)

Skip the step where he installs "mmd_tools" in the video below, it's not needed anymore!

[![VRChat - Importing an MMD to VRChat Megatutorial!](https://img.youtube.com/vi/7P0ljQ6hU0A/0.jpg)](https://www.youtube.com/watch?v=7P0ljQ6hU0A)

## Code contributors:
 - Hotox
 - Shotariya
 - Neitri
 - Kiraver


## Model
![](https://i.imgur.com/dYYAfb4.png)

This tries to completely fix your model with one click.

##### Import/Export Model
- Imports a model of the selected type with the optimal settings
- Exports a model as an .fbx with the optimal settings

##### Fix Model
- Fixes your model automatically by:
  - Reparenting bones
  - Removing unnecessary bones
  - Renaming and translating objects and bones
  - Mixing weight paints
  - Rotating the hips
  - Joining meshes
  - Removing rigidbodies, joints and bone groups
  - Removing bone constraints
  - Deleting unused vertex groups
  - Using the correct shading
  - Making it compatible with Full Body Tracking
  - Combining similar materials

##### Start Pose Mode
- Lets you test how bones will move.

##### Pose to Shape Key
- Saves your current pose as a new shape key.

##### Apply as Rest Pose
- Applies the current pose position as the new rest position. This saves the shape keys and repairs ones that were broken due to scaling


## Model Options

![](https://i.imgur.com/ZPj2VUJ.png)

##### Translation
- Translate certain entities from any japanese to english.
This uses an internal dictionary and Google Translate.

##### Separate by material / loose parts / shapes
- Separates a mesh by materials or loose parts or by whether or not the mesh is effected by a shape key

##### Join meshes
- Joins all/selected meshes together

##### Merge Weights
- Deletes the selected bones and adds their weight to their respective parents

##### Delete Zero Weight Bones
- Cleans up the bones hierarchy, deleting all bones that don't directly affect any vertices

##### Delete Constraints
- Removes constrains between bones causing specific bone movement as these are not used by VRChat

##### Recalculate Normals
- Makes normals point inside of the selected mesh
- Don't use this on good looking meshes as this can screw them up

##### Flip Normals
- Flips the direction of the faces' normals of the selected mesh.

##### Apply Transformations
- Applies the position, rotation and scale to the armature and its meshes.

##### Remove Doubles
- Merges duplicated faces and vertices of the selected meshes.


## Custom Model Creation

![](https://i.imgur.com/szIWglS.png)
![](https://i.imgur.com/04O63q1.png)

**This makes creating custom avatars a breeze!**

##### Merge Armatures
- Merges the selected armature into the selected base armature.
- **How to use:**
  - Use "Fix Model" on both armatures
    - Select the armature you want to fix in the list above the Fix Model button
    - Ignore the "Bones are missing" warning if one of the armatures is incomplete (e.g hair only)
    - If you don't want to use "Fix Model" make sure that the armature follows the CATS bone structure (https://i.imgur.com/F5KEt0M.png)
    - DO NOT delete any main bones by yourself! CATS will merge them and delete all unused bones afterwards
  - Now you have two options:
    - Only move the mesh:
      - Uncheck the checkbox "Apply Transforms"
      - Move the mesh (and only the mesh!) of the merge armature to the desired position
        - You can use Move, Scale and Rotate
        - CATS will position the bones according to the mesh automatically
    - OR move the armature (and with it the mesh):
      - Check the checkbox "Apply Transforms"
      - Move the armature to the desired position
        - You can use Move, Scale and Rotate
        - Make sure that both meshes and armatures are at their correct positions as they will stay exactly like this
    - If you want to merge multiple objects from the same model it is often better to duplicate the armature for each of them and merge them individually
  - Select the base armature and the armature you want to merge into the base armature in the panel
  - If CATS can't detect the bone structure automatically: select a bone you want to attach the new armature to
    - E.g.: For a hair armature select "Head" as the bone
  - Press the "Merge Armatures" button -> Done!

##### Attach Mesh to Armature
- Attaches the selected mesh to the selected armature.
- **How to use:**
  - Move the mesh to the desired position
    - You can use Move, Scale and Rotate
    - INFO: The mesh will only be assigned to the selected bone
    - E.g.: A jacket won't work, because it requires multiple bones.
    - E.g.: A ring on a finger works perfectly, because the ring only needs one bone to move with (the finger bone)
  - Select the base armature and the mesh you want to attach to the base armature in the panel
  - Select the bone you want to attach the mesh to in the panel
  - Press the "Attach Mesh" button -> Done!

##### Support us:
- We worked hard on this feature. If you like it consider supporting us, it helps a lot!

[![](https://i.imgur.com/BFIald5.png)](https://www.patreon.com/catsblenderplugin)


## Decimation

![](https://i.imgur.com/vozxKy9.png)

**Decimate your model automatically.**

##### Save Decimation
- This will only decimate meshes with no shape keys.

##### Half Decimation
- This will only decimate meshes with less than 4 shape keys as those are often not used.

##### Full Decimation
- This will decimate your whole model deleting all shape keys in the process.

##### Custom Decimation
- This will let you choose which meshes and shape keys should not be decimated.


## Eye Tracking
![](https://i.imgur.com/yw8INDO.png)
![](https://i.imgur.com/VHw73zM.png)

**Eye tracking is used to artificially track someone when they come close to you.**
It's a good idea to check the eye movement in the testing tab after this operation to check the validity of the automatic eye tracking creation.

##### Disable Eye Blinking
- Disables eye blinking. Useful if you only want eye movement.

##### Disable Eye Movement
- Disables eye movement. Useful if you only want blinking. **IMPORTANT:** Do your decimation first if you check this!

##### Eye Movement Speed
- Configure eye movement speed


## Visemes (Lip Sync)
![](https://i.imgur.com/muM2PTS.png)

**Mouth visemes are used to show more realistic mouth movement in-game when talking over the microphone.**
The script generates 15 shape keys from the 3 shape keys you specified. It uses the mouth visemes A, OH and CH to generate this output.


## Bone parenting

![](https://i.imgur.com/mgadT4R.png)

**Useful for Dynamic Bones where it is ideal to have one root bone full of child bones.**
This works by checking all bones and trying to figure out if they can be grouped together, which will appear in a list for you to choose from. After satisfied with the selection of this group you can then press 'Parent bones' and the child bones will be parented to a new bone named RootBone_xyz

##### To parent
- List of bones that look like they could be parented together to a root bone. Select a group of bones from the list and press "Parent bones"

##### Refresh list
- Clears the group bones list cache and rebuild it, useful if bones have changed or your model

##### Parent bones
- Starts the parent process


## Texture atlas
![](https://i.imgur.com/XcoF0Ek.png)

**Texture atlas is the process of combining multiple textures into one to drastically reduce draw calls and therefore make your model much more performant**

##### Create Atlas
- Combines all selected materials into one texture. If no material list is generated it will combine all materials.

##### Generate Material List
- Lists all materials of the current model and lets you select which ones you want to combine.

### Useful Tips:
- Split transparent and non-transparent textures into separate atlases to avoid transparency issues
- Make sure that the created textures are not too big, because Unity will downscale them to 2048x2048. 
  Split them across multiple atlases or reduce the individual texture sizes. This can be easily done in the MatCombiner tab.
- You can tell Unity to use up to 8k textures.
  Do so by selecting the texture and then choose a different Max Size and/or Compression in the inspector:
  https://i.imgur.com/o01T4Gb.png


## Bone merging

![](https://i.imgur.com/FXwOvho.png)

**Lets you reduce overall bone count in a group set of bones.**
This works by checking all bones and trying to figure out if they can be grouped together, which will appear in a list for you to choose from. After satisfied with the selection of this group you can then set a percentage value how much bones you would like to merge together in itself and press 'Merge bones'

##### Refresh list
- Clears the group bones list cache and rebuild it, useful if bones have changed or your model

##### Merge bones
- Starts the merge process


## Copy Protection

![](https://i.imgur.com/5qP5bCT.png)

**Can protect your avatars from being ripped from the game cache.**
Game cache rips in most common cases do not include blendshapes and shaders. 
This method will make it much harder for people that try to steal your avatar through ripping from cache.

**This is NOT a 100% protection**, but it's the best what you as a creator can currently do. If you want to be 100% safe, stay in private worlds with people you trust.

#### How to setup:

1. Do all the modifications to your model in Blender before you follow the next steps!
   This option should be the last one you do in Blender before exporting!
2. You won't be able to see the mesh of your model inside the Unity bone mapping screen (it will be garbled mess, but only in there).
   Because of that, if you need to actually see your models mesh (e.g. for straightening the fingers for VR), follow the extra steps below.
   If you don't need to see the mesh (e.g. for unassigning the jaw bone) skip to step 2.
     - Export your model from Blender without enabling the protection
     - Load it up in Unity and configure it in the bone mapping screen and press "Done"
     - In Blender: Click the "Enable Protection" button and export your model
     - Then, except for just dragging the fbx into Unity, you need to go into the folder where this Unity project is located
       and then replace the unprotected fbx with the protected one. 
       That way your configurations will be kept.
     - Skip to step 5
3. In Blender: Click the "Enable Protection" button
4. Export it to Unity by either using the "Export" button within Cats or set the fbx export option by yourself: 
   Geometries > Smoothing > Set to "Face"
5. In Unity: Set the value of the blendshape 'Basis Original' to 100 like so: 
   https://i.imgur.com/RlrGTvV.gif
6. To fix any lighting issues select your .fbx and then select "Import" as the Tangents option here: 

   ![](https://i.imgur.com/SqynQzw.png)
7. Because (for some odd reason) the protection increases your bounding box it could be too big to upload your model.
   If the VRCSDK complains about your model being too large, edit your bounding box back to normal here:
   (this option is below the blendshape list from above)
   
   ![](https://i.imgur.com/4NrfVOr.png)
8. Your avatar now behaves just like a normal one.

People that try to steal your avatar will then only see a box of mangled waifu trash instead of your original character.

  **special thanks to @zarniwoop#6081**


## Shape Key

![](https://i.imgur.com/LgFK4KO.png)

**Apply Shape Key as Basis**
- Applies the selected shape key as the new Basis and creates a reverted shape key from the selected one.


## Settings and Updates

![](https://i.imgur.com/hYy7gD8.png)

**This plugin has an auto updater.**
It checks for a new version automatically once every day.


## Changelog

#### 0.16.0
- **Cats is now fully compatible with Blender 2.81!**
- **Importer**:
  - Added support for ZIP files
    - It will only extract the zip if importable models are found
    - If multiple models are found in the zip, you can select the one you want in a popup window
    - Japanese zip files will be extracted with the correct encoding
  - Models can now be imported with Cats via the windows command shell
- **Fix Model**:
  - Hips bone will now be larger than before, to comply with the adjusted VRChat recommendation
  - FFXIV models are now compatible
- **Model Options**:
  - Remove Doubles no longer effects meshes with no shapekeys
- **Custom Model Creation**:
  - Added "Join Meshes" option
  - Merge Armatures and Attach Mesh no longer require a mesh on the armature
  - Fixed bones from the merge armature sometimes getting unintentionally deleted
- **Optimization**:
  - Added manual download button if Material Combiner is outdated
- **General**:
  - Armatures will no longer be forced into rest position after any action
  - Fixed armatures sometimes not getting detected
  - Small bug fixes
  - Updated mmd_tools

#### 0.15.0
- **Importer**:
  - FBX no longer imports animations and poses by default
- **Fix Model**:
  - Now always applies transforms of the model
  - Added "Keep Upper Chest" option
    - Warning: Currently having an Upper Chest breaks Eye Tracking, so don't use this if you want Eye Tracking
  - Removed "Fix Full Body Tracking" option
    - It is no longer needed for VRChat
    - The button to add/remove the fix is still available in Model Options
  - Improved Hips placement as recommended by VRChat
  - Legs are now getting bend forward very slightly if they are completely straight
  - Fixed a bug which could sometimes delete bones unintentionally
- **Model**:
  - Fixed pose mode error in 2.80
- **Model Options**:
  - Added new "Delete Zero Weight Vertex Groups" button
  - Improved layout of the "Full Body Tracking Fix" buttons
  - Fixed visual "Merge Weights" bug in Blender 2.80
- **Optimization**:
  - Improved Material Combiner detection algorithm
- **General**:
  - Updated mmd_tools

#### 0.14.0
- **Cats is now fully compatible with Blender 2.80!**
- **Fix Model**:
  - Improved DAZ compatibility
- **Model Options**:
  - Added "Merge Weights" and "Remove Zero Weight Bones" to the spacebar search
  - Added "Apply All Transforms" button to correctly apply the transforms of all objects
  - Separating Meshes now deletes the Basis shape key if it is the last shape key left
- **Custom Model Creation**:
  - Added "Apply Transforms" option to "Merge Armatures"
    - Use this if both armatures and meshes are already at their correct positions
  - Merge Armature and Attach Mesh now correctly restore the initial state from before the operation
- **Visemes**:
  - Fixed shape keys sometimes not appearing in the viseme list
- **Optimization**:
  - "Combine Same Materials" and "Convert Textures to PNG" are now compatible with Blender 2.80
  - Added loading cursor to "Convert Textures to PNG"
  - Added support for Shotariyas Material Combiner in Blender 2.80
    - Minimum required Material Combiner version is now v2.1.1.2
      - It now fully supports VRM models, has a greatly improved combining logic and an updated UI
      - It also got compression removed, so you will always get full quality images now
- **Updater**:
  - Made it more robust to different version naming schemes
- **General**:
  - Improved shading in 2.80
  - Improved initial state restoration after an operation
  - Backface culling is now always toggled on
  - Removed tons of unintended functions from the spacebar search
  - Upon startup Cats now enables "Testing" as supported addon level
  - Updated mmd_tools
  - Fixed a bug while loading settings during startup
  - Fixed a bug while loading the initial state after an operation

#### 0.13.3
- **Importer**:
  - Fixed imported armatures being in edit mode
- **Custom Model Creation**:
  - Merge Armatures now properly merges bones when the vertex group of one of the merging bones is missing
  - Attach Mesh no longer removes zero weight bones and constraints
- **Model Options**:
  - Fixed error when switching to object mode during pose mode
- **General**:
  - Updated mmd_tools
  - The Blender 2.80 API is stable now, so Cats should no longer break in 2.80

Read the full changelog [here](https://github.com/michaeldegroot/cats-blender-plugin/releases).


## Roadmap
 - MOAR updates on the armature code
 - Texture translation should have an option to rename the filename also
 - Automatic lower lid creation for eye tracking
 - Manual bone selection button for root bones
 - Full body tracking proportion adjustments


## Feedback
Do you love this plugin or have you found a bug?
Post a response in this thread or send your feedback to the official discord server of the plugin for real-time communication: https://discord.gg/f8yZGnv and look for people with the developer role ;)


## Support us
If you enjoy how this plugin saves you countless hours of work consider supporting us through Patreon:

[![](https://i.imgur.com/BFIald5.png)](https://www.patreon.com/catsblenderplugin)
