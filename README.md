# PCSX2-RR

## TEST

this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test this is a test 

MORE TESTING MORE TESTING MORE TESTING MORE TESTING MORE TESTING MORE TESTING 

## Future of this repository

PCSX2's re-recording tools have been merged into PCSX2 for quite sometime, meaning that releases will not occur here anymore. This fork will serve as a staging ground for my own personal changes and is no longer a distinct fork.

If you are interested in improving the recording tools or fixing a bug, please consider making a pull-request [on pcsx2's main repository](https://github.com/PCSX2/pcsx2), as well as directing any issues / bug reports there as well.

## Credit

This is a fork of https://github.com/DocSkellington/pcsx2-1.4.0-rr which itself is a fork of https://github.com/pocokhc/pcsx2-1.4.0-rr, which itself is based off the original [pcsx2-rr](https://code.google.com/archive/p/pcsx2-rr/). However, since the content has changed a lot and simple merging can not be done, the source code has changed considerably from this original version.

## About

This work tries to bring TAS tools to the latest version of the PCSX2 emulator.
If you have other ideas (or if you find bugs), don't hesitate to open an issue (or write a post in TASVideos' forum).

If you would like to make an improvement to the project, don't hesitate to follow the [steps to build from source](https://github.com/xTVaser/pcsx2-rr/wiki/Building-from-Source) and submit a pull request.

Have fun while creating TAS! :D

## Video Examples

Here is a simple tutorial on getting started with PCSX2-rr, note that keybindings may have changed!

