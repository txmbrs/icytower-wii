# Icy Tower Wii

An enhanced homebrew port of the iconic 2001 PC platformer **Icy Tower** for the **Nintendo Wii** (and vWii on Wii U), featuring full controller support, customizable Tower Mods, custom character skin loading.


> [!WARNING]
> This repository does not include the original Icy Tower graphics and sound files. You must provide them from a legally obtained copy of the original PC game.

## Features

- Wii and vWii support
- Wii Remote, Nunchuk, Classic Controller, and GameCube Controller support
- Custom character skins
- Custom tower themes and visual mods
- Support PNG and MP3 files 

## Requirements

- Nintendo Wii or Wii U in vWii mode, Dolphin
- SD card
- Homebrew Channel
- A legal copy of the original PC version of Icy Tower

## Installation

### 1. Copy the app to your SD card

Clone or download this repository, then copy the `apps` folder to the root of your SD card:

```text
sd:/
└── apps/
    └── icytower/
        ├── boot.dol
        ├── meta.xml
        ├── icon.png
        ├── splash.png
        ├── characters/
        ├── gfx/
        ├── mods/
        └── sfx/
```

### 2. Add the original game assets

From your original PC installation of Icy Tower:

- Copy the required `.bmp` files into `sd:/apps/icytower/gfx/`
- Copy the required `.wav` files into `sd:/apps/icytower/sfx/`

This project expects the standard original game files such as:

```text
gfx/
├── floor01.bmp
├── floor02.bmp
├── ...
├── floor27.bmp
├── sideblock.bmp
├── bgtile.bmp
├── harold/
└── ...
```

## Controls

| Action | Wii Remote | GameCube | Classic Controller |
| --- | --- | --- | --- |
| Move left/right | D-Pad | Stick/D-Pad | Stick/D-Pad |
| Jump | 2 or A | A / X / Y | A / B |
| Pause/Menu | + or Home | Start | + or Home |
| Select | 2 or A | A | A |
| Back/Cancel | 1 or B | B | B |

## Custom Characters

Place character folders in:

```text
sd:/apps/icytower/characters/
```

Example:

```text
characters/
└── MyCharacter/
    ├── character.txt
    ├── character.bmp
    └── sounds/
```

Then open the in-game options menu and select the character.

## Tower Mods

Mods are placed in:

```text
sd:/apps/icytower/mods/
```

Each mod can include custom textures for platforms, walls, backgrounds, and UI elements. Example:

```text
mods/
└── MyMod/
    └── gfx/
        ├── floor01.png
        ├── floor02.png
        ├── sideblock.png
        ├── bgtile.png
        └── combo_meter.png
```

Activate the mod from the in-game options menu.


## Credits

- Original game: Icy Tower by Free Lunch Design
- Wii port and enhancements: txmbrs

## Disclaimer

This project is an unofficial homebrew port and is not affiliated with, endorsed by, or sponsored by the original copyright holders. Created only for testing purpose.

Do not distribute copyrighted game assets without permission.
