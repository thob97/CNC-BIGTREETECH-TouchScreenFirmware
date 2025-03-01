# CNC-BIGTREETECH-TouchScreenFirmware

BIGTREETECH Firmware changed to work for my specific cnc setup.

<img src="./example_pictures/1.jpeg"  width="30%" height="30%">

## Table Of Content

- [Getting Started](#getting-started)
    - [Installing](#installing)
    - [Update TFT Firmware](#update-tft-firmware)
    - [Configuration](#configuration)
- [Example pictures](#example-pictures)
- [Related](#related)
- [Acknowledgments](#acknowledgments)
- [Forked Projekt ReadMe](#bigTreeTech-touchscreen-firmware)

## Getting Started

### Installing

* ```git clone https://github.com/thob97/CNC-BIGTREETECH-TouchScreenFirmware.git```
* ```cd CNC-BIGTREETECH-TouchScreenFirmware```

### Update TFT Firmware

TFT firmware updates are comprised of two parts:

1. The firmware binary (`BIGTREE_TFT*_V*.*.*.bin`). Example: `BIGTREE_TFT35_V3.0.25.2.bin`:
     - `BIGTREE_TFT_35`: model
     - `V3.0`: hardware version
     - `25.2`: software version
2. Fonts and Icons (`TFT*` folder):
   - `TFT*/font`: fonts
   - `TFT*/bmp`: icons

Copy both the `BIGTREE_TFT*_V*.*.*.bin` and `TFT*` folder to the root of a blank SD card that is <8GB and formatted as FAT32:

![image](https://user-images.githubusercontent.com/13375512/76688998-3e989e80-65ef-11ea-93df-29a8216475a6.png)

Place SD card with `BIGTREE_TFT*_V*.*.*.bin` &amp; `TFT*` folder into the TFT's SD card reader and power cycle your printer to start the update process.

<p align=center> ⚠️ Failing to update your icons &amp; fonts will result in missing icons and/or unreadable text ⚠️ </p>

### Configuration
The Firmware can be configured using the **config.ini** file from from one of these folders:
[`Copy to SD Card root directory to update`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update) or
[`Copy to SD Card root directory to update - Unified Menu Material theme`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update%20-%20Unified%20Menu%20Material%20theme)

#### Editing configuration (config.ini) file
To edit the **config.ini** file follow the instruction here: [Detailed Instructions here](config_instructions.md)

#### Updating Firmware Configuration
To update the Firmware configuration:
1. Edit the settings in **config.ini**.
2. Copy the **config.ini** file to the root of the SD card. (The SD card capacity should be less than or equal to 8GB and formatted as FAT32)
3. Insert the SD card in the TFT's SD card slot and restart the TFT by pressing the reset buttion or disconnecting and connecting the power cable.
4. The TFT will update and store the configuraiton form **config.ini** file.

## Example pictures
<p float="left">
    <img src="./example_pictures/1.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/2.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/3.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/4.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/5.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/6.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/7.jpeg"  width="30%" height="30%">
    <img src="./example_pictures/8.jpeg"  width="30%" height="30%">
</p>

## Related
* [3040 CNC Marlin](https://github.com/thob97/3040-CNC-marlin.git)
* [CNC-BIGTREETECH-TouchScreenFirmware](https://github.com/thob97/CNC-BIGTREETECH-TouchScreenFirmware.git)
* [MarlinCNC](https://github.com/thob97/MarlinCNC.git)
* [submodule-mpcnc_post_processor](https://github.com/thob97/submodule-mpcnc_post_processor.git)

## Acknowledgments

* https://github.com/jeffeb3/BIGTREETECH-TouchScreenFirmware
* https://github.com/V1EngineeringInc/BIGTREETECH-TouchScreenFirmware
* https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware

<br /><br /><br /><br /><br /><br /><br /><br /><br />








V1- Folder "Copy to SD Card root directory to update - Unified Menu Material theme"


<!-- omit in toc -->
# BigTreeTech Touchscreen Firmware
![GitHub](https://img.shields.io/github/license/bigtreetech/bigtreetech-TouchScreenFirmware.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/bigtreetech/bigtreetech-TouchScreenFirmware.svg)](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/graphs/contributors)
![GitHub Release Date](https://img.shields.io/github/release-date/bigtreetech/bigtreetech-TouchScreenFirmware.svg)
[![Build Status](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/workflows/Build%20Test/badge.svg?branch=master)](https://github.com/bigtreetech/bigtreetech-TouchScreenFirmware/actions)

Firmware for BigTreeTech's dual-mode touchscreen 3D printer controllers

<img width=500 src="https://user-images.githubusercontent.com/13375512/76691608-ae1b8780-6609-11ea-9ee1-421bcf09e538.png">

<!-- omit in toc -->
## Table of Contents
- [Menus and Themes](#menus-and-themes)
- [Update TFT Firmware](#update-tft-firmware)
- [Configuration](#configuration)
- [Customization](#customization)
  - [Bootscreen and Icons](#bootscreen-and-icons)
  - [Firmware](#firmware)
- [Troubleshooting](#troubleshooting)
- [Version History](#version-history)
- [CNC Targeted Modifications](#CNC-Targeted-Modifications)

## Menus and Themes

| Classic Menu &amp; Icon Theme |  Unified Menu &amp; Material Icon Theme |
:--------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/54511555/77016371-ad9a2e00-6934-11ea-9e57-23c2ab2cad58.png) | ![](https://user-images.githubusercontent.com/54511555/77016415-d3273780-6934-11ea-8c61-a184fa55b420.png)
Use firmware, icons, and fonts from the [`Copy to SD Card root directory to update`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update) folder | Use firmware, icons, and fonts from the [`Copy to SD Card root directory to update - Unified Menu Material theme`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update%20-%20Unified%20Menu%20Material%20theme) folder

## Update TFT Firmware

TFT firmware updates are comprised of two parts:

1. The firmware binary (`BIGTREE_TFT*_V*.*.*.bin`). Example: `BIGTREE_TFT35_V3.0.25.2.bin`:
     - `BIGTREE_TFT_35`: model
     - `V3.0`: hardware version
     - `25.2`: software version
2. Fonts and Icons (`TFT*` folder):
   - `TFT*/font`: fonts
   - `TFT*/bmp`: icons

Copy both the `BIGTREE_TFT*_V*.*.*.bin` and `TFT*` folder to the root of a blank SD card that is <8GB and formatted as FAT32:

![image](https://user-images.githubusercontent.com/13375512/76688998-3e989e80-65ef-11ea-93df-29a8216475a6.png)

Place SD card with `BIGTREE_TFT*_V*.*.*.bin` &amp; `TFT*` folder into the TFT's SD card reader and power cycle your printer to start the update process.

<p align=center> ⚠️ Failing to update your icons &amp; fonts will result in missing icons and/or unreadable text ⚠️ </p>

## Configuration
The Firmware can be configured using the **config.ini** file from from one of these folders:
[`Copy to SD Card root directory to update`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update) or
[`Copy to SD Card root directory to update - Unified Menu Material theme`](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/Copy%20to%20SD%20Card%20root%20directory%20to%20update%20-%20Unified%20Menu%20Material%20theme)

### Editing configuration (config.ini) file
To edit the **config.ini** file follow the instruction here: [Detailed Instructions here](config_instructions.md)

### Updating Firmware Configuration
To update the Firmware configuration:
1. Edit the settings in **config.ini**.
2. Copy the **config.ini** file to the root of the SD card. (The SD card capacity should be less than or equal to 8GB and formatted as FAT32)
3. Insert the SD card in the TFT's SD card slot and restart the TFT by pressing the reset buttion or disconnecting and connecting the power cable.
4. The TFT will update and store the configuraiton form **config.ini** file.

## Customization

### Bootscreen and Icons
See [Customization guides](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/readme/) for detailed  information.

### Firmware
<details><summary>View full instructions</summary>
<ol>
<li>Setup Visual Studio Code with PlatformIO <a href="https://github.com/bigtreetech/Document/blob/master/How%20to%20install%20VScode+Platformio.md">instructions</a></li>
<li>Click on the PlatformIO icon (①) and then click on Open Project (②):
   <img src="https://user-images.githubusercontent.com/25599056/56637513-6b258e00-669e-11e9-9fad-d0571e57499e.png"></li>
<li>Find the BIGTREETECH  firmware source directory , then click Open:
   <img src="https://user-images.githubusercontent.com/25599056/56637532-77115000-669e-11e9-809b-f6bc25412f75.png"></li>
  <li>After opening the project, edit <a href="platformio.ini"><code>platformio.ini</code></a> and change the <code>default_envs</code> to one that matches your TFT model and version:
   <pre>;BIGTREE_TFT35_V1_0
;BIGTREE_TFT35_V1_1
;BIGTREE_TFT35_V1_2
;BIGTREE_TFT35_V2_0
;BIGTREE_TFT35_V3_0
;BIGTREE_TFT35_E3_V3_0
;BIGTREE_TFT28_V1_0
;BIGTREE_TFT28_V3_0
;BIGTREE_TFT24_V1_1
;MKS_32_V1_4
;MKS_32_V1_4_NOBL

[platformio]
src_dir      = TFT
boards_dir   = buildroot/boards
default_envs = BIGTREE_TFT35_V3_0</pre></li>
  <li>Click the check mark (✓) at the bottom of VSCode or press <code>Ctrl</code>+<code>Alt</code>+<code>B</code> (Windows) / <code>Ctrl</code>+<code>Option</code>+<code>B</code> (macOS) to compile.

<img src="https://user-images.githubusercontent.com/25599056/56637550-809ab800-669e-11e9-99d3-6b502e294688.png"></li>
<li>A <code>BIGTREE_TFT*_V*.*.*.bin</code> file will be generated in the <em>hidden</em> <code>.pio\build\BIGTREE_TFT*_V*_*</code> folder. Follow the update process outlined in the <a href="#about-tft-firmware">About TFT Firmware</a> section above to update your TFT to the latest version.</li>
</details>

## Troubleshooting

To reset the TFT's touch screen calibration, create a blank file named `reset.txt` and place in root folder of the sd card. Insert the SD card into the TFT's SD card reader and power cycle your printer to start the reset process.

## Version History

See [BIGTREETECH-TouchScreenFirmware/releases](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/releases) for a complete version history.

## CNC Targeted Modifications

1. Possibility to define CNC_MENU in Configuration.h in order to configure the SW for CNC purposes
2. Introduced new language and icons tags for CNC specific menu items (no impact on 3D printer tags)
3. Added some specific bitmaps (from [BlomsD / MPCNC-TFT35-V2.0](https://github.com/BlomsD/MPCNC-TFT35-V2.0))
4. Introduced a new menu spindle.c in order to add spindle start/stop control
5. Removed Bed and Extruder Heating menu items from Mainpage.c
6. Forced configuration in order to remove persistent Bed/Extruder temperature indication on all the pages
7. Modified the Home menu in order to support G28 XY and G28 Z and Zero axes
8. Possibility to define CNC_LASER in configuration.h in order to introduce menù for laser management (instead of fan)

See:

1.[TFT35 Home Menu (Home XY)](https://youtu.be/tTO4IgWAW1k)

2.[TFT35 Home Menu (Home Z - Zero 0)](https://youtu.be/vSVPUKN2T6w)

3.[TFT35 Home Spindle (Spindle ON/OFF)](https://youtu.be/DXpbi54GyoA)

