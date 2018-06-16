# Thinkpad P51 High Sierra

Feature set source: http://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad%20P51/ThinkPad_P51_Platform_Specifications.pdf

## Hardware:

| Category | Element | Compatibility | Notes |
| ------------- | ------------- | ------------- | ------------- | 
| CPU | i7-7700HQ | FULL | Native power management works correctly, as per: https://www.tonymacx86.com/threads/guide-native-power-management-for-laptops.175801/
| GPU | HD630 | FULL | Same as above. Full hardware acceleration.					
| | NVIDIA M1200 | NO:DISABLED | Disabled as per: https://www.tonymacx86.com/threads/guide-disabling-discrete-graphics-in-dual-gpu-laptops.163772/ |
| MEMORY | 1x16GB | FULL | |
| DISPLAY | 4K | FULL | |
| STORAGE | Samsung NVMe 256GB | FULL | |
| ETHERNET | Intel I219-V | FULL | https://www.tonymacx86.com/threads/intel-i219-ethernet-drivers-for-skylake-100-series-motherboards-testing.180995/ |
| WLAN | Intel AC8265 | NO | To be replaced with BCM94352Z with FULL compatibility |
| BLUETOOTH | Intel AC8265 | YES | Fixes needed to make it work fully. To be replaced with BCM94352Z with FULL compatibility |
| EXPRESS CARD | | NO:DISABLED | |
| SD READER | | NO | Possible driver? https://www.insanelymac.com/forum/topic/321080-sineteks-driver-for-realtek-rtsx-sdhc-card-readers/ |
| PORTS | 4xUSB3.1 Gen 1 | YES | Need to be correctly setup through USBInjectAll.kext + custom SSDT |
| | 1xUSB C (Thunderbolt) | ? | Needs to be correctly tested and setup as above. Thunderbolt will probably never work, but USB C yes, objective is to make it a substitute for HDMI/Mini Displayport/VGA through Macbook cable adapters. Example of this: https://www.tonymacx86.com/threads/xps-9360-usb-c-to-hdmi-audio-still-not-working.216140/|
| | HDMI 1.4b | NO | Since Nvidia is disabled, this port connected to it can't work |
| | Mini Displayport 1.2a | NO | Since Nvidia is disabled, this port connected to it can't work |
| CAMERA | | FULL | |
| AUDIO | ALC3268 (Speakers + Internal Mic + Headphone/Mic Combo) | FULL | AppleALC.kect + Layout #29 as per: https://www.reddit.com/r/hackintosh/comments/4e23w6/guide_native_audio_with_clover_applealckext/ |
| KEYBOARD | | YES | Some keys need to be fixed/setup with SSDT patches |
| ULTRANAV | Trackpoint | YES | Needs to be fixed: movement is not smooth (it's blocky/jumpy). Also, center trackpoint button should be fixed since it's imprecise. |
| | Touchpad | FULL | |
| FP READER | | YES | USB device: needs to be disabled through USBInjectAll.kext + custom SSDT since not used to preserve battery |
| COLOR CALIBRATOR | | YES | USB device: needs to be disabled through USBInjectAll.kext + custom SSDT since not used to preserve battery |

## Software:

| Feature | Compatibility | Notes |
| ------------- | ------------- | ------------- |
| Sleep + Wake | NO | Needs to be fixed |
| Battery Status | FULL | https://www.tonymacx86.com/threads/guide-how-to-patch-dsdt-for-working-battery-status.116102/ |
| Brightness Control | FULL | https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/ |
| App Store | FULL | |
| iTunes | FULL | |
| iMessage | NO | Can't authenticate (probably needs payment method in account) EASY FIX but low priority |
| Siri | NO | Can't authenticate (probably needs payment method in account) EASY FIX but low priority |
| Facetime | NO | Can't authenticate (probably needs payment method in account) EASY FIX but low priority |

## Setup:
1) MOST IMPORTANT: https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093/
2) TBD
