# Icy Tower Wii

An enhanced homebrew port of the iconic 2001 PC platformer **Icy Tower** for the **Nintendo Wii** (and vWii on Wii U), featuring full controller support, customizable Tower Mods, custom character skin loading, and buttery-smooth 60 FPS gameplay.

---

## Features

- **Tower Mods Engine**: Completely transform the tower's atmosphere, platform textures, walls, background, and UI on the fly via the Options menu.
  - Easily drop your own community character skins into `sd:/apps/icytower/characters/`.
- **Comprehensive Controller Support**:
  - **Wii Remote** (held sideways with D-Pad + 2/1, or upright with A)
  - **Wii Remote + Nunchuk**
  - **Classic Controller / Classic Controller Pro**
  - **GameCube Controller** (with automatic disconnected port filtering and debounce protection)


---

## Installation Guide

> [!NOTE]
> Due to copyright reasons, this repository contains the homebrew engine, custom characters, and tower mods, but **does not distribute the original PC base game graphics and sound effects**. You must provide these files from your own legal copy of Icy Tower for PC (v1.3, v1.4, or v1.5).

### Step 1: Copy to SD Card
1. Download or clone this repository.
2. Copy the `apps` folder to the root of your SD card:
   ```
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

### Step 2: Supply Base Game Assets
1. On your PC, navigate to your installed copy of Icy Tower.
2. Copy all `.bmp` files from the PC game's `gfx` directory into `sd:/apps/icytower/gfx/`.
   - Ensure `floor01.bmp` through `floor27.bmp`, `sideblock.bmp`, `bgtile.bmp`, fonts, and the `harold/` folder are placed inside `sd:/apps/icytower/gfx/`.
3. Copy all sound files (`.wav`) from the PC game's `sfx` directory into `sd:/apps/icytower/sfx/`.

---

## Controls

| Action | Wii Remote (Horizontal) | GameCube Controller | Classic Controller |
| :--- | :--- | :--- | :--- |
| **Move Left / Right** | D-Pad Left / Right | Control Stick / D-Pad | D-Pad / Left Stick |
| **Jump** | **2** or **A** | **A** / **X** / **Y** | **b** / **a** |
| **Pause / In-Game Menu** | **+** (Plus) or **Home** | **Start** | **+** (Plus) / **Home** |
| **Menu Select** | **2** or **A** | **A** | **a** |
| **Menu Back / Cancel** | **1** or **B** | **B** | **b** |

---

## Modding & Customization

### Adding Custom Character Skins
Place any Icy Tower custom character folder into `sd:/apps/icytower/characters/`:
```
sd:/apps/icytower/characters/
└── YourCharacter/
    ├── character.txt
    ├── character.bmp
    └── sounds...
```
Navigate to **Game Options -> Character** in the main menu to select and play as your custom hero.

### Creating Tower Mods
To create or install a new Tower Mod:
1. Create a directory: `sd:/apps/icytower/mods/<ModName>/gfx/`.
2. Add your custom textures:
   - `floor01.png` - `floor27.png`: Platform pieces (`floor01` = left cap 21x37, `floor02` = center loop 16x37, `floor03` = right cap 21x37). Full 32-bit RGBA transparency is supported!
   - `sideblock.png`: Tower wall texture (132x124, vertically seamless).
   - `bgtile.png`: Background texture (546x128, vertically seamless).
   - `combo_meter.png`, `combo_liquid.png`, `combo_count.png`: Combo meter UI.
   - `harold/`: Optional theme-specific character sprites (idle, walk, jump, etc.).
3. In the main menu, go to **Options -> Tower Mod** and switch to your mod.
