# ikeyv3 — 3x3 Macropad

Simple 3x3 macropad designed by Aditya Narravula for Hack Club.

<img width="364" height="338" alt="Screenshot 2026-03-12 at 6 19 18 AM" src="https://github.com/user-attachments/assets/6b69b1dc-609d-4d9a-b66e-8ae0c69ae1eb" />

I didn't know you could upload the PCB from kicad before this

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
<img width="534" height="462" alt="Screenshot 2026-02-12 at 4 58 29 PM" src="https://github.com/user-attachments/assets/28fce08f-582f-475f-830b-3938823db816" />
## Build & Flash
From the root of the QMK repo (this workspace):
```bash
qmk compile -kb ikeyv3 -km default
# copy .build/ikeyv3_default.uf2 to the XIAO RP2040 when in bootloader (or use qmk flash)
```

## Bootloader / Notes
- This keyboard targets the RP2040 platform (Seeed XIAO RP2040). The `keyboard.json` uses `processor: RP2040` and `bootloader: rp2040` so QMK generates a UF2.
