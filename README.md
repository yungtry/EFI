# EFI
 Vanilla AMD Ryzen OpenCore config for my hackintosh 🏴‍☠️ 
## Specs
* **Motherboard:**  Asrock AB350M Pro4 R2.0

* **CPU:** AMD Ryzen 5 3600

* **RAM:** G.Skill Aegis 16GB (2x8GB) DDR4 3000MHz CL16

* **GPU:** NVIDIA GTX 670, NVIDIA GTX 1060 (Disabled)

* **Network:**

      Ethernet: Realtek RTL8111

      Wi-Fi: TL-WN725N

* **Bluetooth:** Asus BT400

## config.plist

Edited sample.plist from OpenCorePKG/Docs.

I've followed [that](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/amd-config.plist/amd-config) tutorial with few minor changes:

1. Disabled GTX 1060 - Root -> DeviceProperties -> Add -> `PciRoot(0x0)/Pci(0x3,0x1)/Pci(0x0,0x0)`
2. Added built-in Realtek ethernet to make iServices work: Root -> DeviceProperties -> Add -> `PciRoot(0x0)/Pci(0x1,0x3)/Pci(0x0,0x2)/Pci(0x1,0x0)/Pci(0x0,0x0)`

## SSDTs

Compiled my own [SSDT-EC-USBX.dsl](https://github.com/yungtry/EFI/blob/master/EFI/OC/ACPI/SSDT-EC-USBX.dsl)

## Kexts

[Nothing interesting tbh.](https://github.com/yungtry/EFI/tree/master/EFI/OC/Kexts)

## UEFI settings

Under boot options: Disabled CSM, Enabled Above 4G

## Useful post-install apps

* [MountEFI](https://github.com/corpnewt/MountEFI)

* [ProperTree](https://github.com/corpnewt/ProperTree) - Cross platform GUI plist editor written in python

* [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) - Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist.

* [iasl](https://github.com/RehabMan/Intel-iasl)

* [TL-WN725N Driver](https://www.tp-link.com/en/support/download/tl-wn725n/)

* [BetterTouchTool](https://folivora.ai/) - Modifies gestures

* [SteelSeries Engine](https://steelseries.com/engine) - Fixes acceleration on SteelSeries mouse

* [ckb-next](https://github.com/ckb-next/ckb-next) - Corsair RGB Driver for Linux and macOS

* [SwitchResX](https://www.madrau.com/) - Upscales resolution, disables unused screens

* [Rocket](https://matthewpalmer.net/rocket/) - Discord/Slack-style emoji picker

* [Lungo](https://sindresorhus.com/lungo) - Prevent your Mac from going to sleep

* [RunCat](https://apps.apple.com/us/app/runcat/id1429033973?mt=12) - The cat runs at the speed according to the CPU usage of your Mac. By looking at the running of a cat, you can see how much CPU load is.
