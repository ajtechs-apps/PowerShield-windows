# 🛡️ PowerShield v1.0.0 — Production Release (x64)

> **Next-Generation Windows System Diagnostics, Kernel-Grade Optimization & Privacy Suite**  
> *Crafted with WinUI 3, Windows App SDK 1.6, and .NET 8 for high performance with zero bloat.*

[![Release](https://img.shields.io/badge/Release-v1.0.0-0284c7.svg?style=flat-square)](https://github.com/ajtechs/powershield-win/releases/tag/v1.0.0)
[![Target](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011%20x64-blue.svg?style=flat-square)](https://github.com/ajtechs/powershield-win)
[![Runtime](https://img.shields.io/badge/Framework-.NET%208.0%20%7C%20WinUI%203-0284c7.svg?style=flat-square)](https://github.com/ajtechs/powershield-win)
[![License](https://img.shields.io/badge/License-MIT-emerald.svg?style=flat-square)](LICENSE)

---

## 🌟 Executive Summary

**PowerShield v1.0.0** is the inaugural production release of our unified Windows maintenance and diagnostics suite. Designed to replace fragmented legacy applets and aggressive third-party cleaning tools, PowerShield combines modern Fluent design with deep Win32, WMI, and native ACPI hardware interfaces.

Whether you run an ultrabook requiring battery preservation or an overclocked workstation demanding zero micro-latencies, PowerShield delivers granular control without background telemetry or unwanted processes.

---

## 🚀 Key Feature Pillars

### 1. ⚡ System Cleaner & Memory Optimizer
* **Multi-Level Storage Purge**: Safely scans and reclaims gigabytes of disk space occupied by Windows temporary directories, DirectX shader caches, delivery optimization buffers, crash dumps, error reports, and icon thumbnail databases.
* **Kernel Working Set & Standby Purge**: Real-time memory pressure monitoring with instant working set reduction and kernel standby cache flushing via documented Win32 memory APIs.
* **Smart Whitelist Engine**: Protects active user sessions, locked handles, and critical background services from unexpected termination.

### 2. 🔋 Battery Health & Power Orchestration
* **Hardware Degradation Diagnostics**: Queries ACPI battery rails via WMI to measure real-time wear percentage, factory design capacity, current full charge capacity, and lifetime charge cycles.
* **Instant Power Scheme Switching**: Switch seamlessly between **Balanced**, **High Performance**, **Power Saver**, and **Ultimate Performance** without navigating the legacy Windows Control Panel.
* **Built-in Power Diagnostics**: Single-click generation of native Windows HTML Battery Reports, 5-second Energy Audits, and Sleep Study traces.

### 3. 🎮 Game Boost & Latency Governor
* **Low-Latency Governor**: Completely suppresses CPU core down-clocking during intensive workloads by maximizing processor performance states.
* **Background Worker Parking**: Automatically parks idle background tasks and diagnostic polling to eliminate frame drops and audio stutter during gaming.
* **Always-On-Top Floating Widget**: Compact desktop pill displaying live CPU usage, RAM consumption, and network throughput with a tactile **Boost** button.

### 4. 🔒 Privacy & Telemetry Hardening
* **Configurable Telemetry Protection**: Three hardening levels (**Minimal**, **Balanced**, and **Maximum Privacy**) that disable telemetry logging, diagnostic consumers, and user feedback agents.
* **Ad & Tracker Suppression**: Disables advertising identifiers, customer experience improvement program (CEIP) hooks, and diagnostic tracking services.
* **Reversible Staging**: Restore default Windows configuration settings at any time with a single click.

### 5. 🛠️ System Repair & Component Health
* **Windows Component Store Repair**: Automated execution of DISM (`CheckHealth`, `ScanHealth`, `RestoreHealth`) to repair corrupted Windows system images.
* **System File Checker (SFC)**: Integrates `sfc /scannow` with real-time log output and post-scan health reporting.
* **Process & Startup Manager**: Deep inspection of active process hierarchies, memory working sets, and autostart application boot impact ratings.

### 6. 🌐 Network Tools & App Management
* **Network & DNS Suite**: Live bandwidth throughput telemetry, active TCP/UDP socket monitoring, one-click DNS cache flushing, and DoH (DNS-over-HTTPS) encrypted resolver status.
* **Modern Uninstaller**: Batch uninstaller supporting both traditional Win32 desktop software and provisioned Windows UWP/AppX packages with leftover file scanning.

---

## 📦 Distribution Packages & Downloads

PowerShield is distributed in two official 64-bit packaging flavors:

| Distribution Package | Download Link | File Size | Description |
| :--- | :---: | :---: | :--- |
| **PowerShield Standalone (x64)** | [Download `.zip`](https://github.com/ajtechs/powershield-win/releases/download/v1.0.0/PowerShield-v1.0.0-Standalone-x64.zip) | **~85 MB** | **Self-Contained**: All .NET 8 runtime libraries and Windows App SDK assets are bundled. Requires no external prerequisites. Ideal for portable USB storage and enterprise offline workstations. |
| **PowerShield Lightweight (x64)** | [Download `.zip`](https://github.com/ajtechs/powershield-win/releases/download/v1.0.0/PowerShield-v1.0.0-Lightweight-x64.zip) | **~15 MB** | **Framework-Dependent**: Minimal footprint utilizing shared Windows runtimes. Features an automated smart bootstrapper that checks, downloads, and silently installs required prerequisites in seconds. |

---

## 📋 System Requirements

| Specification | Minimum / Recommended |
| :--- | :--- |
| **Operating System** | Windows 11 (all editions) or Windows 10 (version 2004 / Build 19041 or newer) |
| **Architecture** | 64-bit (`x64` / `AMD64` / `Intel 64`) |
| **Memory** | 2 GB RAM minimum (4 GB+ recommended) |
| **Storage** | 30 MB free space (Lightweight) / 120 MB free space (Standalone) |
| **User Privileges** | Standard user privileges (prompts for UAC elevation only when executing kernel repairs or DISM maintenance) |

---

## 🔧 Installation & Usage Guide

### Standalone Package
1. Download `PowerShield-v1.0.0-Standalone-x64.zip`.
2. Extract the archive to any desired folder (e.g. `C:\Program Files\PowerShield` or a portable USB drive).
3. Double-click `PowerShield.exe` to launch immediately.

### Lightweight Package
1. Download `PowerShield-v1.0.0-Lightweight-x64.zip`.
2. Extract the archive to any folder.
3. Double-click `PowerShield.exe`.
4. If your system is missing the **Microsoft .NET 8 Desktop Runtime** or **Windows App SDK 1.6 Runtime**, the modern **Prerequisites Setup** window will appear automatically.
5. Click **"Install Missing Prerequisites"** — the launcher will automatically download and install the required components silently.
6. Click **"Launch PowerShield"** once complete.

---

## 📱 Mobile Companion

* **PowerShield for Android**: Android companion app featuring kernel cache purging, background app hibernation, battery health monitoring, and zero-telemetry device tuning.  
  *Repository*: [github.com/ajtechs-apps/powershield-android](https://github.com/ajtechs-apps/powershield-android)

---

## 🤝 Contributing, Support & Feedback

* **Bug Reports & Feature Requests**: Please file issues via the [GitHub Issue Tracker](https://github.com/ajtechs-apps/powershield-windows/issues).
* **Source Code**: [github.com/ajtechs-apps/powershield-windows](https://github.com/ajtechs-apps/powershield-windows)
* **Star the Repo**: If you find PowerShield useful, consider giving us a star ⭐ on GitHub!

