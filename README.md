================================================================================
                           POWERSHIELD WINDOWS SUITE
  Kernel-grade system maintenance, telemetry hardening, and real-time hardware orchestration
================================================================================

Platform      : Windows 10 (Build 19041+) & Windows 11 (All Builds)
Architecture  : x64 Native Binary
Framework     : .NET 8.0 Windows | WinUI 3 (Windows App SDK 1.6)
License       : MIT Open Source
Version       : v1.0.0 Release
Author        : ajtechs
Repository    : https://github.com/ajtechs-apps/PowerShield-windows
Android App   : https://github.com/ajtechs-apps/PowerShield-android (Comming soon)
Support       : https://ko-fi.com/ajtechs

--------------------------------------------------------------------------------
1. OVERVIEW
--------------------------------------------------------------------------------
PowerShield is a modern, high-performance Windows optimization and diagnostic 
workstation designed for Windows 10 and 11. Built from the ground up using C# 12, 
.NET 8, and WinUI 3 (Windows App SDK 1.6), PowerShield delivers native speed, 
responsive Fluent Design (Mica and Desktop Acrylic backdrops), and deep hardware-level 
control without third-party junk, telemetry ingestion, or aggressive background services.

Whether you are tuning gaming latencies, reclaiming gigabytes of disk space, 
purging hidden memory leaks, hardening OS privacy policies, or managing network 
routing, PowerShield consolidates 20+ specialized system utilities into a unified, 
privacy-first desktop application.

--------------------------------------------------------------------------------
2. KEY PILLARS
--------------------------------------------------------------------------------
* 100% Private & Open Source:
  Zero tracking, zero phone-home metrics, zero ads. Every scan and clean operation 
  runs 100% locally on your machine.

* Native .NET 8 Performance:
  Compiled as a native x64 binary utilizing high-precision hardware timers and 
  asynchronous multi-threaded kernel APIs.

* True Fluent Design:
  Full Windows 11 Mica Alt / Desktop Acrylic support with seamless Dark and 
  Light theme adaptation.

* Zero Antivirus Heuristics:
  Designed with clean, sanctioned Windows APIs (NtQuerySystemInformation, DISM, ACPI) 
  to ensure 0 heuristic false positives.

--------------------------------------------------------------------------------
3. CORE MODULES & FEATURES
--------------------------------------------------------------------------------
1. Interactive Dashboard:
   - Live hardware telemetry: multi-core CPU %, RAM allocation, Network up/down throughput, GPU status
   - Real-time hardware activity graph with interactive tooltips and historical delta inspection
   - Algorithmic System Health Grade (0-100%, A+ to F) with prioritized recommendations
   - Quick Actions Bar for instant memory flush, DNS purge, disk clean, and security status

2. 1-Touch Cleaner & Storage Optimizer:
   - Intelligent Presets: Quick Clean, Safe Recommended, Deep Thorough, Gaming Pre-Flight, Developer Purge
   - Duplicate Files Finder: Multi-threaded MD5/SHA256 duplicate content detection across drives
   - Empty Folder Remover: Recursive empty directory scanner with dry-run preview and batch deletion
   - Large Files Finder: Interactive disk visualizer identifying large files (>100MB, >1GB, >5GB)

3. RAM Cleaner & Memory Governor:
   - Standby memory list purge (clears cached standby lists without losing unsaved data)
   - Process working set trimming (trims active pages across idle background tasks back to disk)
   - Windows filesystem cache flush
   - Unwanted programs & memory bloatware detector with one-click trim/stop
   - Optimization audit & verification reporting exact before/after memory reclaimed

4. Windows Tweaks & Component Manager (97+ Tweaks):
   - UI & Shell: Classic context menu, remove shortcut arrows, disable '- Shortcut' suffix, Start Menu Bing search
   - Privacy & Bloatware: Disable telemetry (DiagTrack), Cortana, advertising ID, location tracking, feedback
   - Performance & Gaming: Ultimate Performance power scheme, disable mouse acceleration, Xbox Game Bar overlay
   - DISM Optional Features: Toggle Hyper-V, WSL, Windows Sandbox, TFTP, and Telnet with admin elevation

