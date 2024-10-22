# Dell Precision 5540
| Hardware  | |
| ------------- | ------------- |
| CPU  | Intel® Core™ i7-9850H |
| RAM  | 32GB DDR4 |
| GPU  | Intel UHD Graphics 630  |
| dGPU  | NVIDIA Quadro T1000 Mobile 4GB  |
| Network  | Intel Wireless-AC 9260  |
| Storage  | Samsung SSD 990 PRO 2TB |
| OS  | NixOS, macOS Sequoia 15.0.1 |
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
|  Thunderbolt Adapter Configuration ||
| ------------- | ------------- |
| Enable Thunderbolt™ Technology Support | ✅ |
| Enable Thunderbolt™ Boot Support | ✅ |
| Enable Thunderbolt™ Adapter Pre-boot Modules | ✅ |
| No Security | ✅ |

|  Thunderbolt Auto Switch ||
| ------------- | ------------- |
| Auto Switch | ✅ |

## Hardware compatibility

#### What works
- CPU power management
- GPU acceleration and video codecs
- SSD
- Wi-Fi (itlwm)
- All USB ports
- USB-C Video
- Trackpad
- FN Keys
- Webcam
- Screen Brightness
- Battery percentage
- Sleep
- HDMI Out
- Thunderbolt
- Internal Audio (Speakers, Headphones, Microphone)

#### Untested
- iCloud Services
- Bluetooth (no kext installed yet)

#### Not working
- Fingerprint Sensor
- dGPU (disabled)
- Touchscreen
