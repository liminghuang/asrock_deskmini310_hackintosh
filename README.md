### Hi ALL, my deskmini 310 starts to use an external graphic card now, this master version will not be under my maintenance. If you are interested in the new branch version with AMD RX580, go to [here](https://github.com/liminghuang/asrock_deskmini310_hackintosh/tree/iMac_with_RX580) and I will focus on this new version, thanks.

嗨! 各位,我的deskmini 310開始使用外掛顯卡了,這個版本我不再維護,如果你對於新版本有興趣,請到[這裡](https://github.com/liminghuang/asrock_deskmini310_hackintosh/tree/iMac_with_RX580)

# Asrock deskmini 310 hackintosh
2019/07/17: Upgrade to Clover 5018. Clover has new folder struct, all drivers moved to CLOVER/drivers/UEFI. I found my bluetooth keyboard has latency issue. I recommand keep Clover version at 4972.

2019/05/14: Upgrade to 10.14.15, everything is alright.

## Gears
CPU: Intel Coffee Lake i7-8700

RAM: Kingston DDR4-2666 16GBx2

SSD: Intel 760p 512GB M.2 PCIE

HDD1: Intel 545s 512GB SATAIII

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

## Works
- [x] Ethernet/WIFI/Bluetooth/Audio/USB 2.0, 3.0(type-A, type-C)

- [x] DP/HDMI dual monitor output

- [x] Shutdown、Sleep

- [x] Graphics(Intel UHD 630)

## Issues
~~If you are using FCPX, system will hang/freeze in FCPX when you add some video effects. 
Please disable background rendering in FCPX first.
It's macOS 10.14.3 issue, someone report that 10.14.4 beta has already fixed this issue, let's wait the version release.(finger crossed!)~~

After upgraded to 10.14.4, FCPX is running smoothly, enable background rendering and everything is fine.

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
