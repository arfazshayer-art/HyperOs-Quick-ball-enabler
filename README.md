# HyperOs-Quick-ball-enabler
"A systemless Magisk/KernelSU module to forcefully bypass shared UID restrictions and enable native Touch Assistant (Quick Ball) on HyperOS 3."

# 🪐 HyperOS Touch Assistant Unlocker

[![Magisk](https://img.shields.io/badge/Magisk-Module-00AF9C.svg?style=flat-square)](#) 
[![HyperOS](https://img.shields.io/badge/Tested_on-HyperOS_3-blue.svg?style=flat-square)](#)
[![Status](https://img.shields.io/badge/Status-Stable-success.svg?style=flat-square)](#)

A meticulously crafted systemless module designed to forcefully bypass the `INSTALL_PARSE_FAILED_BAD_SHARED_USER_ID` restriction and seamlessly inject the native MIUI/HyperOS Touch Assistant (Quick Ball) into the system partition.

## 📌 Architecture & Mechanism
Modern HyperOS architecture strictly heavily limits privileged applications via shared system UIDs (`android.uid.system`). Attempting to install flagship-exclusive APKs on restricted devices natively results in signature verification failures. 

This module resolves the namespace and permission barrier by:
1. **Systemless Injection:** Utilizing Magisk/KernelSU overlay technology to mount the application directly into `/system/priv-app/`.
2. **Permission overriding:** Automatically assigning the strict `0644` (rw-r--r--) file permissions and `0755` directory permissions required by the Android environment for seamless execution.
3. **Bootloop Prevention:** Operates dynamically without modifying the immutable physical system partition (EROFS/OverlayFS safe).

## 🚀 Compatibility
- **OS Environment:** Strictly developed and tested on **HyperOS 3**.
- **Root Manager:** Magisk (v24.0+) or KernelSU.
- **Device Dependency:** Universal (Tested heavily on specific low/mid-tier hardware lacking native support).

## ⚙️ Installation Guide
1. Download the latest `TouchAssistant_Enabler.zip` from the [Releases](../../releases) section.
2. Open your Root Manager (Magisk / KernelSU).
3. Navigate to the **Modules** tab.
4. Select **Install from storage** and choose the downloaded `.zip` file.
5. Wait for the flashing process and permission allocation to complete.
6. **Reboot** your device.
7. Navigate to `Settings > Additional Settings > Quick Ball` to verify.

## ⚠️ Disclaimer & Warning
**USE AT YOUR OWN RISK.** Modifying system-level applications and bypassing predefined manufacturer hardware restrictions can lead to unexpected UI crashes or bootloops if your device framework lacks the core dependencies. 
- I am not responsible for bricked devices, corrupted partitions, or thermonuclear war.
- Always keep a safe mode protocol or custom recovery ready before flashing system-level modules.

## 👨‍💻 Author
**Mahir** *System Modification & Security Enthusiast*
