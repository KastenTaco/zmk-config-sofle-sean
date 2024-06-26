Sean's Sofle Keyboard
=============== 

Happy Birthday, Sean.

Thi is the repository to your brand new [Sofle]([https://holykeebs.com/products/span](https://github.com/josefadamcik/SofleKeyboard), a split wireless
mechanical keyboard. Your keyboard is a wireless variant of the original Sofle. It is based off the Sofle RGB's design: [SofleChocWireless]https://github.com/db-ok/SofleChocWireless(https://github.com/josefadamcik/SofleKeyboard)

 * QWERTY base layout
 * 3-layer configuratioon
 * OLED Screens
 * Per Key LED Lighting


## Keyboard

![keyboard image](img/seankeeb.jpg)

## Case
The files for the case can be found within the repository. The pcb sits flush to the upper edge of the case. I've added some standoffs to screw the PCB on with M2x4 screws. Ideally you'd use 5 per side, 4 will do just fine as well. 
Just note that cutouts are for cosmetic purposes only.

![keyboard image](img/spankeebback.jpg)

## Keymap

![keymap image](img/span.svg)


## Building

Either generate the firmware via the GitHub action, or build locally by setting
up the ZMK toolchain as described [here](https://zmk.dev/docs/development/setup).
Given a directory structure like:

```
...
|-- config-temper/
|-- zephyr-sdk-0.16.5-1/
`-- zmk/
    |-- app
    `-- ...
```

Then from the `zmk/app` directory run the following command to build the
firmware for the left hand board:

```sh
west build -b nice_nano_v2 -p -c -- -DSHIELD="temper_left nice_view_adapter nice_view_temper" -DZMK_CONFIG=../../config-temper-zmk/config -DZMK_EXTRA_MODULES=../../config-temper-zmk -DZephyr-sdk_DIR=../../zephyr-sdk-0.16.5-1/cmake
```

This will produce the file `zmk/app/build/zephyr/zmk.utf`. Put the board into
bootloader mode by pressing the reset button twice, and copy this file to the
board, which will show up as a USB drive when connected to your computer. Repeat
for the right side board.

## Keymap image

The keymap image is created using [keymap-drawer](https://github.com/caksoylar/keymap-drawer).
It can be regenerated with the commands:

```sh
keymap -c img/keymap_drawer.config.yaml parse -c 10 -z config/temper.keymap > img/temper.yaml
keymap -c img/keymap_drawer.config.yaml draw -k chocofi img/temper.yaml > img/temper.svg
```


## Miscellaneous

In MacOS, when a key is held down while entering text, a popup is shown which
lets you choose between various accented forms of the character. The following
command will disable this behaviour.

```sh
defaults write -g ApplePressAndHoldEnabled -bool false
```

## Resources

 * https://github.com/urob/zmk-config
 * https://github.com/caksoylar/keymap-drawer

