# HP EliteBook 840 G3 · OpenCore Hackintosh

Intel Core i5-6300U | HD 530 | 8 GB DDR4 | OpenCore 1.0.4

![CPU](https://img.shields.io/badge/CPU-Intel_Core_i5_6300U-0071C5)
![GPU](https://img.shields.io/badge/GPU-Intel_HD_530-0071C5)
![OpenCore](https://img.shields.io/badge/OpenCore-1.0.4-9cf)
![Status](https://img.shields.io/badge/Status-Working-success)

---

## Hardware

| Component | Specification |
|:----------|:--------------|
| CPU | Intel Core i5-6300U |
| GPU | Intel UHD Graphics 530 |
| RAM | 8 GB DDR4 2133 MHz |
| Touchpad | Synaptics SMBus |
| Audio | Conexant CX20724 |
| Wi-Fi / Bluetooth | Intel Wireless-AC 8260 |
| Ethernet | Intel I219-LM |

## BIOS Settings

| Option | Value |
|:-------|:-----:|
| Intel SGX | Disabled |
| Fast Boot | Disabled |
| Boot Mode | UEFI |
| Legacy Boot | Disabled |
| Secure Boot | Disabled |
| Hyperthreading | Enabled |
| VT-x | Enabled |
| VT-d | Disabled |
| Video Memory | 64 MB |

## Driver Status

| Feature | Status | Feature | Status |
|:--------|:------:|:--------|:------:|
| Audio | ✅ Working | Wi-Fi | ✅ Working |
| Ethernet | ✅ Working | Bluetooth | ✅ Working |
| Graphics | ✅ Working | USB | ✅ Working |
| Touchpad | ✅ Working | Sleep | ✅ Working |

---

## Screenshots

**Model:**

| | |
|:---:|:---:|
| ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/31dd2db566519738586f4b34485a8bbed05ec0bc/Model/1.png) | ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/31dd2db566519738586f4b34485a8bbed05ec0bc/Model/2.png) |

**System:**

| | |
|:---:|:---:|
| ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/1.png) | ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/2.png) |
| ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/3.png) | ![](https://github.com/WT2072861996/EFI-HP-EliteBook-840-G3-Hackintosh/blob/1e1262dc4ca7b685a06feaaaf50b58c831b1561b/After%20installation/4.png) |

## Installation

1. Configure BIOS per above
2. Mount EFI partition with OpenCore Configurator
3. Copy EFI folder to EFI partition
4. Boot from USB → OpenCore → Install macOS
