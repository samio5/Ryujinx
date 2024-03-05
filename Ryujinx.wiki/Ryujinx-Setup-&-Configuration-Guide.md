This article assumes you have already [hacked your Nintendo Switch](https://nh-server.github.io/switch-guide/) and [dumped your Nintendo Switch keys](https://github.com/Ryujinx/Ryujinx/wiki/Keys)
(prod.keys) and firmware file(s). This guide illustrates using a
properly dumped recent game cartridge as an untrimmed XCI file to
install a firmware directly to Ryujinx. It is also possible to install
firmware from a folder or ZIP file. You may also follow this [firmware dumping guide](https://github.com/Ryujinx/Ryujinx/wiki/Firmware-Dumping-Guide-(TegraExplorer-or-hbmenu-&-Goldleaf)).  

If you haven't already downloaded Ryujinx, get the latest version
from: <https://ryujinx.org/download>.  
Ryujinx checks for updates automatically at startup. You can disable this feature if you wish in Options > Settings . You may also check for updates manually by navigating to Help > Check for Updates.

## Table of Contents

[Preface](#preface)

[System Requirements](#system-requirements)

[Dependencies](#dependencies)

[Initial Setup - Placement of prod.keys](#initial-setup---placement-of-prodkeys)

[Initial Setup Continued - Installation of Firmware](#initial-setup-continued---installation-of-firmware)

[Adding Your Games to Ryujinx](#adding-your-games-to-ryujinx)

[Managing Game Updates](#managing-game-updates)

[Managing DLC](#managing-dlc)

[Managing Mods](#managing-mods)

[Managing Cheats](#managing-cheats)

[Managing User Profiles](#managing-user-profiles)

[Input Configuration](#input-configuration)

[Motion Controls](#motion-controls)

[Amiibo Emulation](#amiibo-emulation)

[Profiled Persistent Translation Cache](#profiled-persistent-translation-cache)

[Graphics Enhancements](#graphics-enhancements)

[Portable Mode](#portable-mode)

[Launch in Fullscreen](#launch-in-fullscreen)

Preface
=======

Ryujinx comes pre-optimized by default. If a particular menu option is
not mentioned in this guide, it should be ignored and should not be
changed unless directly instructed by Ryujinx staff.

***When requesting support on the Ryujinx official Discord server, you
will usually be asked for your log file. With this in mind, Logging
should be left at default settings (enabled) for everything except debug
logs. Do not enable debug logs unless specifically instructed by Ryujinx
staff.***

System Requirements
===================

In order to use *Ryujinx* your computer will need:

-   At least 8GB RAM

-   A video card/GPU that supports OpenGL 4.5 or higher, or Vulkan.

-   Your Switch keys and either your [dumped firmware](https://github.com/Ryujinx/Ryujinx/wiki/Firmware-Dumping-Guide) or recent game
    cartridge untrimmed XCI

-   Your dumped Nintendo Switch games or homebrew

-   A 64-bit Operating System

-   OS-specific dependencies installed

Dependencies
============
**Windows**
-   **Windows 10 RS4 (Redstone 4, version 1803) or newer** is required.
-   Graphics drivers must be up to date. On laptops with 2 different graphics cards, both iGPU and dGPU drivers must be updated.

**Linux**<br>
copy the command into your terminal emulator of choice and execute it
-   *Archlinux based distros:*<br>
`sudo pacman -S sdl2 openal`

-   *Ubuntu based distros:*<br>
`sudo apt-get install libsdl2-2.0 libsdl2-dev libalut-dev`

-   *Fedora:*<br>
`sudo dnf install SDL2-devel openal-soft`

**MacOS**


Initial Setup - Placement of prod.keys
======================================

**Ryujinx supports [portable mode!](#portable-mode) If you set up portable mode, note that any time the %appdata% folder is referenced in the guide below, it is referring to your custom data folder.**


1.  Now that you've downloaded the *Ryujinx* archive, open it and
    extract the contents of the publish folder onto your hard drive in
    the location of your choice.

2.  Navigate to where you extracted the *Ryujinx* files, and
    double-click on *Ryujinx.exe*. This will launch the emulator and you
    will be met with the following message (don't worry; this is
    normal!):\
    ![image](https://user-images.githubusercontent.com/62343878/86277688-5ee76b80-bb94-11ea-9c51-0f5ba153371b.png)

3.  Click *OK* on the warning box.\
    Now that *Ryujinx* has been launched, the proper folders have been
    created for you in your %appdata% folder.

4.  Click *File* at the top left of the *Ryujinx* window, and then click
    *Open Ryujinx* *Folder*.\
    ![image](https://user-images.githubusercontent.com/62343878/86277744-7b83a380-bb94-11ea-96c3-83acfbd9b534.png)

5.  Navigate down into the system subfolder and paste your prod.keys file
    here. The file/folder structure should look like this (JohnDoe
    substituted for your username):\
    ![image](https://user-images.githubusercontent.com/62343878/86277827-9d7d2600-bb94-11ea-9900-b5351364fd14.png)

6.  Close and reopen *Ryujinx* so that the prod.keys file is validated.\
    You're done installing keys!

Initial Setup Continued - Installation of Firmware
==================================================

Now that your keys are installed, it's time to install a firmware. Make
sure you have an untrimmed XCI file of a recent game cartridge you
dumped, or have compiled your [dumped firmware](https://github.com/Ryujinx/Ryujinx/wiki/Firmware-Dumping-Guide) into a ZIP file.

1.  Open *Ryujinx*. There should be no warning about KEYS.md anymore; if
    you still get the warning, go back through the prod.keys steps and
    ensure you have placed the file correctly.

2.  Now that *Ryujinx* is open, click *Tools \> Firmware \> Install from
    XCI/ZIP*\
    ![image](https://user-images.githubusercontent.com/62343878/86277870-aec63280-bb94-11ea-8932-df14c870e25c.png)\
    This brings up the "Choose the firmware file to open" window.\
    \
    ![image](https://user-images.githubusercontent.com/62343878/86277923-c69db680-bb94-11ea-99ab-2d8c7ea74e0e.png)

3.  Using the *Ryujinx* window, navigate to the location of your dumped
    XCI file and click *Open*. You will be asked to confirm whether you
    want to install the firmware. Make sure your prod.keys are at least
    as new as the firmware you are installing!\
    (Your firmware version number may vary)\
    \
    ![image](https://user-images.githubusercontent.com/62343878/86277970-db7a4a00-bb94-11ea-9142-2616ed6e742b.png)

4.  Click *Yes*. You will see a message that the firmware is
    installing:\
    \
    ![image](https://user-images.githubusercontent.com/62343878/86278026-ee8d1a00-bb94-11ea-98ab-a45d9d4ca48c.png)
\
    \
    and was successfully installed:\
    ![image](https://user-images.githubusercontent.com/62343878/86278058-fcdb3600-bb94-11ea-861f-866a13dbefdb.png)

5.  Click *OK*. If all went well, you will now see your firmware version
    listed as the "System Version" in the bottom right hand corner of
    the main *Ryujinx* window.\
![image](https://user-images.githubusercontent.com/62343878/86278217-4035a480-bb95-11ea-9803-fabc39dbec5b.png)

Adding Your Games to Ryujinx
============================

You have keys and firmware ready to go. Time to add your games!

With *Ryujinx* open, click on *Options \> Settings*. This takes you
straight to the *General* tab.\
![image](https://user-images.githubusercontent.com/62343878/86278362-7c690500-bb95-11ea-9667-cb61e7d45b8e.png)

There are two different methods in which you can add a Game Directory in this window.\
\
**1st Method:**\
Type the absolute path of the folder containing your games into the path
field and click *Add*.\
![image](https://user-images.githubusercontent.com/62343878/86278453-a6bac280-bb95-11ea-8bb0-005e89dbb295.png)\
\
**2nd Method:**\
Without typing anything into the path field, click *Add*.\
![image](https://user-images.githubusercontent.com/62343878/86278489-b76b3880-bb95-11ea-929c-da8b53052406.png)\

\
This brings up the navigation window. Navigate to the folder containing
your games (e.g. D:\\Switch Games) and click *Add*.\
![image](https://user-images.githubusercontent.com/62343878/86278572-d5d13400-bb95-11ea-98e6-91a58667a538.png)

1.  Whichever method you chose, **click *Save*** to save the game
    directory setting.

2.  Your games will now show up in the main *Ryujinx* window.\
    ![image](https://user-images.githubusercontent.com/62343878/86278608-e7b2d700-bb95-11ea-8b2c-f12b1b7f0fcc.png)

Managing Game Updates
=====================

Manage game update versions from within Ryujinx

Now that your games are added, you may wish to update your game for
various reasons e.g. bugfixes, new content, etc. *Ryujinx* has built-in
functionality to manage which version of the game you want to play.

1.  In the main *Ryujinx* game list right-click the game you want to
    apply an update to. Then click *Manage Title Updates*.\
    ![image](https://user-images.githubusercontent.com/62343878/86278648-fef1c480-bb95-11ea-8a28-6099f5e0c8bf.png)\
    \
    After clicking *Manage Title Updates*, you will see the *Ryujinx --
    Title Update Manager* menu.

2.  In the *Ryujinx -- Title Update Manager* menu, click *Add*.\
    ![image](https://user-images.githubusercontent.com/62343878/86278688-0d3fe080-bb96-11ea-8aae-f353f2dc952d.png)

3.  Clicking *Add* will bring up the navigation menu. Navigate to the
    location of your game's update files and select update you want to
    add to *Ryujinx*, and click *Add*.\
   ![image](https://user-images.githubusercontent.com/62343878/86278723-16c94880-bb96-11ea-972f-bb1c8683ed6d.png)\
    This will bring you back to the *Ryujinx -- Title Update Manager*
    window. You may repeat this for any other game version update files
    you wish to add to *Ryujinx*.

4.  In the *Ryujinx -- Title Update Manager* window, select the version
    of the update you wish to be applied to the game and click *Save*.\
    ![image](https://user-images.githubusercontent.com/62343878/86278755-22b50a80-bb96-11ea-9c1c-c4fc13a0e4cb.png)

5.  Verify that the proper version number is shown in the main *Ryujinx*
    games list window.\
    ![image](https://user-images.githubusercontent.com/62343878/86278789-2e083600-bb96-11ea-9b55-816a81b53601.png)\
    \
    Your game update has now been applied, and you may repeat the
    process for any other games you wish to apply updates to.

Managing DLC
============

Manage Downloadable Content for your games

Some games have downloadable content available that you may wish to add
to your game. *Ryujinx* has built-in functionality to add & manage your
DLC.

1.  With *Ryujinx* open, right-click on the game you want to add or
    manage DLC for and click *Manage DLC* to bring up the *Ryujinx - DLC
    Manager* window.\
    ![image](https://user-images.githubusercontent.com/62343878/86278819-37919e00-bb96-11ea-93cb-0a266c0c1b24.png)

2.  Within the *Ryujinx -- DLC Manager* window, click *Add* to open the
    DLC navigation screen.\
    ![image](https://user-images.githubusercontent.com/62343878/86278847-40826f80-bb96-11ea-99bf-05c22af2c680.png)

3.  Navigate to the location of the DLC file(s) you wish to apply, then
    double-click the file to automatically add it. Or you may select the
    file or files, and click *Add*.\
    **Note: you may add more than one DLC file at a time!**\
    ![image](https://user-images.githubusercontent.com/62343878/86278879-5001b880-bb96-11ea-9fb3-859efbd631f9.png)

4.  You will now see your DLC in the *Ryujinx - DLC Manager* window.
    **Click *Save*** to save your configuration.\
    ![image](https://user-images.githubusercontent.com/62343878/86286616-08822900-bba4-11ea-838e-eaf95c98d6dc.png)\
    \
    **Note: always drill down to see the proper status of the DLC .nca file you are managing. Checking and unchecking the .nca file is the way to enable and disable the DLC. The parent container (.nsp file) shows unchecked by default, even if the DLC is enabled.**  

Repeat this process, if you wish, for any other games you would like to manage DLC for.

Managing Mods 
============
Quick Start Guide for managing mods

Various game mods are available from enthusiasts & content creators online. _Ryujinx_ supports the following types of mods:
1. ExeFS Partition Replacement
2. ExeFS File Replacement
3. ExeFS Patching
4. RomFS Partition Replacement
5. RomFS File Replacement

**For an in-depth explanation of the mods implementation & advanced usage options in _Ryujinx_, check the description in the original PR [here](https://github.com/Ryujinx/Ryujinx/pull/1249)**.

To enable mods:

1. With _Ryujinx_ open, right-click on the game you wish to manage mods for and click _Open Mods Directory_.

![image](https://user-images.githubusercontent.com/62343878/87058158-f9fbc900-c1c4-11ea-8dcd-7bea51fc71e6.png)

This will open the `AppData\Roaming\Ryujinx\mods\contents\<game ID>\` folder.

2. Create a subfolder under the game id folder with an appropriate name conveying the mod you will be using. For instance, you might name the folder "Lana" if you were using a mod to add a Lana skin to Mario Kart 8 Deluxe.

![image](https://user-images.githubusercontent.com/62343878/87060018-3d573700-c1c7-11ea-82f8-3a54c788490c.png)

3. Copy your mod's romfs folder or exefs folder into the new folder you created.

![image](https://user-images.githubusercontent.com/62343878/87071634-b3fc3080-c1d7-11ea-8a28-a1aa86009f5c.png)

Mods can also be placed in the `AppData\Roaming\Ryujinx\sdcard` folder if the mod has been packaged for real hardware (usually indicated with an "atmosphere" folder as the top directory). With _Ryujinx_ open, right-clicking on the game you wish to manage SD mods for and clicking _Open Atmosphere Mods Directory_ will open the `AppData\Roaming\Ryujinx\sdcard\atmosphere\contents\<game ID>` folder where the romfs/exefs folders are located.

![image](https://user-images.githubusercontent.com/44103205/156943587-5242ccda-d74d-4d2f-8446-a1941beb4c2c.png)
![image](https://user-images.githubusercontent.com/44103205/156943543-ea49ec82-57b7-46eb-a12e-5daf64b1cad5.png)

Managing Cheats
===============

Ryujinx now has native cheats/runtime mods support!  
It implements full support Atmosphere style cheats (except game pausing/resume): 
https://github.com/Atmosphere-NX/Atmosphere/blob/master/docs/features/cheats.md

## Installation of Atmosphere Cheats

Two good places to acquire Atmosphere cheats are:

- https://github.com/WerWolv/EdiZon_CheatsConfigsAndScripts/tree/master/Cheats (general switch cheats)
- https://yuzu-emu.org/wiki/switch-mods/ (emulator-specific mods such as high FPS, ultrawide, etc...)

Inside the cheat `zip`, `rar`, or other archive format, there is usually a file structure like this:

```
Cheat_Name\cheats\0123456789ABCDEF.txt
```

Where `0123456789ABCDEF` will vary according to the game and the cheat (this is the build id of the executable the cheat attaches itself to). A cheat can also contain several `txt` files. **Cheats are game-specific and version-specific, they will not work if transferred from one game to another or to an incompatible update of the game.**

To install the cheat: 

- Open Ryujinx, right-click the game you wish to install the cheat and select to open its `Mod directory`;
- A directory like this will open: `Ryujinx\mods\contents\XXXXXXXXXXXXXXXX\`, `XXXXXXXXXXXXXXXX` will be the id of the chosen game;
- Extract the cheat archive to the mod directory, keeping the cheat name: `Ryujinx\mods\contents\XXXXXXXXXXXXXXXX\Cheat_Name\cheats\<all the txt files>`.

## Activating/Deactivating cheats

Currently, all cheats are automatically enabled and cannot be disabled, so mixing, for instance, 60, 90 and 120 fps cheats may cause a conflict. 

One alternative is to create a directory `disabled_cheats` in the mod directory and move all unused cheats there. Another one is to prepend something to the file name, for instance `off_0123456789ABCDEF.txt` as a valid cheat must not have anything but `0123456789ABCDEF.txt` in its name.

The .txt files can also contain several cheats that may conflict. To switch off individual cheats inside a .txt file first **backup the .txt file** to something like `bak_0123456789ABCDEF.txt` (this will also prevent the backup to be loaded as a cheat). Next, in the .txt file, there will be sections, each with a name within `[ ]` brackets and filled with sequences of letters and numbers (the code of the cheat), for instance:

```
[New Super Mario Bros. U Deluxe]

[Start with 99 Lives]
58000000 00CC9860
78000000 0002A1C0
61000000 00000000 00000063

[Time = 999]
58000000 00C88A70
78001000 00000090
64000000 00000000 003E6F00

[Start as Penguin]
58000000 00CC9860
78000000 0002A1C4
61000000 00000000 00000005
```

To disable the time cheat, just remove its section and the code:

```
[New Super Mario Bros. U Deluxe]

[Start with 99 Lives]
58000000 00CC9860
78000000 0002A1C0
61000000 00000000 00000063

[Start as Penguin]
58000000 00CC9860
78000000 0002A1C4
61000000 00000000 00000005
```

Managing User Profiles
=====================

Ryujinx offers the ability to use multiple, customizable user profiles. **WARNING:** Save data is specific to each user profile so if you delete a profile, the save data under that profile is also deleted.

### To edit a user profile:  
1. With Ryujinx open, but no game running, click on Options > Manage User Profiles  
![image](https://user-images.githubusercontent.com/62343878/115936775-62b1ea80-a453-11eb-9df8-5d39cf414057.png)

Now in the Manage User Profiles window, you will see the default RyuPlayer profile. This is the default profile that comes with Ryujinx and **cannot be deleted** as it contains all of the original save data for your games. You may, however, rename it and change the picture to something else, if you like.  
![image](https://user-images.githubusercontent.com/62343878/115936853-98ef6a00-a453-11eb-9bdb-2b2076ff529d.png)  

2. To rename a profile, simply select it and type in the new text.  
![image](https://user-images.githubusercontent.com/62343878/115936950-e1a72300-a453-11eb-9d5d-027826457759.png)  

3. To change the profile image, select the profile in the list and click **Change Profile Image**.  
![image](https://user-images.githubusercontent.com/62343878/115937027-10bd9480-a454-11eb-977a-2afdec837dab.png)  

You will then be prompted to select from either a custom image, or from one of the many avatars provided in the firmware.  
![image](https://user-images.githubusercontent.com/62343878/115937083-2df26300-a454-11eb-95de-7db4a12aaa45.png)

If you choose to import an image: supported formats are `png`, `bmp`, and `jpg`. You can use the image you want, but it will be resized to 256x256 pixels, so using a square image is recommended.

If you choose to use a built-in firmware avatar, click on **Select Firmware Avatar**  

In the Manage Accounts - Avatar window, select the avatar you want, and choose a background color. When finished, click **Choose** to make it the profile's image.
![image](https://user-images.githubusercontent.com/62343878/115937295-df919400-a454-11eb-90ac-f31263ec543e.png)

![image](https://user-images.githubusercontent.com/62343878/115937710-b7566500-a455-11eb-905c-c748e8baeae8.png)

### To add a new profile:

1. With Ryujinx open, but no game running, click on Options > Manage User Profiles  
![image](https://user-images.githubusercontent.com/62343878/115936775-62b1ea80-a453-11eb-9df8-5d39cf414057.png)

2. Click on the **Add New Profile** button at the bottom left corner of the window.  

![image](https://user-images.githubusercontent.com/62343878/115938010-8a568200-a456-11eb-8a1b-a610fd8f5c7e.png)  

3. A window will pop up asking you to name the new Profile. Enter the desired name of the new profile, and click OK.  

![image](https://user-images.githubusercontent.com/62343878/115938038-9e9a7f00-a456-11eb-8464-3855cde7241d.png)

4. You will now be prompted to choose the profile image. Follow step 3 from the user profile editing instructions above.  

![image](https://user-images.githubusercontent.com/62343878/115938416-c9390780-a457-11eb-9761-eff2e0dd5efa.png)

That's it!

Input Configuration
===================

Setting up your controls: this part requires close attention, so read
carefully!

1.  Plug in the controller(s) that you will be using.

2.  Open *Ryujinx* and navigate to *Options \> Settings*\
    !![image](https://user-images.githubusercontent.com/62343878/86278975-7aec0c80-bb96-11ea-897f-9a4ed393f3b0.png)

3.  You will now see the *Ryujinx - Settings* window. Click on the
    *Input* tab.\
    ![image](https://user-images.githubusercontent.com/62343878/86278991-82abb100-bb96-11ea-9a00-adacae14b34c.png)

Before proceeding to configure anything, the options on the Input page
need some explanation:

*Direct Keyboard Access*: checking this box emulates a real, physical
keyboard being directly connected to a Nintendo Switch via USB. ***Do
not check this box unless you have a specific reason***

*Enable Docked Mode*: checking this box emulates the Nintendo Switch
being docked. Docked Mode enables higher resolution, higher FPS, and
better graphical fidelity on games that support these features.\
**If you check this box, you will need to click configure under Player**
**1 (top left menu item)**\
**If you leave this box unchecked, you will need to click configure under**
**Handheld (bottom right menu item)**\


4.  Click *Configure* under *Player 1* if you have enabled *Docked
    Mode*, or click configure *Handheld* if you have not enabled *Docked
    Mode*.\
    ![image](https://user-images.githubusercontent.com/62343878/86279008-8d664600-bb96-11ea-9ed3-32034ad9f53a.png)

5.  You should now be in the *Ryujinx -- Controller Settings* screen.
    Click on the *Input Device* dropdown and choose the *Xinput
    controller*. If you have connected multiple controllers, choose the
    one you want to be configured to be P1 in game. **If you do not see**
    **any Xinput controllers in the list, you will need to use an Xinput**
    **wrapper/translator such as**
    [x360ce](https://www.x360ce.com/).\
    ![image](https://user-images.githubusercontent.com/62343878/86279068-a969e780-bb96-11ea-913c-6da064e6d7a6.png)
    

6.  After selecting your Xinput controller you should now see a full
    mapping UI. If you want to map the buttons in a standard
    Xinput-compatible fashion, there is no need to individually map the
    buttons. Simply click on the empty *Profile* dropdown, select
    *Default*, and click *Load*. This populates the buttons with preset
    mappings for your Xinput-compatible (or Xinput wrapped/translated)
    controller. Otherwise, click on "*Unbound*" for each button you want
    to map, then press the actual button on your controller that you
    want for the Nintendo Switch controller button you've
    chosen.
![image](https://user-images.githubusercontent.com/62343878/86279165-d1f1e180-bb96-11ea-9d77-b9c029ce5b3a.png)
    \
    You may continue tweaking the settings to your liking, or binding
    each button from scratch if you want a fully custom button layout.\
    **NOTE: while the default *Deadzones* are 0.10, we recommend
    increasing your *Deadzones* to at least 0.20 in order to avoid
    unwanted joystick drift.**

If you are in *Docked Mode* and have additional controllers to
configure, configure them now under Player 2, Player 3, and so on.

7.  ***Click Save to save your configuration.***

Alternately, you may skip the input UI and edit your config.json file
found in %appdata%\\ryujinx\\

Motion Controls
===============
### Motion Controls

Ryujinx offers the ability to use motion controls with motion-enabled controllers such as a Switch Pro Controller, Joycons, Playstation DS4, smartphones with motion support, Steam controller, and others.

To use motion controls in Ryujinx:

1. Launch & configure your favorite cemuhook server application (Betterjoy, DS4Windows, Steam Gyro, etc.) with your bluetooth or wired motion-enabled controller. Leave the application running.

2. In Ryujinx, navigate to Options > Settings > Input tab and select which controller you are configuring. Remember: if you are in docked mode, configure Player 1. If you are in Handheld mode, configure the Handheld controller.

  ![image](https://user-images.githubusercontent.com/62343878/92328779-5c841080-f020-11ea-80a1-af54341c4deb.png)

3. Select your motion controller from the dropdown. It will be listed as "Xinput controller". 

  ![image](https://user-images.githubusercontent.com/62343878/92328812-9ead5200-f020-11ea-88f4-706c8f2bd5b6.png)

4. Configuration options:

- If you have already configured your controller's input buttons to your liking and only need to configure motion controls, check the "Enable Motion Controls" box and fill in the following information:  

**Controller Slot:** the controller slot # your motion controller is configured as in your cemuhook server application. Default is "0"
**Gyro Sensitivity:** 100% (you may adjust this to suit)
**Server Host:** the IP address of the computer being used to host the cemuhook server. 127.0.0.1 is localhost/the same computer running Ryujinx.
**Server Port:** 26760

![image](https://user-images.githubusercontent.com/62343878/92329071-542cd500-f022-11ea-9aff-9b1e22f29b61.png)

- Alternately, you can simply click on the empty Profile dropdown, select Default, and click Load. This populates the buttons with preset mappings and also fills in the motion control settings with recommended defaults. You may continue tweaking the settings to your liking, or binding each button from scratch if you want a fully custom button layout.

**NOTE: while the default Deadzones are 0.10, we recommend increasing your Deadzones to at least 0.20 in order to avoid unwanted joystick drift.**
Make sure to check the "Enable Motion Controls" box!

  ![image](https://user-images.githubusercontent.com/62343878/92328941-740fc900-f021-11ea-9663-ee1eeee47cee.png)

- Paired Joycons extra options:

If you set your controller type to Joycon Pair, an option called "Mirror Input" becomes available. This is useful for games in which both Joycons are connected to a Joycon grip and are moving together. If you enable this checkbox, the first Joycon's motion will be used for both Joycons.

  ![image](https://user-images.githubusercontent.com/62343878/92338812-00e17380-f070-11ea-9090-e94abe4d1134.png)


5. Click Save to save your configuration.

Repeat steps 2 through 5 for any other motion controllers you wish to configure. If you have more than one, make sure to choose the respective slot # for each controller!

Amiibo Emulation
================

All Amiibo are able to be virtually scanned within the emulator, as long as you are actively connected to the internet. No files or dumps are required!

**To scan an Amiibo:**
1. While playing a game that supports Amiibo, either navigate to the area where Amiibo scanning is expected, or press/hold the correct button to enable the Amiibo scan prompt (this site has a basic list of supported games and what benefits are provided by each: https://amiibo.life/games  
2. Click the "Actions" menu header, then click "Scan an Amiibo"  
![unknown1](https://user-images.githubusercontent.com/4905390/111011795-d82d9400-839a-11eb-8798-c426fe5bc973.png)  
3. Choose the Amiibo you want from the Amiibo Series and Character dropdowns. Note: only the Amiibo that have content for the game you are currently playing are shown in this window. All the same, if you'd like to see all Amiibo you may check the box that says "Show All Amiibo".  
  ![unknown2](https://user-images.githubusercontent.com/4905390/111011810-e8de0a00-839a-11eb-8a5c-d03b0e094ec4.png)  
**Addendum:** In The Legend of Zelda: Breath of the Wild, you may continually scan Amiibo as many times as you wish by checking the box labeled "Hack: Use Random Tag Uuid" box.

Profiled Persistent Translation Cache
=====================================

Speed up game loading times with PPTC

In a nutshell, this feature caches translated functions so that they do
not need to be translated every time the game loads. This results in a
significant reduction of load times \--the amount of time between
launching a game and arriving at the title screen\-- for nearly every
game.

**NOTE: You must launch the game at least twice and let it load**
**to the title screen or beyond before performance improvements are**
**unlocked on the third launch! These improvements are permanent and do**
**not require any extra launches going forward.**

PPTC (Profiled Persistent Translation Cache) is now enabled by default. To disable it:

1.  With *Ryujinx* open, click on *Options \> Settings*\
    ![image](https://user-images.githubusercontent.com/62343878/86279303-082f6100-bb97-11ea-92bc-68f24612d7e2.png)
    

2.  Then navigate to the *System* tab and **uncheck the box** marked
    *Enable Profiled Persistent Translation Cache*\
    ![image](https://user-images.githubusercontent.com/62343878/86279433-3b71f000-bb97-11ea-8bd2-0435ba8ece33.png)

From time to time you may wish to examine or purge your PPTC cache files if you are experiencing PPTC-related issues.

To open the PPTC cache file location:
1.  With Ryujinx open, right-click the game in the game list whose PPTC cache files you wish to view. This will bring up a pop-up menu.

2.  Navigate to _Cache Management_ > _Open the PPTC directory_

    ![image](https://user-images.githubusercontent.com/62343878/86624278-486c5600-bf80-11ea-9de5-47340af14a0c.png)

To purge the PPTC cache files:
1.  With Ryujinx open, right-click the game in the game list whose PPTC cache files you wish to purge. This will bring up a pop-up menu.

2.  Navigate to _Cache Management_ > _Purge the PPTC cache_

    ![image](https://user-images.githubusercontent.com/62343878/86625047-ac434e80-bf81-11ea-9dd7-7f3465f8c0d2.png)

Graphics Enhancements
=====================

*Ryujinx* offers a few graphics enhancement options.

1. _Resolution Scaling_, which offers a much sharper image with little to no impact to performance. Resolution scaling can increase image quality much more noticeably than Anisotropic Filtering. Ryujinx's resolution scaling implementation allows native, 2x, 3x, 4x, or even custom ratios for upscaling.

2. _Anisotropic Filtering_, which can visibly improve graphic quality.
[Wikipedia says](https://en.wikipedia.org/wiki/Anisotropic_filtering):\
_In layman\'s terms, anisotropic filtering retains the \"sharpness\" of_
_a texture normally lost by MIP map texture\'s attempts to avoid_
_aliasing. Anisotropic filtering can therefore be said to maintain crisp_
_texture detail at all viewing orientations while providing fast_
_anti-aliased texture filtering._

3. _Shader Cache_, which stores onto disk the shaders that have already been compiled, negating the need to compile them again. This feature is highly sought after as it significantly reduces stuttering and FPS drops on subsequent plays of a particular game making for a smoother, more enjoyable gameplay experience. **Note: Shader Cache is enabled by default.**

4. _Aspect Ratio Options_, which allow you to adjust the width-to-height ratio to your liking. **Note: these options may give your game a stretched or squeezed appearance unless you are using mods that change the expected aspect ratio of the game.**

**To enable _Resolution Scaling_:**\
**Note: Enabling this feature may cause graphical glitches on some games.**\
**These settings may be changed in-game on the fly! On a standard 1080p display, 2x resolution scaling is recommended.**

1. With *Ryujinx* open, click *Options \> Settings*\
   ![image](https://user-images.githubusercontent.com/62343878/86672580-078e3480-bfb4-11ea-8c01-86b05066a4dc.png)
2. Navigate to the *Graphics* tab and click the dropdown next to Resolution Scale. Select your desired level of resolution scaling.\
   ![image](https://user-images.githubusercontent.com/62343878/86673437-e7ab4080-bfb4-11ea-86de-876d7563f6a2.png)
   \
   **Click *Save*** to save the enhancement setting.

**To enable _Anisotropic Filtering_:**

**Note: enabling this feature may cause graphical glitches on some**
**games.**

1.  With *Ryujinx* open, click on *Options \> Settings*\
    ![image](https://user-images.githubusercontent.com/62343878/86279490-547aa100-bb97-11ea-97ad-549534e9d635.png)
    

2.  Navigate to the *Graphics* tab and click the dropdown next to
    *Anisotropic Filtering*. Set it to your desired level.\
    ![image](https://user-images.githubusercontent.com/62343878/86279552-6ceabb80-bb97-11ea-8b88-1e19983ed890.png)
    \
    **Click *Save*** to save the enhancement setting.

**To Manage _Shader Cache_:**  
**Shader Cache is enabled by default**. There are no good reasons to disable it other than for testing purposes. 

Disabling this setting is strongly discouraged. However, if you absolutely must disable it:
1. With Ryujinx open, navigate to _Options > Settings_.

2. Navigate to the Graphics tab and disable shader cache by unchecking the box marked "Enable Shader Cache"


In some rare cases, a shader cache might become corrupted and crash when compiling shaders on boot. To solve this you'll have to purge the shader cache for that particular game:
1. Right click on a game in the game list and navigate to Cache Management > Purge Shader Cache.

   ![image](https://user-images.githubusercontent.com/62343878/98551756-e76ccb80-225a-11eb-83b8-ce99b712e7d6.png)


To view the shader cache directory for a particular game:
1. Right click on a game in the game list and navigate to Cache Management > Open Shader Cache Directory.

   ![image](https://user-images.githubusercontent.com/62343878/98551866-0ec39880-225b-11eb-8380-967c97bfd97f.png)

To adjust your aspect ratio:  

**Option 1:**
- With Ryujinx open, navigate to Options > Settings and click on the Graphics tab. Click on the Aspect Ratio dropdown and adjust the ratio to your liking.
![image](https://user-images.githubusercontent.com/62343878/102350497-3f85a480-3f62-11eb-95b2-c9ef3d468315.png)

**Option 2:**  
- With your game running, click on the aspect ratio button in the status toolbar at the bottom of the Ryujinx window.  
![image](https://user-images.githubusercontent.com/62343878/102351140-3517da80-3f63-11eb-8d14-a2c1fc9bfd5d.png)

**Option 3:**  
1. Use Option 1 and select "Stretch to Fit Window" or Option 2 and select "Stretched".

2. Simply click and drag your window borders to the size you want!

Portable Mode
=============

If you wish, you may use a custom folder location for all Ryujinx data (as opposed to keeping it in its default location: %appdata%). This is done via the command-line or, more conveniently, a custom shortcut. In the future, the ability to configure custom data folders may be added to the GUI.

**NOTE: You must manually create the custom folder first before using portable mode! After enabling portable mode, you will need to copy your prod.keys file and any desired game data/save data from its original location to the new data folder.**

To enable *Portable Mode*  

**Option 1: (Recommended)** Create a "portable" subfolder
1. Create a subfolder in the Ryujinx program base directory called "portable". This automatically enables portable mode and utilizes this "portable" folder for system folder contents (keys, firmware, PPTC/shader caches, etc.).  
![image](https://user-images.githubusercontent.com/62343878/111225959-14811000-85a6-11eb-9ffa-a8d2f5d899cd.png)

**Option 2:** Command-line
1. Open a command prompt, navigate to the location of the Ryujinx executable and type the following command: ryujinx.exe -r d:\[folderpath]. For example, if your custom folder was d:\ryujinxdata, your command would be the following, without quotes (_THIS IS ONLY AN EXAMPLE. USE WHATEVER CUSTOM FOLDER NAME YOU PREFER_):
"ryujinx.exe -r d:\ryujinxdata"

   ![image](https://user-images.githubusercontent.com/62343878/91670371-0ec84f00-eada-11ea-9e0a-034ff6eee440.png)

The command prompt window will become the console window when Ryujinx launches.

**Option 3:** Custom Shortcut

1. Right-click on your Ryujinx executable and click Send To -> Desktop Shortcut

   ![image](https://user-images.githubusercontent.com/62343878/91670437-bf365300-eada-11ea-8bde-ce0b1cb7aa73.png)

2. Locate the new shortcut on your desktop and right-click on it, then click Properties

   ![image](https://user-images.githubusercontent.com/62343878/91670516-8fd41600-eadb-11ea-8eb3-acfb97d64c65.png)

3. In the Properties window, click into the Target field and add a space onto the end of the existing command. Then add "-r [folderpath]" without quotes where [folderpath] is your own custom data folder full path, and click OK. For example, if your custom data folder was d:\ryujinxdata, the addition you would paste into the target field would be "-r d:\ryujinxdata" without the quotes.

   ![image](https://user-images.githubusercontent.com/62343878/91670585-315b6780-eadc-11ea-8534-244a46eb1536.png)

Note: On MacOS, the command would be as follows, without the quotes:
"/Applications/Ryujinx.app/Contents/MacOS/Ryujinx -r /path/to/custom/ryujinx/folder"

You can now use this shortcut any time you want to launch Ryujinx in portable mode!

Launch in Fullscreen
====================

Ryujinx can automatically launch games in fullscreen mode. You can enable this functionality in one of two ways:

**Method One:** In Ryujinx, click on Options, then check the box marked "Start Games in Fullscreen Mode".

   ![image](https://user-images.githubusercontent.com/62343878/100805553-173b6900-33ec-11eb-9702-71626f67f6e3.png)

**Method Two:** If you launch Ryujinx from the commandline, add a --fullscreen option. Like so:

  ![image](https://user-images.githubusercontent.com/62343878/100806049-03dccd80-33ed-11eb-88a4-d5a56ada8bb0.png) 