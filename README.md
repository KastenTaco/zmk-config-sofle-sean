Sean's Sofle Keyboard
=============== 

Happy Birthday, Sean.

Thi is the repository to your brand new [Sofle](https://github.com/josefadamcik/SofleKeyboard), a split wireless
mechanical keyboard. Your keyboard is a wireless variant of the original Sofle. It is based off the Sofle RGB's design: [SofleChocWireless](https://github.com/josefadamcik/SofleKeyboard)

Key Features:
 * Compatible Kailh Choc V1 low profile switches
 * QWERTY base layout
 * FULLY programable and customizable
 * 3-layer configuratioon
 * OLED Screens
 * Per Key LED Lighting
 * Wireless using a NRF52840
 * 2500mAh battery per keyboard half
 

## Keyboard

This keyboard is designed for low profile Kailh Choc V1 switches. Choc switches generally have shorter actuation. In short, this allows keys to activate even quicker than the classic MX switches. On top of that, low profile keys are thought to be more ergonomic. 

The keyboard origninally came with [Kailh Choc V1 Red Pro Switches](https://www.littlekeyboards.com/products/kailh-choc-pro-low-profile-switches?variant=32328459681859). These linear switches come in at 35g of actuation force. A lightweight actuation translates to quicker keypresses and even quicker reaction times for gaming. 

![keyboard image](img/seankeeb.jpg)

## Case
The case is a fully custom and self designed. It comes with a gasket mount for increased comfort and best possible sound.
The stl files for the case can be found within the repository.

![keyboard image](img/seankeebback.jpg)

## Keymap
If you would like to make changes to the layout, let me know. It's super straightforward and something we can do together. There are MANY features we can add. Some of those are: Comgos, Tap Dancing, Home Row Mods, Tap-Hold Behavior, and some really elaborate Macros. 
More information on what all you can do is here [ZMK Firmware](https://zmk.dev/). 

This is the keyboards keymap including layer shifts:
![keymap image](img/sofle.svg)


______________________________________________________________________________________________
## Other information


## Keymap image

The keymap image is created using [keymap-drawer](https://github.com/caksoylar/keymap-drawer).
It can be regenerated with the commands:

```sh
keymap -c img/keymap_drawer.config.yaml parse -c 10 -z config/temper.keymap > img/temper.yaml
keymap -c img/keymap_drawer.config.yaml draw -k chocofi img/temper.yaml > img/temper.svg
```

```sh
defaults write -g ApplePressAndHoldEnabled -bool false
```

## Resources

 * https://github.com/urob/zmk-config
 * https://github.com/caksoylar/keymap-drawer

