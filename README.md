# Asrock deskmini 310 hackintosh
This branch is iMac 19,2 with external graphic card. If you don't have an eGPU, please don't use this branch.

The SSDT doesn't same with master, it will make the bluetooth invalid in hackintosh. Please make sure what version you would like to do.

As the [link](https://egpu.io/external-gpu-buyers-guide-2019/#m2-interface) mentios, M2 eGPU outperforms a 32Gbps-TB3 eGPU by over 20%. The adapter card insteds of SSD on M.2 PCIE slot, please prepare a SATA HDD for system installation first.

![rx580](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/iMac_with_RX580/snapshot/rx580.jpg)

## Gears
CPU: Intel Coffee Lake i7-8700

External eGPU Adapter Card: [ADT R43SG](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.5e242e8dEZJSvC&id=560189396157&_u=lbsepu1bcd3)

Power of external eGPU adapter card：[Dell 12V/220W power](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.5e242e8dEZJSvC&id=583671576782&_u=lbsepu1f5bc)

Video: MSI Radeon RX 580 ARMOR 8G OC

RAM: Kingston DDR4-2666 16GBx2

HDD1: Micron MX500 1T SATAIII

HDD2: Intel 545s 512GB SATAIII

WIFI/BT: DW1560/BCM94352Z WIFI/Bluetooth module mini PCIE/NGFF M2 [taobao link](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.74d62e8d2XfNbV&id=524391843184&_u=lbsepu1ca39)

CPU cooler: NOCTUA NH L9i Fan + CRYORIG C7 Cu

## Important task
- Please keep BIOS in 3.x version
- After copied all kexts to system, please remerber to use tool - Kext Utility to rebuild cache.

## For BIOS 4.x
DSDT Patch

```code
comment: Fix RTC _STA bug (fix asrock new bios failed to boot)
Find: A00A9353 54415301
Replace: A00A910A FF0BFFFF
```

## Issues
NO!!!

## Snapshot
![About](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/about.png)

![IGPU](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/IGPU.png)

![bluetooth](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/bluetooth.png)

![ethernet](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/ethernet.png)

![usb](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/usb.png)

![video_1](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/video_1.png)

## Dual monitor output - DP and HDMI
![video_2](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/dual_monitor1.png)

![video_3](https://github.com/liminghuang/asrock_deskmini310_hackintosh/raw/master/snapshot/dual_monitor2.png)


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

# Why I choose hackintosh? 
[My youtube link](https://youtu.be/d5WUizoIxy0) <-- Language is Mandarin
