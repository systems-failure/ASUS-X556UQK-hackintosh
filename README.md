# Asus F556U (X556UQK) - High Sierra hackintosh

## Specs


---- | Asus X556UQK
------------ | -------------
Processor |	Intel Core i7-7500U CPU (Kaby Lake)
Video |	Integrated Intel HD 620 + Nvidia GTX 940MX
Memory |	8 GB DDR4
Storage |	Micron 512 GB SSD
Connectivity |	Wireless AC Atheros ATH9565, Realtek Gigabit Lan, Bluetooth 4.0
Audio | Intel HDA - Realtek ALC255
Ports | 2x USB 3.0, 1x USB 3.1, HDMI, mic, earphone, SD card reader, LAN
TouchPad | Elan Touchpad (ELAN1000)

# What works
  
✅ Intel HD 620 (with QE/CI)

✅ HDMI (Audio + Video)

✅ All USB ports

✅ Keyboard

✅ TouchPad

✅ Keyboard Backlighting

✅ Ethernet (LAN)

✅ Wi-Fi

✅ Bluetooth

✅ UVC HD Webcam

✅ Speaker + Internal Microphone

✅ Laptop lid

⚠️ Battery Status (mostly)

⚠️ USB-C (not tested, should work fine)

⚠️ Sleep (fixable)

⚠️ FN Keys (only works with volume control - fixable)

⚠️ Battery status is 0% when AC Adapter is connected. (fixable)

❌ SD card reader

❌ NVIDIA Optimus (impossible to get working at the moment)


# Kexts list

#### Everything should be installed with a proper Kext Installer into /Libraries/Extensions for proper compatibility

[Lilu](https://github.com/acidanthera/Lilu)

[ATH9KInjector + ATH9KFixup](https://github.com/black-dragon74/ATH9KFixup) (with -ath9565 boot flag)

[ACPIBatteryManager](https://bitbucket.org/RehabMan/os-x-acpi-battery-driver/downloads/) + DSDT patches (ASUS VivoBook)

[VoodooI2C + VoodooI2CELAN](https://github.com/alexandred/VoodooI2C) (with DSDT patches - 0x55 pinout + disable AppleIntelLpss from Clover)

[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)

[RehabMan' s FakeSMC sensors](https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads/)

[AppleALC](https://github.com/acidanthera/AppleALC) (layout-id 27) + Clover ACPI Fixes (FixHPET, FixIPIC, FixRTC, FixTMR)

[AppleBacklightInjector + SSDT-PNLF + AppleBacklight Clover
patch](https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/)

Thanks to everyone who made this possibile: developers and the whole hackintosh community.