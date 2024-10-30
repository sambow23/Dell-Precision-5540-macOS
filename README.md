# Dell Precision 5540
<img src="https://i.imgur.com/Uql3mVu.png" width="650">

| Hardware  | |
| ------------- | ------------- |
| CPU  | Intel® Core™ i7-9850H |
| RAM  | 32GB DDR4 |
| GPU  | Intel UHD Graphics 630  |
| dGPU  | NVIDIA Quadro T1000 Mobile 4GB  |
| Network  | Intel Wireless-AC 9260  |
| Storage  | Samsung SSD 990 PRO 2TB |
| OS  | NixOS, macOS Sequoia 15.1, Windows 11 24H2 LTSC |
| Screen  | 15.6" 3840x2160 Touchscreen  | 

## EFI Vars
#### Use with `modGRUBShell` tool In OpenCore
|  Var | Offset |
| ------------- | ------------- |
| setup_var_cv | Setup 0x6ED 0x01 0x00 |
| setup_var | 0xA10 0x02 |
| setup_var | 0xA11 0x03 |
| setup_var_3 | 0x789 0x00 |

## Thunderbolt
> [!CAUTION]
> If you plug in a Thunderbolt dock with a PCIe-based NIC while already booted into macOS, the system will freeze and kernel panic. For these kind of docks, make sure it's already plugged in before booting macOS.
> 
> There is stability issues with hotplug depending on the Thunderbolt device used, so YMMV

> [!NOTE]  
> If using a Thunderbolt dock such as the CalDigit TS3 Plus or above, the Intel I210 NIC causes system instability when active, it's suggested you either unplug the ethernet cable from the dock or disable the DriverKit kext using these boot arguments.
> 
> `dk.e1000=0 e1000=0`


### Thunderbolt BIOS Settings
|  Thunderbolt Adapter Configuration ||
| ------------- | ------------- |
| Enable Thunderbolt™ Technology Support | ✅ |
| Enable Thunderbolt™ Boot Support | ✅ |
| Enable Thunderbolt™ Adapter Pre-boot Modules | ✅ |
| No Security | ✅ |

|  Thunderbolt Auto Switch ||
| ------------- | ------------- |
| Auto Switch | ✅ |

## Issues
#### External Displays
When plugging in external displays, the internal display will become blank and strobe the backlight at a high frequency. It can be temporarily fixed by closing the lid for at least 10 seconds and then opening it back up. EDID patching may fix this.

#### System Stutter
There is mild to severe stutter every few minutes, I believe it has to do the with Samsung NVMe drive I am using.

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
- Thunderbolt
  - eGPUs ✅
  - Thunderbolt Docks ✅
- Internal Audio (Speakers, Headphones, Microphone)

#### Untested
- iCloud Services
- Bluetooth (no kext installed yet)

#### Not working
- Fingerprint Sensor (no support)
- dGPU (disabled)