5. Battery Health & Power Orchestration:
   - ACPI degradation diagnostics: Charge capacity, design capacity, cycle count, cell wear percentage
   - Windows energy scheme switcher: Balanced, High Performance, Power Saver, Ultimate Performance
   - One-click HTML Battery Report generation, 5-second Energy Audit, and Sleep Study

6. Network Tools & DNS Optimization:
   - Encrypted DNS (DoH) switching: Cloudflare DNS (1.1.1.1), Google Public DNS (8.8.8.8), Quad9 (9.9.9.9), DHCP
   - Live ICMP ping latency, DNS socket query latency, active listening ports, traceroute, and adapter resets

7. VPN & Privacy Shield (Cloudflare WARP):
   - Native Cloudflare WARP client orchestration with connection status indicators and wireguard routing toggles

8. App Uninstaller & Software Updates:
   - Winget Package Manager: Search, upgrade, or bulk-update installed Windows applications
   - Deep Uninstaller: Cleanly uninstall Win32 software and UWP/MSIX packages with residual file cleanup

9. Floating Desktop Widget:
   - Always-on-top telemetry pill displaying live CPU, RAM, and Network speeds
   - One-Click Boost: Instant memory trimming directly from the desktop widget
   - Windows 11 acrylic blur backdrop with custom DPI scaling

10. PowerShield for Android (Companion):
    - a. Cache cleaner: Multi-level app cache & thumbnail purge
    - b. Hibernate apps: Freeze background apps & wakelocks
    - c. Battery manager: Cycle health curves & extreme saver mode
    - d. App Manager: Batch uninstaller, split-APK backup & privacy audit
    - e. Network manager: Throughput monitor & DoH encrypted resolver
    - f. Storage manager: Space treemap & duplicate locator
    - g. Junk cleaner: Empty folders, residual uninstalled files & obsolete APKs

--------------------------------------------------------------------------------
4. INSTALLATION & USAGE
--------------------------------------------------------------------------------
Standalone Release (Recommended):
1. Download the latest PowerShield release from GitHub:
   https://github.com/ajtechs/powershield-win/releases
2. Extract the archive and launch PowerShield.exe.
3. (Optional) Click the elevation shield in the top titlebar to unlock Administrator
   privileges for kernel tweaks, DISM repair, and driver management.

Building From Source:
Prerequisites:
- Visual Studio 2022 (v17.8 or newer) with .NET Desktop Development and Windows App SDK
- .NET 8.0 SDK (x64)

Build commands:
  git clone https://github.com/ajtechs/powershield-win.git
  cd powershield-win
  dotnet restore PowerShield.sln
  dotnet build PowerShield.csproj -c Release -p:Platform=x64
  dotnet test PowerShield.Tests/PowerShield.Tests.csproj -c Debug -p:Platform=x64
  ./bin/x64/Release/PowerShield.exe

--------------------------------------------------------------------------------
5. SECURITY & PRIVACY GUARANTEE
--------------------------------------------------------------------------------
- Zero Telemetry Collection: No analytical payloads, crash reporting pings, or 
  telemetry logs are ever transmitted to external servers.
- Local Execution: All diagnostic queries, registry adjustments, and file cleanups 
  execute exclusively on your local hardware.
- System Restore Protection: Automatically create Windows System Restore points 
  before applying major tweaks or deep uninstalls.
- Antivirus Integrity: Clean, sanctioned Windows APIs without packers or obfuscators, 
  ensuring 0 false-positive alerts on Windows Defender, Bitdefender, and enterprise EDRs.

--------------------------------------------------------------------------------
6. LICENSE
--------------------------------------------------------------------------------
MIT License - Copyright (c) 2026 ajtechs

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

================================================================================
Crafted with precision by ajtechs · Built for Windows 10 & 11
================================================================================

