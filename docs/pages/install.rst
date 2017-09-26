================
Install
================

This page shows the steps to install THRotator.

Download THRotator
=============================

Download the latest release from `<https://github.com/massanoori/THRotator/releases>`_.
The file named like ``THRotator-X.Y.Z.zip`` is what has to be downloaded.


Determine which DLL is needed
=============================

First, determine the target game runs on Direct3D 8 or Direct3D 9.

If the game is one of the following, the game is Direct3D 8-based.

- the Embodiment of Scarlet Devil (Touhou 6)
- Perfect Cherry Blossom (Touhou 7)
- Imperishable Night (Touhou 8)
- Phantasmagoria of Flower View (Touhou 9)
- Shoot the Bullet (Touhou 9.5)

If the game is one of the following or later, the game is Direct3D 9-based.

- Mountain of Faith (Touhou 10)
- Subterranean Animism (Touhou 11)
- Undefined Fantastic Object (Touhou 12)
- Double Spoiler (Touhou 12.5)
- Fairy Wars (Touhou 12.8)
- Ten Desires (Touhou 13)
- Double Dealing Character (Touhou 14)
- Impossible Spell Card (Touhou 14.3)
- Legacy of Lunatic Kingdom (Touhou 15)
- Hidden Star in Four Seasons (Touhou 16)
- Uwabami Breakers

If the game is Direct3D 8-based and
`DX8 to DX9 Converter <http://enbdev.com/download_convertor_dx8todx9.htm>`_ is not installed,
you need to copy ``d3d8/d3d8.dll``.

Otherwise, you need to copy ``d3d9/d3d9.dll``.

Copy DLL file
=========================

Copy DLL file to the location where the game is installed (where the .exe file exists).
Windows may ask you to input an administrator's name and password to copy the DLL file.


Copy config file
=========================

Copy config file corresponding to the game ``sample-config/<filename of executable>.throtator`` to the following directory.

For Touhou 6, 7, 8, 9, 9.5, 10, 11, 12, and alcostg
  Where the game is installed.

For Touhou 12.5, 12.8, 13, 14, 14.3, 15, and later
  Where the player's data (score, replay, screen capture, and others) is saved.

.. note:: Location of player's data
   
   - On Windows Vista, 7, 8, and 10
   
     - ``C:\Users\<user name>\AppData\Roaming\ShanghaiAlice\th<product number>\``
     - ``open-player-data-directory.bat`` opens the parent of the directory above

   - Executing command ``set APPDATA=`` before launching
   
     - Where the game is installed.

.. note:: Migration from old format

   - Don't copy new config file named as ``<filename of exe>.throtator``. THRotator tries to load ``<filename of exe>.throtator`` first.
   - Keep the installed location of ``throt.ini`` or copy your backed-up ``throt.ini`` to the location of save data.
   - Your configuration will be saved to ``<filename of exe>.throtator`` since next launch.

Localize
========================

GUI and messages are in Japanese by default.

If you copy ``d3d8/en-US`` (for  ``d3d8/d3d8.dll``) or ``d3d9/en-US`` (for ``d3d9/d3d9.dll``) folder to the same directory where DLL file exists, GUI and messages become in English.



Aspect ratio distortion by default config files
===============================================================

In order to show all digits in HUD elements,
their aspect ratios are not preserved in the following products.

- Touhou 8 (To show all digits)
- Touhou 9.5 (To show all digits)
- Touhou 12.5 (To show all digits)
- Touhou 12.8 (To show `Perfect Freeze`)
- Since Touhou 13 (To show the denominators of fragments)

