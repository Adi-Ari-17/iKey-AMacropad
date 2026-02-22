# ikeyv3 — 3x3 Macropad

Simple 3x3 macropad designed by Aditya Narravula for Hack Club.

![ikeyv3 schematic and case](imgur.com image replace me!)

* Keyboard Maintainer: [Aditya Narravula](https://github.com/Adi-Ari-17)

## Contents
- Keyboard firmware (QMK): `keymaps/default/keymap.c`
- Board info: `keyboard.json`
- Case model: `case/MacropadCase.step`

## Hardware
- Keyboard: ikeyv3 (custom 3x3 PCB)
- MCU: Seeed XIAO RP2040 (RP2040)
- Pinout (as used in `keyboard.json`):
    - Columns: GP0, GP1, GP2
    - Rows:    GP3, GP4, GP5

## Build & Flash
From the root of the QMK repo (this workspace):
```bash
qmk compile -kb ikeyv3 -km default
# copy .build/ikeyv3_default.uf2 to the XIAO RP2040 when in bootloader (or use qmk flash)
```

## Bootloader / Notes
- This keyboard targets the RP2040 platform (Seeed XIAO RP2040). The `keyboard.json` uses `processor: RP2040` and `bootloader: rp2040` so QMK generates a UF2.

## Submitting to Hack Club Blueprints
- Create a GitHub repository and push this folder. Example:
```bash
git remote add origin <your-github-repo-url>
git branch -M main
git push -u origin main
```

If you want, I can create a remote repo for you (requires GitHub access/token/`gh`).
