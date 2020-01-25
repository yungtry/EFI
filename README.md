# EFI
OpenCore config for my hackintosh.

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

## Post-install apps

*To be updated*
