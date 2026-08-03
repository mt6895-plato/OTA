# Installation Guide for Xiaomi 12T
## Overview
This guide provides step-by-step on how to install AOSP ROMs to your Xiaomi 12T.<br>
Before proceeding, make sure you have all of your data backupped, and you must have unlocked bootloader!!!

## Steps
1. Download engineered preloader [right here.](https://raw.githubusercontent.com/xiaomi-mediatek-devs/mt6895_eng_preloaders/master/preloader_plato_eng.bin) ( SHA256SUM: `544f0a12fff598ed1866b695398d3b193b3ffc58`)
2. Flash `preloader_plato_eng.bin` to preloader1 and preloader2 through fastboot
```
fastboot flash preloader1 preloader_plato_eng.bin
fastboot flash preloader2 preloader_plato_eng.bin
```
3. Flash `boot.img` and `vendor_boot.img`
```
fastboot flash boot_ab boot.img
fastboot flash vendor_boot_ab vendor_boot.img
```
4. Reboot to recovery
5. In the recovery, click `Factory Reset -> Format Data`
6. Go back, select `Apply Update -> Apply from ADB`
7. Sideload the ROM
```
adb sideload your-downloaded-rom.zip
```
