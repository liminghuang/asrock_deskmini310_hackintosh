# Asrock deskmini 310 hackintosh

## Gears
CPU: Intel Coffee Lake i7-8700

RAM: Kingston DDR4-2666 16GBx2

SSD: Intel 760p 512GB M.2 PCIE

HDD1: Intel 545s 512GB SATAIII

WIFI/BT: DW1560/BCM94352Z WIFI/Bluetooth module mini PCIE/NGFF M2

CPU cooler: NOCTUA NH L9i Fan + CRYORIG C7 Cu


## Works
- [x] Ethernet/WIFI/Bluetooth/Audio/USB

- [x] DP/HDMI dual monitor output

- [x] Shutdown、Sleep

- [x] Graphics(Intel UHD 630)

## Issues
If you are using FCPX, system will hang/freeze in FCPX when you add some video effects. 
Please disable background rendering in FCPX first.
It's macOS 10.14.3 issue, someone report that 10.14.4 beta has already fixed this issue, let's wait the version release.(finger crossed!) 

## Snapshot
![About](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/about.png)

![IGPU](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/IGPU.png)

![bluetooth](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/bluetooth.png)

![ethernet](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/ethernet.png)

![usb](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/usb.png)

![video_1](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/video_1.png)

## Tools - Here are some tools you need...

Clover Configurator

MultiBeast

MaciASL

Kext Utility

IORegistryExplorer

Hackintool

Kext Updater

## Notes
After macOS installed done, please leave FakeSMC.kext only in /Library/Extensions and use Kext Updater tool to install other kexts again. Kext Updater will help you to manage what dictionary is good for kext driver to install.

*ps. I remove my serial number and others private info in SMBIOS, please refill those info by Clover first.
