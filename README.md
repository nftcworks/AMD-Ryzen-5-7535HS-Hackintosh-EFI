# Acer Nitro V15 (ANV15-41-R2M0) Hackintosh

A complete EFI folder and guide for running macOS on the Acer Nitro V15. 

## System Specifications

| Component | Specification | Status in macOS |
| :--- | :--- | :--- |
| **Model** | Acer Nitro V15 (ANV15-41-R2M0) | Supported |
| **CPU** | AMD Ryzen 5 7535HS | Supported |
| **iGPU** | AMD Radeon 660M | Supported (via NootedRed) |
| **dGPU** | NVIDIA GeForce RTX 2050 | **Unsupported** (Disabled via boot-args/SSDT) |
| **RAM** | 8GB DDR5 | Supported |
| **Storage** | 512GB PCIe NVMe SSD | Supported |
| **Display** | 15.6" FHD (1920x1080) @ 144Hz | Supported |
| **Audio** | [Insert Audio Codec/ALC ID] | Supported |
| **Network** | [Insert Wi-Fi/BT Card Model] | Supported |

## 🛠️ What's Working
* [x] AMD Radeon iGPU Hardware Acceleration
* [x] Native Refresh Rate (144Hz)
* [x] Audio (Internal Speakers & Headphone Jack)
* [x] Wi-Fi and Bluetooth
* [x] Keyboard and Trackpad (with multi-touch gestures)
* [x] All USB Ports mapped correctly
* [x] Battery Percentage Readout
* [x] Sleep/Wake

## ⚠️ What's Not Working
* [ ] NVIDIA RTX 2050 (macOS does not support modern NVIDIA GPUs)
* [ ] HDMI Out (If routed directly through the disabled NVIDIA dGPU)
* [ ] [Add any other specific bugs or unsupported features]

## ⚙️ BIOS Settings
Before booting the USB, ensure the following BIOS settings are configured:
* **Secure Boot:** Disabled
* **Fast Boot:** Disabled
* **SATA Mode:** AHCI
* **TPM:** Disabled (if causing boot issues)

## 🚀 Installation Notes
1. Create a macOS installer USB using the standard method.
2. Replace the `EFI` folder on the USB's EFI partition with the one from this repository.
3. Boot from the USB and install macOS.
4. Once installed, mount your internal drive's EFI partition and copy the `EFI` folder over to boot without the USB.

*Note: You must generate your own SMBIOS data (Serial Number, Board Serial, UUID, and MAC Address) using GenSMBIOS before signing into any Apple services.*

## 🙏 Credits
* [Acidanthera](https://github.com/acidanthera) for OpenCore and essential kexts.
* [ChefKissInc](https://github.com/ChefKissInc) for NootedRed.
* [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the comprehensive OpenCore Install Guide.
