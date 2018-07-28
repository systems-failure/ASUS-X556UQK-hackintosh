# Asus F556U (X556UQK) - High Sierra hackintosh

## Specs


---- | Asus X556UQK
------------ | -------------
Processor |	Intel Core i7-7500U CPU (Kaby Lake)
Video |	Integrated Intel HD 620 + Nvidia GTX 940MX
Memory |	8 GB DDR4
Storage |	Micron 512 GB SSD
Connectivity |	Wireless AC Atheros ATH9565, Realtek Gigabit Lan, Bluetooth 4.2
Audio | Intel HDA - Realtek ALC255
Ports | 2x USB 3.0, 1x USB 3.1, HDMI, mic, earphone, SD card reader, LAN
TouchPad | Elan Touchpad (ELAN1000)

## Please note: DO NOT blindly copy the CLOVER folder into your EFI partition. 

## DSDT and SSDT tables can be different even on the same model.

## You must then [extract DSDT/SSDTs](https://www.tonymacx86.com/threads/guide-patching-laptop-dsdt-ssdts.152573/) and modify the files as needed.

# What works
  
✅ Intel HD 620 (with QE/CI)

✅ HDMI (Audio + Video)

✅ All USB Type A ports

✅ Keyboard

✅ Touchpad

✅ Internal screen backlight change

✅ Ethernet (LAN)

✅ Wi-Fi

✅ Bluetooth

✅ UVC HD Webcam

✅ Speaker + Internal Microphone + Headphone jack (auto detection)

✅ Laptop lid

✅ Native power managment

⚠️ FN Keys (brightness and volume control - FN+F9 for disabling the touchpad does not work)

⚠️ Battery Status (mostly, battery status is 0% when AC Adapter is connected)

⚠️ Sleep (wakes up immediately)

⚠️ USB-C (not tested, should work fine)

❌ Realtek SD card reader

❌ NVIDIA GeForce 940MX (Optimus - impossible to get working at the moment)


# Kexts list

#### Everything should be installed with a proper Kext Installer into /Libraries/Extensions for proper compatibility

[Lilu](https://github.com/acidanthera/Lilu)

[ATH9KInjector + ATH9KFixup](https://github.com/black-dragon74/ATH9KFixup) (with -ath9565 boot flag)

[ACPIBatteryManager](https://bitbucket.org/RehabMan/os-x-acpi-battery-driver/downloads/) + DSDT patches (ASUS VivoBook)

[VoodooI2C + VoodooI2CELAN](https://github.com/alexandred/VoodooI2C) (with DSDT patches - 0x55 pinout + disable AppleIntelLpss from Clover)

[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)

[RehabMan's FakeSMC sensors](https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads/)

[AppleALC](https://github.com/acidanthera/AppleALC) (layout-id 27) + Clover ACPI Fixes (FixHPET, FixIPIC, FixRTC, FixTMR)

[AppleBacklightInjector + SSDT-PNLF + AppleBacklight Clover
patch](https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/)

Thanks to everyone who made this possibile: developers and the whole hackintosh community.
