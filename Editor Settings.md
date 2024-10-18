Now some editor settings:

> Note there may be minor discrepancies as these are done in 4.3 Release Candidate 1\
> Any setting not listed is left as the default as of 4.3 RC 1

## Interface

### Editor

- **Editor Screen** and **Project Manager Screen** > Screen with Mouse Input
 	- Sets what monitor Godot opens on, generally will be more correct than default behaviour. Could also do "Screen With Keyboard Focus"
- **Use Native File Dialogs** > On
 	- I find Godot's custom file explorer clunky, this lets me use the Windows default. Note this has a few usability bugs, maybe wait until 4.4
- **Save on Focus Loss** > On
 	- When I tab out, auto save's the scene/script. Nice when tabbing to Github Desktop
- **Import Resources When Unfocused** > On
 	- This one is more personal preference, usually after adding files to the project you'd have to click on Godot and wait for it to reload. This allows it to reload automatically as soon as the files are added, removing the wait

### Inspector

- **Float Drag Speed** > 0.1
 	- Useful for custom properties, 5 is way too huge when most of my exported floats are supposed to be touchy. Maybe 0.2 would be good
- **Default Color Picker Shape** > HSV Rectangle Wheel or HSV Rectangle
 	- I dislike the default colour picker, find the wheel feels easier to use

### Theme

- As stated before, I use Passive Star's [Minimal Theme](<https://github.com/passivestar/godot-minimal-theme>) (except for the font change)

## FileSystem

### External Programs

- Hook up any external editors you have (raster/vector/audio/3d model). this allows right-clicking (for example) an mp3 file, choosing "Open in External Program", and automatically sending it straight into  Audacity\
If unset, uses system default\
Sadly, Blender can't handle opening exported models (eg gltf) directly

### Directories

- **Autoscan Project Path** and **Default Project Path** > C:\Users\nick\Documents\Godot
 	- Setting the default and autoscan to the same path is quite convenient, and good to move it out of Documents so things can be a little more organized. I then create all my projects in the "Godot" folder in Documents

### Import

- **Blender Path** > The path to your blender.exe executable
- **RPC Port** > Anything but 0 (I believe 6011 is default, can set this really set this to anything though *except 0*)

## Text Editor

### Behavior

#### Navigation

- **Scroll Past End of File** > On
  - Personal preference, I like having it when I'm typing a lot of code

#### Files

- **Autosave Interval Secs** > Anything but 0
  - I set mine to 15, this is just autosave. May not always be desireable, but with undo steps and version control, I think it's nice to have on
- **Auto Reload Scripts on External Change** > On
  - This paired with autosaving may resolve *some* of the git overriding issues we've had, though it's also good if merge conflicts were resolved in an external editor

### Completion

- **Idle Parse Delay** > 0.1
  - This is the lowest possible and will greatly improve the responsiveness of error checking
- **Code Complete Delay** > 0.01
  - This is also the lowest possible, makes autocomplete kick in faster. This one's more personal preference

## Debugger

- **Auto Switch to Remote Scene Tree** > On
  - Very personal preference, usually depends what I'm doing. Can be nice to see the remote more often to better gauge the layout of the game

## Project Manager

- **Directory Naming Convention** > PascalCase or Title Case
  - Personal preference

---
Other things of note:

- Some line numbers are grey, others are green. Why?\
A green line number means the type of all variables on that line are known, and so it may run faster thanks to typed instructions!
- Lines of code can be bookmarked!\
Either right click and choose "bookmark", or use the hotkey ctrl+alt+B
- Viewport "Joysticks" can be enabled!\
Editor Settings > Editors > 3D > Navigation > Show Viewport Navigation Gizmo\
Left is view position, right is view rotation
