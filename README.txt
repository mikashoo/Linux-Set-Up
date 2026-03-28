If you are looking for the script where you actually switched the theme to "style-1," that is handled by the launch scripts.

Based on your file list, these are the exact locations of the files that determine which layout style is used:
1. For the App Launchers (Search Engine)

The file that tells Rofi to use "style-1" is located here:

    Path: ~/.config/rofi/launchers/type-1/launcher.sh

    What's inside: This script contains a line like theme='style-1'. If you change it to style-2, the whole look changes.

2. For the Applets (Settings/Quicklinks)

The files that control the "style" for your applets are located in the bin folder:

    Paths: * ~/.config/rofi/applets/bin/apps.sh

        ~/.config/rofi/applets/bin/quicklinks.sh

    What's inside: These scripts define the type and style. You likely changed a line in here to point to type-1 and style-1.

3. The Global "Active" Script

There is also a shortcut script that usually sits in the scripts folder which triggers these:

    Path: ~/.config/rofi/scripts/launcher_t1

    What it does: This is the execution bridge that calls the launcher script mentioned in step 1.
