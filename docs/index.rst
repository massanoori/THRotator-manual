﻿=======================================
THRotator User's Manual
=======================================

THRotator allows users to enjoy vertically-scrolling shoot 'em up games on a vertically-long monitor.
THRotator provides a way to rotate a screen and to rearrange HUD elements.

THRotator also allows users to customize HUD arrangements for a vertical screen by the following GUI.

.. |thr_sample_screenshot_en| image:: ./images/HSiFS-screenshot-en.png
.. |thr_sample_screenshot_ja| image:: ./images/HSiFS-screenshot-ja.png

|thr_sample_screenshot_en|

Background is replaced by solid gray for easy redistribution.

THRotator mainly focuses on Touhou Project and Uwabami Breakers, which shares the foundation of Touhou Project.
Possibly, you can use THRotator for other vertically-scrolling shoot 'em up games.

THRotator is not tested on Touhou 7.5, Touhou 10.5, and Touhou 12.3.
THRotator is tested only on Windows 10.

Supported products
=======================================

- the Embodiment of Scarlet Devil (Touhou 6)
- Perfect Cherry Blossom (Touhou 7)
- Imperishable Night (Touhou 8)
- Phantasmagoria of Flower View (Touhou 9)

  - Screen rotation only, not fully tested.

- Shoot the Bullet (Touhou 9.5)
- Mountain of Faith (Touhou 10)
- Subterranean Animism (Touhou 11)
- Undefined Fantastic Object (Touhou 12)
- Double Spoiler (Touhou 12.5)
- Fairy Wars (Touhou 12.8)
- Ten Desires (Touhou 13)
- Double Dealing Character (Touhou 14)

  - Tested on demo version.

- Impossible Spell Card (Touhou 14.3)
- Legacy of Lunatic Kingdom (Touhou 15)

  - Tested on demo version.

- Hidden Star in Four Seasons (Touhou 16)
- Violet Detector (Touhou 16.5)
- Uwabami Breakers

Main features
=======================================

- Rotate screen in left or right direction by pressing Alt+Left or Alt+Right key.
- Magnify screen to as large size as possible while THRotator detects that you are playing.
- Vertically-long window in windowed mode.
- If you are not satisfied by the default HUD elements (such as lives, bombs, and score), you can customize them.
- Save screen capture in BMP format on Touhou 6 by Home key.
- Fix jaggy pixels in Touhou 11, 12, 12.5, 12.8, and 13 when screen resolution of 960x720 or 1280x960 is chosen.


Notes
=====================

- Use THRotator at your own risk.
- Don't ask any question about THRotator to the game publishers.

  - Before reporting an issue to the publisher, you must first verify that the issue is independent of THRotator.

- Because THRotator forces a game to behave in a way different from the original design,
  you must pay attention to any possibilities of degrading fairness by using THRotator.

  - For example, your replay assisted by THRotator might be rejected from leaderboards, which are usually stricly fair.
  - When you share a replay or a video assisted by THRotator, it is a good choice to give credit to THRotator to let people know your gameplay is assisted by a tool.

- Don't copy ``d3d8.dll`` and ``d3d9.dll`` to your system directory.
- THRotator's behavior is undefined on games not listed in supported products.


License
======================

THRotator is under GPL v3.

`Source code (GitHub) <https://github.com/massanoori/THRotator>`_

But configuration files are in the public domain.

If you would like to build THRotator from source code or to add your own mods,
see :doc:`pages/development`.


Motivation
======================

Development of THRotator was initially inspired by Vertical Play developed by `niisaka at Tari Lari Run <http://bygzam.seesaa.net/>`_,
which is the first screen rotation tool for Touhou Project to my best knowledge.
In fact, THRotator and Vertical Play share the way how a user rotates a screen (alt+arrow keys).

But in terms of the following points, THRotator and Vertical Play are different.

Support on earlier works
-------------------------

Vertical Play provides screen rotation functionality only to works working on Direct3D 9 (Touhou 10 and later).

In addition to supporting works on Direct3D 9, THRotator also supports works built upon Direct3D 8 (from Touhou 6 to 9.5).


Future product support
-------------------------

Although I haven't seen any specific implementation of Vertical Play,
the rearrangements of HUD elements seem hard coded.
When a new title is released, users must wait for implementation by the developer.

THRotator allows users to configure how HUD elements are arranged.
Users can enjoy a new product immediately after its release with THRotator on vertically-long screen.


How user's configuration is saved
-----------------------------------

Vertical Play saves user's configuration via registry keys on Windows.

On the other hand, THRotator saves user's configuration through .ini file.



Performance
---------------

I haven't measured performance and seen implementation of Vertical Play.
But what Vertical Play does looks simply hacking transform matrix update from Touhou Project.

On the other hand, THRotator copies pixels from dummy back buffer,
which is undoubtedly more costly than just overwriting transform matrices.


Neatness of rendering
-------------------------

What THRotator does is just copying rects.
Thus noticeable pixel discontinuity appears near boundary of rects.

Vertical Play results in much cleaner rendering since it overrides draw calls with transparency.
HUD elements and background is well blended with Vertical Play.


Table of contents
======================

.. toctree::
   :maxdepth: 2

   pages/install
   pages/usage
   pages/troubleshoot
   pages/development
   pages/uninstall
   pages/releasenotes
   pages/credits
