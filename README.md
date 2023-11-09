# Godot Game Template
For Godot 4.1.3

This template has a dynamic main menu, pause menu, and credits scene. Multiple options menus to choose from with key rebinding and persistent config settings.

## Features

### App (Base)

The `App/` folder holds the core components of the menus application. It represents the minimum features and complexity.

-   Main Menu    
-   Options Menus
-   Pause Menu
-   Credits
-   Loading Screen
-   Persistent Settings
-   Simple Config Interface
-   Keyboard/Mouse Support
-   Gamepad Support

### Extras

The `Extras/` folder holds components that generally extend the core features.

-   Scripts for logging game starts, progress through levels, and playtime.
-   A `GameUI.tscn` scene that displays inputs and can trigger the pause menu.
-   Options menus that have an additional game option to reset the level progress.
-   An inherited `MainMenu.tscn` that uses the extra options menu and game scene.
-   An inherited `PauseMenu.tscn` that uses the extra options menu and main menu scene.
-   An inherited `InitApp.tscn` that uses the extra main menu scene.
-   An `EndCredits.tscn` scene, inherited from `Credits.tscn`, that uses the extra main menu scene.

  

## Usage

### App vs. Extras

To begin with, use the `Extras/` folder, and make changes there. However, to start minimally, use just the `App/` folder. Compare [Features](#features) to decide.

If you just want to use just the minimum App:

1.  Go to `Project > Project Settings… > General > Application > Run`.
    
2.  Update `Main Scene` to `res://App/Scenes/InitApp/InitApp.tscn`.
    
3.  Close the window.
    

The remaining instructions will apply the same for either folder you decide to use.

### New Project
These instructions assume starting with the entire contents of the project folder.
  

1.  Update the project’s name.
    

    1.  Go to `Project > Project Settings… > General > Application > Config`.
        
    2.  Update `Name` to `"Game Name"`.
        
    3.  Close the window.
        
    4.  Open `MainMenu.tscn`.
        
    5.  Select the `Title` node.
        
    6.  Update the `Text` to `"Game Name"`.
        
    7.  Save the scene.
        

2.  Point the main menu to the game scene.
    

    1.  Open `MainMenu.tscn`.
        
    2.  Select the `MainMenu` node.
        
    3.  Update `Game Scene Path` to the path of “Game Name” game scene.
        
    4.  Save the scene.
        

3.  Update the project’s inputs.
    

    1.  Go to `Project > Project Settings… > Input Map`.
        
    2.  Update the input actions and keybindings for “Game Name”.
        
    3.  Close the window.
        
    4.  Open `InputOptionsMenu.tscn`.
        
    5.  Select the `Controls` node.
        
    6.  Update the `Action Name Map` to show readable names for “Game Name” input actions.
        
    7.  Update the `Add Button Texture` and `Remove Button Texture` with textures.
        
    8.  Save the scene.
    

4.  Update the game credits / attribution.
    

    1.  Copy `ATTRIBUTION_example.md` over `ATTRIBUTION.md`.
        
    2.  Update `ATTRIBUTION.md` with “Game Name” credits, following the example.
        
    3.  Reload `Credits.tscn` scene to apply changes from `ATTRIBUTION.md`.
        
    4.  Include the attribution in exports.
        

        1.  Go to Project > Export.
            
        2.  Select one of “Game Name” presets (or set them up).
            
        3.  Select the Resources tab.
            
        4.  Update `Filters to export non-resource file/folders` to include `ATTRIBUTION.md`.
            
        5.  Close the window.
    


### Existing Project

For an existing project, just copy over the `App/` folder (optionally the `Extras/` folder, as well).

  

1.  Update the project’s main scene.
    

    1.  Go to Project > Project Settings… > General > Application > Run.
        

    2.  Update `Main Scene` to `res://…/InitApp.tscn`.
        
    3.  Close the window.
    

2.  Update the project’s autoloads.
    

    1.  Go to Project > Project Settings… > Autoload.
        
    2.  Add `res://App/Scripts/SceneLoader.gd`.
        
    3.  Add `res://App/Scripts/InGameMenuController.gd`.
        
    4.  Optionally add `res://Extras/Scripts/RuntimeLogger.gd`.
        
    5.  Close the window.
        

3.  Update the project’s name.
    

    1.  Open `MainMenu.tscn`.
        
    2.  Select the `Title` node.
        
    3.  Update the `Text` to `Game Name`.
        
    4.  Save the scene.
    

4.  Point the main menu to the game scene.
    

    1.  Open `MainMenu.tscn`.
        
    2.  Select the `MainMenu` node.
        
    3.  Update `Game Scene Path` to the path of “Game Name” game scene.
        
    4.  Save the scene.
    

5.  Update the project’s inputs.
    

    1.  Open `InputOptionsMenu.tscn`.
        
    2.  Select the `Controls` node.
        
    3.  Update the `Action Name Map` to show readable names for “Game Name” input actions.
        
    4.  Update the `Add Button Texture` and `Remove Button Texture` with textures.
        
    5.  Save the scene.
        

6.  Update the game credits / attribution.
    

    1.  Copy `ATTRIBUTION_example.md` over `ATTRIBUTION.md`.
        
    2.  Update `ATTRIBUTION.md` with “Game Name” credits, following the example.
        
    3.  Reload `Credits.tscn` scene to apply changes from `ATTRIBUTION.md`.
        
    4.  Include the attribution in exports.
        

        1.  Go to Project > Export.
            
        2.  Select one of “Game Name” presets (or set them up).
            
        3.  Select the Resources tab.
            
        4.  Update `Filters to export non-resource file/folders` to include `ATTRIBUTION.md`.
            
        5.  Close the window.
   

## Links
[Attribution](ATTRIBUTION.md)  
[License](LICENSE.txt)  