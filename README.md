# Thinkpad T450s Catalina

## Notice: If you need to edit config.plist, don't use OpenCore configurator, use ProperTree or Xcode instead.

## Introduction

EFI for Thinkpad T450s Hackintosh Catalina.

CPU: i5-5300U

Integrated Graphics: HD Graphics 5500

Sound Card: ALC292/ALC3232

Wireless Card: BCM94360CS2 With Adapter 

## Bios

- `Security -> Security Chip`: **Disabled**;
- `Memory Protection -> Execution Prevention`: **Enabled**;
- `Virtualization -> Intel Virtualization Technology`: **Enabled**;
- `Internal Device Access -> Bottom Cover Tamper Detection`: must be **Disabled**;
- `Anti-Theft -> Current Setting`: **Disabled**;
- `Anti-Theft -> Computrace -> Current Setting`: **Disabled**;
- `Secure Boot -> Secure Boot`: **Disabled**;
- `UEFI/Legacy Boot`: **UEFI Only**;
- `CSM Support`: **NO**.
- `Wake On LAN`:**Disabled**
- 
## What works

- Sleep / Wake
- Wifi and Bluetooth (BCM94360CS2)
- Handoff, Continuity, AirDrop
- iMessage, FaceTime, App Store, iTunes Store (Change Config.plist -> PlatformInfo -> Generic -> MLB and SystemSerialNumber)
- Ethernet (Disabling Wake on Lan in both the BIOS and the OS can help with sleep problems) (Also SSDT Patches can help)
- Onboard audio (Use alc_fix to fix unworking jack after replug) (Disabling CSM along with alc_fix can help as well)
- USB 2.0 / USB 3.0 (WIP for a more permanent solution)
- Battery(somewhat accurate readout, but i'm still working to make it more accurate)
- Touchpad
- Trackpoint(With RehabMan's voodoops2controller for the three buttons, but at the cost of the gestures not working as perfectly but for the trackpoint users, who cares am i right?)
- Use [one-key-hidpi](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/blob/master/one-key-hidpi) to enable HiDPI

## What doesn't work / Untested

- VGA
- SD Card Reader (more permanent solution needed :P)
- Sidecar (I don't have an iPad to test)
- MiniDP(I don't have a dongle lol)
