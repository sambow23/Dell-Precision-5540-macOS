# Dell Precision 5540
<img src="https://i.imgur.com/Uql3mVu.png" width="650">

| Hardware  | |
| ------------- | ------------- |
| CPU  | Intel® Core™ i7-9850H |
| RAM  | 32GB DDR4 |
| GPU  | Intel UHD Graphics 630  |
| dGPU  | NVIDIA Quadro T1000 Mobile 4GB  |
| Network  | Intel Wireless-AC 9260  |
| Storage  | WD_BLACK SN850X 2TB |
| OS  | NixOS, macOS Sequoia 15.1, Windows 11 24H2 LTSC |
| Screen  | 15.6" 3840x2160 Touchscreen  | 

> [!CAUTION]
> [You must set the EFI Variables before booting this EFI](https://github.com/sambow23/Dell-Precision-5540-macOS/discussions/6)

## Issues
#### [External Displays](https://github.com/sambow23/Dell-Precision-5540-macOS/issues/3)
#### [System Stutter](https://github.com/sambow23/Dell-Precision-5540-macOS/issues/2#issuecomment-2458689714)
#### [Headphones](https://github.com/sambow23/Dell-Precision-5540-macOS/issues/4)

## Hardware compatibility

#### What works
- CPU power management
- GPU acceleration and video codecs
- SSD
- Wi-Fi (itlwm)
- All USB ports
- USB-C Video
- Trackpad
- Touchscreen 
- FN Keys
- Webcam
- Screen Brightness
- Battery percentage
- Sleep
- HDMI Out
- [Thunderbolt](https://github.com/sambow23/Dell-Precision-5540-macOS/discussions/5)
  - eGPUs ✅ | No hotplug, needs a different [SSDT](https://github.com/sambow23/Dell-Precision-5540-macOS/blob/ed29189690d0f5e7b026cdae1497c871b5c75907/EFI/OC/ACPI/SSDT-TB3.aml)
  - Thunderbolt Docks ✅ | Hotplug supported
- Internal Audio (Speakers, Headphones, Microphone)

#### Untested
- iCloud Services
- Bluetooth (no kext installed yet)

#### Not working
- Fingerprint Sensor (no support)
- dGPU (disabled)
