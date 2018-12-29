  

# Asus F556U (X556UQK) - High Sierra hackintosh

  
  
  

## Specs

  

Processor | Intel Core i7-7500U CPU (Kaby Lake)

  

Video | Integrated Intel HD 620 + Nvidia GTX 940MX

  

Memory | 8 GB DDR4

  

Storage | Micron 512 GB SSD

  

Connectivity | Wireless AC Atheros ATH9565, Realtek Gigabit Lan, Bluetooth 4.2

  

Audio | Intel HDA - Realtek ALC255

  

Ports | 2x USB 3.0, 1x USB 3.1, HDMI, mic, earphone, SD card reader, LAN

  

TouchPad | Elan Touchpad (ELAN1000)

  

# What works

  

✅ Intel HD 620 (with QE/CI)

  

  

✅ VGA/HDMI (Audio + Video)

  

  

✅ All USB Type A ports

  

  

✅ USB type C port

  

  

✅ Keyboard

  

  

✅ Touchpad

  

  

✅ Internal screen backlight change

  

  

⚠️ Onboard Ethernet (network drops when high speed transfers are initiated)

  

  

✅ Wi-Fi

  

  

✅ UVC HD Webcam

  

  

✅ Speaker + Internal Microphone + Headphone jack (auto detection)

  

  

✅ Laptop lid

  

  

✅ Native power managment

  

  

✅ Battery status

  
  
  

✅ ️Sleep (takes a bit for going completely into sleep mode, but it works!)

  
  
  

⚠️ Bluetooth (Detected by the system but no BT devices can be found)

  
  
  

⚠️ FN Keys (brightness and volume control works - FN+F9 for disabling the touchpad does not work, sleep with FN+F1 crashes the system)

  

  

❌ Realtek SD card reader

  

  

❌ NVIDIA GeForce 940MX (Optimus - impossible to get working at the moment)

  

  

# Kexts list

  

#### Install into your CLOVER/kext/10.13 folder:

  

[Lilu](https://github.com/acidanthera/Lilu)

  

  

[ACPIBatteryManager](https://bitbucket.org/RehabMan/os-x-acpi-battery-driver/downloads/)

  

  

[VoodooI2C + VoodooI2CELAN](https://github.com/alexandred/VoodooI2C)

  

  

[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)

  

  

[RehabMan's FakeSMC sensors](https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads/)

  

  

[AppleALC](https://github.com/acidanthera/AppleALC)
  

  
  

[ATH9KFixup.kext](https://github.com/black-dragon74/ATH9KFixup)





#### Install in /System/Library/Extensions:

  
  
  

[ATH9KInjector.kext](https://github.com/black-dragon74/ATH9KFixup)

  
  

  
#### Install in /Library/Extensions:

  
  
  

[AppleBacklightFixUp.kext](https://bitbucket.org/RehabMan/applebacklightfixup/)

  
  
  

# DSDT/SSDT patches

## Note:

Patched AML files are not available, DSDT and SSDT tables can be different even on the same model.

  

[Extract your DSDT/SSDTs](https://www.tonymacx86.com/threads/guide-patching-laptop-dsdt-ssdts.152573/), modify the files as needed, compile and save your new AML files into CLOVER/ACPI/patched.

(also check out CLOVER/ACPI/patched_dsl for working examples)

  

### Installed patches (with the MaciASL tool):

**_RehabMan Laptop Repo**

  

-  [syn] Fix PARSEOP_ZERO Error (aggressive)

  

-  [bat] ASUS N55SL-Vivobook

  

  

**_VoodooI2C-Patches Repo**

  

- Windows 10 Patch

  

  

- "custom made patch" (check out Scope (_SB.PCI0.I2C1) - Device (ETPD) from the DSL example - 0x55 pinout)

  
  
  

**Others**
-  **AUDIO (AppleALC)**: Enable Clover ACPI Fixes (FixHPET, FixIPIC, FixRTC, FixTMR) and set the layout-id 27.

-  **BRIGHTNESS**: SSDT-PNLF in ACPI/patched (you should already have AppleBacklightFixup.kext installed to /Library/Extensions)

[Guide](https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightfixup-kext.218222/)

- **Wi-FI**: Add "-ath9565" as boot flag
  
- **TOUCHPAD**: DSDT patches as specified before + patch for disabling AppleIntelLpss with Clover, available in the config.plist file)

# Credits

  

Thanks to everyone who made this possibile: RehabMan, alexandred, black-dragon74, Mieze, acidanthera, every contributor to the repos/guides and the whole Hackintosh community.