- [Video Tutorial](https://www.youtube.com/watch?v=1rgJ3jowxIo)

Here are some TAS examples (made with the original pcsx2-rr v.1):

- [TAS of Chulip part0 (WIP) pcsx2-1.4.0-rr (nicovideo)](http://www.nicovideo.jp/watch/sm30385451)
- [TAS of Chulip part0 (WIP) pcsx2-1.4.0-rr (youtube)](https://youtu.be/Ib2MnRfCCzc)

## Getting the Emulator

Check the [release page](https://github.com/xTVaser/pcsx2-rr/releases) for the latest build, there is also a build for the old 1.4.0 release of pcsx2 that may be better suited for some games.  
You will need:

- The [Visual C++ 2015 x86 Redistributables](https://www.microsoft.com/en-us/download/details.aspx?id=48145)

This was tested only on Windows 10, but the application should work on the other OS supported by PCSX2.

## Features

- KeyMovie recording
- Pause/Unpause/FrameAdvance
- Lua Support
  - Lua engine keeps running when the end of the script is reached (allows to display data each frame);
- Save/Load states to/from files;
- An editor for KeyMovie files
- Virtual Pad;
  - TAS Input Manager:
    - Calls LuaManager::ControllerInterrupt
    - Reads, if it is open, the virtual pad. Be wary that the virtual pad overwrites the other sources of inputs (lua and user).

For more detail, see the wikis:

- [PCSX2-rr v3](https://github.com/pocokhc/pcsx2-1.4.0-rr/wiki) (in Japanese)
- [PCSX2-rr v4](https://github.com/DocSkellington/pcsx2-1.4.0-rr/wiki) (only explains changes)

## New shortcuts

### Activate Shortcuts for save/load

If you wish to activate the keyboard shortcuts for saving to (or loading from) a specific slot without having to manually switch the current slot to this one (so, if you don't want to use only F1, F2 and F3), here are the steps:

1. In the `PCSX2-rr_keys.ini` remove the `#` before States_SaveSlot0, States_SaveSlot1 (and so on)
2. Change the 10 into a 0 (zero)
3. In LilyPad settings, switch the Keyboard API to Raw input

### Fast Frame Advance

If you set Lilypad's Keyboard API to Raw Input (in the Plugin Settings), you will be able to hold space to "frame advance" multiple times in a row (the number of times per second should depend on your operating system's settings).

## Desync

See this [wiki page](https://github.com/xTVaser/pcsx2-rr/wiki#key-movie-creation-assumption-procedure-updated-april-9-2017)

## How to build for development (Windows 10) full details to come

See this [wiki article](https://github.com/xTVaser/pcsx2-rr/wiki/Building-from-Source)

## Current Issues (probably should just move to an issue page

### Titlebar during FrameAdvance

Had to cheat a little to force the frame counter to update in the titlebar. So, the other information displayed is not accurate (because it's not updated).

---

# PCSX2

![Windows Build](https://github.com/PCSX2/pcsx2/workflows/Windows%20Build/badge.svg)
![Linux Build](https://github.com/PCSX2/pcsx2/workflows/Linux%20Build/badge.svg)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/1f7c0d75fec74d6daa6adb084e5b4f71)](https://www.codacy.com/gh/PCSX2/pcsx2/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=PCSX2/pcsx2&amp;utm_campaign=Badge_Grade)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/6310/badge.svg)](https://scan.coverity.com/projects/6310)
[![Discord Server](https://img.shields.io/discord/309643527816609793)](https://discord.com/invite/TCz3t9k)

PCSX2 is a free and open-source PlayStation 2 (PS2) emulator. Its purpose is to emulate the PS2's hardware, using a combination of MIPS CPU [Interpreters](<https://en.wikipedia.org/wiki/Interpreter_(computing)>), [Recompilers](https://en.wikipedia.org/wiki/Dynamic_recompilation) and a [Virtual Machine](https://en.wikipedia.org/wiki/Virtual_machine) which manages hardware states and PS2 system memory. This allows you to play PS2 games on your PC, with many additional features and benefits.

## Project Details

The PCSX2 project has been running for more than ten years. Past versions could only run a few public domain game demos, but newer versions can run most games at full speed, including popular titles such as Final Fantasy X and Devil May Cry 3. Visit the [PCSX2 compatibility list](https://pcsx2.net/compatibility-list.html) to check the latest compatibility status of games (with more than 2500 titles tested), or ask for help in the [official forums](https://forums.pcsx2.net/).

The latest officially released stable version is version 1.6.0.

Installers and binaries for both Windows and Linux are available from [our website](https://pcsx2.net/download.html).

Development builds are also available from [our website](https://pcsx2.net/download/development.html).

## System Requirements

### Minimum

| Operating System                                                                                                       | CPU                                                                                                                                                                                           | GPU                                                                                                                                                                                               | RAM  |
| ---------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |
| - Windows 8.1 or newer (32 or 64 bit) <br/> - Ubuntu 18.04/Debian or newer, Arch Linux, or other distro (32 or 64 bit) | - Supports SSE4 <br/> - [PassMark Single Thread Performance](https://www.cpubenchmark.net/singleThread.html) rating near or greater than 1600 <br/> - Two physical cores, with hyperthreading | - Direct3D10 support <br/> - OpenGL 3.x support <br/> - [PassMark G3D Mark](https://www.videocardbenchmark.net/high_end_gpus.html) rating around 3000 (GeForce GTX 750) <br/> - 2 GB Video Memory | 4 GB |

_Note: Recommended Single Thread Performance is based on moderately complex games. Games that pushed the PS2 hardware to its limits will struggle on CPUs at this level. Some release titles and 2D games which underutilized the PS2 hardware may run on CPUs rated as low as 1200. A quick reference for CPU **intensive games**: [Wiki](https://wiki.pcsx2.net/Category:CPU_intensive_games), [Forum](https://forums.pcsx2.net/Thread-LIST-The-Most-CPU-Intensive-Games) and CPU **light** games: [Forum](https://forums.pcsx2.net/Thread-LIST-Games-that-don-t-need-a-strong-CPU-to-emulate)_

### Recommended

| Operating System                                                                                 | CPU                                                                                                                                                                                                       | GPU                                                                                                                                                                                                   | RAM  |
| ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |
| - Windows 10 (64 bit) <br/> - Ubuntu 19.04/Debian or newer, Arch Linux, or other distro (64 bit) | - Supports AVX2 <br/> - [PassMark Single Thread Performance](https://www.cpubenchmark.net/singleThread.html) rating near or greater than 2100 <br/> - Four physical cores, with or without hyperthreading | - Direct3D11 support <br/> - OpenGL 4.5 support <br/> - [PassMark G3D Mark](https://www.videocardbenchmark.net/high_end_gpus.html) rating around 6000 (GeForce GTX 1050 Ti) <br/> - 4 GB Video Memory | 8 GB |

_Note: Recommended GPU is based on 3x Internal, ~1080p resolution requirements. Higher resolutions will require stronger cards; 6x Internal, ~4K resolution will require a [PassMark G3D Mark](https://www.videocardbenchmark.net/high_end_gpus.html) rating around 12000 (GeForce GTX 1070 Ti). Just like CPU requirements, this is also highly game dependent. A quick reference for GPU **intensive games**: [Wiki](https://wiki.pcsx2.net/Category:GPU_intensive_games)_

### Technical Notes

-   You need the [Visual C++ 2019 x86 Redistributables](https://support.microsoft.com/en-us/help/2977003/) to run PCSX2.
-   Windows XP and Direct3D9 support was dropped after stable release 1.4.0.
-   Windows 7 and Windows 8 support was dropped after stable release 1.6.0.
-   Make sure to update your operating system and drivers to ensure you have the best experience possible. Having a newer GPU is also recommended so you have the latest supported drivers.
-   Because of copyright issues, and the complexity of trying to work around it, you need a BIOS dump extracted from a legitimately-owned PS2 console to use the emulator. For more information about the BIOS and how to get it from your console, visit [this page](https://pcsx2.net/config-guide.html#Bios).
-   PCSX2 uses two CPU cores for emulation by default. A third core can be used via the MTVU speed hack, which is compatible with most games. This can be a significant speedup on CPUs with 3+ cores, but it may be a slowdown on GS-limited games (or on CPUs with fewer than 2 cores). Software renderers will then additionally use however many rendering threads it is set to and will need higher core counts to run efficiently.
-   Requirements benchmarks are based on a statistic from the Passmark CPU bench marking software. When we say "STR", we are referring to Passmark's "Single Thread Rating" statistic. You can look up your CPU on [Passmark's website for CPUs](https://cpubenchmark.net) to see how it compares to PCSX2's requirements.

### Screenshots

![Okami](https://pcsx2.net/images/stories/gitsnaps/okami_n1s.jpg "Okami") ![Final Fantasy XII](https://pcsx2.net/images/stories/gitsnaps/finalfantasy12izjs_s2.jpg "Final Fantasy XII") ![Shadow of the Colossus](https://pcsx2.net/images/stories/gitsnaps/sotc6s2.jpg "Shadow of the Colossus") ![DragonBall Z Budokai Tenkaichi 3](https://pcsx2.net/images/stories/gitsnaps/DBZ-BT-3s.jpg "DragonBall Z Budokai Tenkaichi 3") ![Kingdom Hearts 2: Final Mix](https://pcsx2.net/images/stories/gitsnaps/kh2_fm_n1s2.jpg "Kingdom Hearts 2: Final Mix") ![God of War 2](https://pcsx2.net/images/stories/gitsnaps/gow2_s2.jpg "God of War 2") ![Metal Gear Solid 3: Snake Eater](https://pcsx2.net/images/stories/gitsnaps/mgs3-1_s2.jpg "Metal Gear Solid 3: Snake Eater") ![Rogue Galaxy](https://pcsx2.net/images/stories/gitsnaps/rogue_galaxy_n1s2.jpg "Rogue Galaxy")

Want more? [Check out the PCSX2 website](https://pcsx2.net/demo-videos-screenshots/screenshots.html).
