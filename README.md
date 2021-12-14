# Asus Vivobook A442UQ-FA047T OpenCore Hackintosh
Opencore Bootloader Configuration for running macOS on Asus Vivobook A442UQ-FA047T with BIOS ver. 300.
Not intended for Public Usage, but available to use at your own risks, and don't forget to provide feedback.

![Screen Shot 2021-12-14 at 12 32 29](https://user-images.githubusercontent.com/46070105/145934710-3596001d-e9e8-40d9-aef4-4f7095c37442.png)

OpenCore version 0.7.5

Tested on the following build
- Big Sur 11.5.1
- Monterey 12.0.1

## System Specification
Items | Details |
--- | --- |
Model	| Asus Vivobook A442UQ-FA047T
CPU	| Intel Core i5-8250U (KabyLake-R)
Graphics	| Intel UHD Graphics 620 & Nvidia Geforce 940MX
RAM	| SKHynix Onboard 8GB + TEAM Elite 8GB DDR4 @ 2400 Mhz
Storage | TEAM 3D L5 SATA SSD 240GB
Wi-Fi / Bluetooth	| Intel Wireless AC-7265 (Replaced)
Card Reader	| Realtek USB Based Card Reader
Webcam	| ASUS UVC HD Camera
Audio	| Realtek ALC256 (5)
Touchpad	| ELAN1200
UEFI BIOS |	X442UQR.300

## Not Working
- Nvidia Geforce 940MX dGPU (Optimus)
- ELAN1200 Touchpad sometimes freeze for a bit. (Usable)
- etc.

## General Guides
- Download a copy of OpenCore latest releases and replace the following files from this repository
  - EFI/BOOT/BOOTx64.efi
  - EFI/OC/OpenCore.efi
  - EFI/OC/Drivers/OpenRuntime

  with the ones from the latest OpenCore release, and don't forget to adjust as well as compare my config.plist file with the sample.plist from latest OpenCore     release.
And lastly validate the config with [Sanity Checker](https://opencore.slowgeek.com/), and [ocvalidate](https://github.com/acidanthera/OpenCorePkg/tree/master/Utilities/ocvalidate).
- I advise you to go to [Dortania's Opencore Guide](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html) for a better understanding with OpenCore Configurations.
- Unlock MSR 0xE2 Register using OpenCore's ControlMsrE2.efi
- Generate your own SMBIOS and Platform Info (Serial Number, etc) before booting with this configuration.

## Post-Install
- Refer to [Dortania's Post-Install Guide](https://dortania.github.io/OpenCore-Post-Install/) for stuff to do after installation of macOS.
- To make the Combo 3.5mm Jack working properly visit maz-1's [Combo Jack Repository](https://github.com/hackintosh-stuff/ComboJack) and follow the steps there starting from step 2 since we are using OpenCore and only need the shell file because the VerbStub.kext was already added in OC/Kexts.

## Acknowledgements
- Apple for macOS
- tctien342 and hieplpvip for Asus stuff and repositories.
- The VoodooI2C Team for I2C touchpad patches and kexts.
- The Acidanthera Team for OpenCore and many other kexts.
- The Dortania Team for OpenCore Guides.
- maz-1 for the Combo Jack Fix repositories and VerbStub.kext.
- IlhamSevensky for the Fn Keys Patch on OpenCore Bootloader.
- corpnewt for SSDTTime and many othe hotpatches.
- headkaze for Hackintool.
- The whole hackintosh community and many more people that I can't state here.
