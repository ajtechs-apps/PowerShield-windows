<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🛡️ PowerShield v1.0.0 — Production Release (x64)</title>
<style>
  :root {
    --primary: #0284c7;
    --primary-dark: #0369a1;
    --accent: #10b981;
    --dark: #0f172a;
    --darker: #020617;
    --surface: #1e293b;
    --surface-hover: #334155;
    --text: #f8fafc;
    --text-muted: #94a3b8;
    --border: #334155;
    --shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3), 0 4px 6px -2px rgba(0, 0, 0, 0.1);
    --radius: 12px;
  }

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    background: var(--darker);
    color: var(--text);
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1.5rem;
  }

  /* Header & Badges */
  header {
    padding: 3rem 0 2rem;
    border-bottom: 1px solid var(--border);
    margin-bottom: 2.5rem;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-bottom: 1.25rem;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    padding: 0.35rem 0.8rem;
    border-radius: 6px;
    font-size: 0.82rem;
    font-weight: 600;
    text-decoration: none;
    color: var(--text);
    background: var(--surface);
    border: 1px solid var(--border);
    transition: transform 0.2s, border-color 0.2s;
  }

  .badge:hover {
    transform: translateY(-2px);
    border-color: var(--primary);
  }

  .badge img {
    vertical-align: middle;
    margin-right: 0.4rem;
  }

  h1 {
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
    letter-spacing: -0.5px;
  }

  .subtitle {
    font-size: 1.05rem;
    color: var(--text-muted);
    margin-bottom: 0.5rem;
    font-weight: 500;
  }

  .tagline {
    font-style: italic;
    color: var(--text-muted);
    font-size: 0.95rem;
  }

  hr {
    border: none;
    height: 1px;
    background: var(--border);
    margin: 2.5rem 0;
  }

  /* Sections */
  section {
    margin-bottom: 2.75rem;
  }

  h2 {
    font-size: 1.4rem;
    font-weight: 700;
    margin-bottom: 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.6rem;
  }

  h3 {
    font-size: 1.15rem;
    font-weight: 700;
    margin-bottom: 0.75rem;
    color: var(--primary);
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  p {
    margin-bottom: 1rem;
    color: var(--text);
  }

  p strong {
    color: var(--text);
  }

  blockquote {
    border-left: 4px solid var(--primary);
    padding-left: 1rem;
    margin: 1rem 0;
    font-size: 1.1rem;
    color: var(--text-muted);
    font-style: italic;
    background: var(--surface);
    padding: 1rem 1.25rem;
    border-radius: 0 var(--radius) var(--radius) 0;
  }

  /* Feature Cards */
  .features {
    display: grid;
    gap: 1.25rem;
  }

  .feature {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.5rem;
    transition: border-color 0.2s, transform 0.2s;
  }

  .feature:hover {
    border-color: var(--surface-hover);
    transform: translateY(-2px);
  }

  .feature h3 {
    margin-bottom: 0.75rem;
    color: var(--text);
  }

  .feature ul {
    list-style: none;
    padding-left: 0;
  }

  .feature li {
    margin-bottom: 0.6rem;
    padding-left: 1.4rem;
    position: relative;
    color: var(--text);
  }

  .feature li::before {
    content: "▹";
    position: absolute;
    left: 0;
    color: var(--primary);
    font-weight: bold;
  }

  .feature li strong {
    color: var(--text);
  }

  /* Tables */
  .table-wrap {
    overflow-x: auto;
    margin-bottom: 1.5rem;
    border-radius: var(--radius);
    border: 1px solid var(--border);
    background: var(--surface);
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.95rem;
  }

  th, td {
    padding: 0.9rem 1rem;
    text-align: left;
    border-bottom: 1px solid var(--border);
  }

  th {
    background: var(--surface-hover);
    color: var(--text-muted);
    font-weight: 600;
    text-transform: uppercase;
    font-size: 0.8rem;
    letter-spacing: 0.5px;
  }

  tr:last-child td {
    border-bottom: none;
  }

  tr:hover {
    background: var(--surface-hover);
  }

  .download-cell a {
    color: var(--primary);
    text-decoration: none;
    font-weight: 600;
  }

  .download-cell a:hover {
    text-decoration: underline;
  }

  .size-cell {
    font-weight: 700;
    color: var(--accent);
  }

  /* Installation Steps */
  .steps {
    list-style: none;
    padding-left: 0;
  }

  .steps li {
    margin-bottom: 0.9rem;
    padding-left: 2.2rem;
    position: relative;
    color: var(--text);
  }

  .steps li::before {
    content: counter(step);
    counter-increment: step;
    position: absolute;
    left: 0;
    top: 0.05rem;
    width: 1.6rem;
    height: 1.6rem;
    background: var(--primary);
    color: var(--darker);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 0.9rem;
  }

  .steps {
    counter-reset: step;
  }

  code {
    font-family: "SF Mono", Monaco, Consolas, "Liberation Mono", monospace;
    background: var(--surface-hover);
    padding: 0.15rem 0.4rem;
    border-radius: 4px;
    font-size: 0.9em;
    color: var(--accent);
  }

  pre code {
    display: block;
    padding: 1rem;
    overflow-x: auto;
  }

  a {
    color: var(--primary);
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  .mobile-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.5rem;
    margin-top: 1rem;
  }

  .footer {
    margin-top: 3rem;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
    color: var(--text-muted);
    font-size: 0.9rem;
  }

  .footer a {
    color: var(--primary);
  }

  .footer a:hover {
    text-decoration: underline;
  }

  @media (max-width: 640px) {
    .container {
      padding: 0 1rem;
    }

    h1 {
      font-size: 1.4rem;
    }

    h2 {
      font-size: 1.2rem;
    }

    .badges {
      gap: 0.5rem;
    }

    .badge {
      font-size: 0.75rem;
      padding: 0.3rem 0.6rem;
    }

    table {
      font-size: 0.85rem;
    }

    th, td {
      padding: 0.7rem 0.85rem;
    }
  }
</style>
</head>
<body>
<div class="container">

  <header>
    <div class="badges">
      <a href="https://github.com/ajtechs/powershield-win/releases/tag/v1.0.0" class="badge" target="_blank" rel="noopener">
        <img src="https://img.shields.io/badge/Release-v1.0.0-0284c7.svg?style=flat-square" alt="Release v1.0.0">
      </a>
      <a href="https://github.com/ajtechs/powershield-win" class="badge" target="_blank" rel="noopener">
        <img src="https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011%20x64-blue.svg?style=flat-square" alt="Platform Windows 10 / 11 x64">
      </a>
      <a href="https://github.com/ajtechs/powershield-win" class="badge" target="_blank" rel="noopener">
        <img src="https://img.shields.io/badge/Framework-.NET%208.0%20%7C%20WinUI%203-0284c7.svg?style=flat-square" alt="Framework .NET 8.0 | WinUI 3">
      </a>
      <a href="LICENSE" class="badge" target="_blank" rel="noopener">
        <img src="https://img.shields.io/badge/License-MIT-emerald.svg?style=flat-square" alt="License MIT">
      </a>
    </div>

    <h1>🛡️ PowerShield v1.0.0 — Production Release (x64)</h1>
    <p class="subtitle">Next-Generation Windows System Diagnostics, Kernel-Grade Optimization &amp; Privacy Suite</p>
    <p class="tagline">Crafted with WinUI 3, Windows App SDK 1.6, and .NET 8 for high performance with zero bloat.</p>
  </header>

  <hr>

  <section>
    <h2>🌟 Executive Summary</h2>
    <p><strong>PowerShield v1.0.0</strong> is the inaugural production release of our unified Windows maintenance and diagnostics suite. Designed to replace fragmented legacy applets and aggressive third-party cleaning tools, PowerShield combines modern Fluent design with deep Win32, WMI, and native ACPI hardware interfaces.</p>
    <p>Whether you run an ultrabook requiring battery preservation or an overclocked workstation demanding zero micro-latencies, PowerShield delivers granular control without background telemetry or unwanted processes.</p>
  </section>

  <hr>

  <section>
    <h2>🚀 Key Feature Pillars</h2>
    <div class="features">
      <div class="feature">
        <h3>⚡ System Cleaner &amp; Memory Optimizer</h3>
        <ul>
          <li><strong>Multi-Level Storage Purge:</strong> Safely scans and reclaims gigabytes of disk space occupied by Windows temporary directories, DirectX shader caches, delivery optimization buffers, crash dumps, error reports, and icon thumbnail databases.</li>
          <li><strong>Kernel Working Set &amp; Standby Purge:</strong> Real-time memory pressure monitoring with instant working set reduction and kernel standby cache flushing via documented Win32 memory APIs.</li>
          <li><strong>Smart Whitelist Engine:</strong> Protects active user sessions, locked handles, and critical background services from unexpected termination.</li>
        </ul>
      </div>

      <div class="feature">
        <h3>🔋 Battery Health &amp; Power Orchestration</h3>
        <ul>
          <li><strong>Hardware Degradation Diagnostics:</strong> Queries ACPI battery rails via WMI to measure real-time wear percentage, factory design capacity, current full charge capacity, and lifetime charge cycles.</li>
          <li><strong>Instant Power Scheme Switching:</strong> Switch seamlessly between <strong>Balanced</strong>, <strong>High Performance</strong>, <strong>Power Saver</strong>, and <strong>Ultimate Performance</strong> without navigating the legacy Windows Control Panel.</li>
          <li><strong>Built-in Power Diagnostics:</strong> Single-click generation of native Windows HTML Battery Reports, 5-second Energy Audits, and Sleep Study traces.</li>
        </ul>
      </div>

      <div class="feature">
        <h3>🎮 Game Boost &amp; Latency Governor</h3>
        <ul>
          <li><strong>Low-Latency Governor:</strong> Completely suppresses CPU core down-clocking during intensive workloads by maximizing processor performance states.</li>
          <li><strong>Background Worker Parking:</strong> Automatically parks idle background tasks and diagnostic polling to eliminate frame drops and audio stutter during gaming.</li>
          <li><strong>Always-On-Top Floating Widget:</strong> Compact desktop pill displaying live CPU usage, RAM consumption, and network throughput with a tactile <strong>Boost</strong> button.</li>
        </ul>
      </div>

      <div class="feature">
        <h3>🔒 Privacy &amp; Telemetry Hardening</h3>
        <ul>
          <li><strong>Configurable Telemetry Protection:</strong> Three hardening levels (<strong>Minimal</strong>, <strong>Balanced</strong>, and <strong>Maximum Privacy</strong>) that disable telemetry logging, diagnostic consumers, and user feedback agents.</li>
          <li><strong>Ad &amp; Tracker Suppression:</strong> Disables advertising identifiers, customer experience improvement program (CEIP) hooks, and diagnostic tracking services.</li>
          <li><strong>Reversible Staging:</strong> Restore default Windows configuration settings at any time with a single click.</li>
        </ul>
      </div>

      <div class="feature">
        <h3>🛠️ System Repair &amp; Component Health</h3>
        <ul>
          <li><strong>Windows Component Store Repair:</strong> Automated execution of DISM (<code>CheckHealth</code>, <code>ScanHealth</code>, <code>RestoreHealth</code>) to repair corrupted Windows system images.</li>
          <li><strong>System File Checker (SFC):</strong> Integrates <code>sfc /scannow</code> with real-time log output and post-scan health reporting.</li>
          <li><strong>Process &amp; Startup Manager:</strong> Deep inspection of active process hierarchies, memory working sets, and autostart application boot impact ratings.</li>
        </ul>
      </div>

      <div class="feature">
        <h3>🌐 Network Tools &amp; App Management</h3>
        <ul>
          <li><strong>Network &amp; DNS Suite:</strong> Live bandwidth throughput telemetry, active TCP/UDP socket monitoring, one-click DNS cache flushing, and DoH (DNS-over-HTTPS) encrypted resolver status.</li>
          <li><strong>Modern Uninstaller:</strong> Batch uninstaller supporting both traditional Win32 desktop software and provisioned Windows UWP/AppX packages with leftover file scanning.</li>
        </ul>
      </div>
    </div>
  </section>

  <hr>

  <section>
    <h2>📦 Distribution Packages &amp; Downloads</h2>
    <p>PowerShield is distributed in two official 64-bit packaging flavors:</p>
    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Distribution Package</th>
            <th>Download Link</th>
            <th>File Size</th>
            <th>Description</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><strong>PowerShield Standalone (x64)</strong></td>
            <td class="download-cell"><a href="https://github.com/ajtechs/powershield-win/releases/download/v1.0.0/PowerShield-v1.0.0-Standalone-x64.zip" target="_blank" rel="noopener">Download <code>.zip</code></a></td>
            <td class="size-cell">~85 MB</td>
            <td><strong>Self-Contained:</strong> All .NET 8 runtime libraries and Windows App SDK assets are bundled. Requires no external prerequisites. Ideal for portable USB storage and enterprise offline workstations.</td>
          </tr>
          <tr>
            <td><strong>PowerShield Lightweight (x64)</strong></td>
            <td class="download-cell"><a href="https://github.com/ajtechs/powershield-win/releases/download/v1.0.0/PowerShield-v1.0.0-Lightweight-x64.zip" target="_blank" rel="noopener">Download <code>.zip</code></a></td>
            <td class="size-cell">~15 MB</td>
            <td><strong>Framework-Dependent:</strong> Minimal footprint utilizing shared Windows runtimes. Features an automated smart bootstrapper that checks, downloads, and silently installs required prerequisites in seconds.</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <hr>

  <section>
    <h2>📋 System Requirements</h2>
    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Specification</th>
            <th>Minimum / Recommended</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><strong>Operating System</strong></td>
            <td>Windows 11 (all editions) or Windows 10 (version 2004 / Build 19041 or newer)</td>
          </tr>
          <tr>
            <td><strong>Architecture</strong></td>
            <td>64-bit (<code>x64</code> / <code>AMD64</code> / <code>Intel 64</code>)</td>
          </tr>
          <tr>
            <td><strong>Memory</strong></td>
            <td>2 GB RAM minimum (4 GB+ recommended)</td>
          </tr>
          <tr>
            <td><strong>Storage</strong></td>
            <td>30 MB free space (Lightweight) / 120 MB free space (Standalone)</td>
          </tr>
          <tr>
            <td><strong>User Privileges</strong></td>
            <td>Standard user privileges (prompts for UAC elevation only when executing kernel repairs or DISM maintenance)</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <hr>

  <section>
    <h2>🔧 Installation &amp; Usage Guide</h2>

    <h3>Standalone Package</h3>
    <ol class="steps">
      <li>Download <code>PowerShield-v1.0.0-Standalone-x64.zip</code>.</li>
      <li>Extract the archive to any desired folder (e.g. <code>C:\Program Files\PowerShield</code> or a portable USB drive).</li>
      <li>Double-click <code>PowerShield.exe</code> to launch immediately.</li>
    </ol>

    <h3>Lightweight Package</h3>
    <ol class="steps">
      <li>Download <code>PowerShield-v1.0.0-Lightweight-x64.zip</code>.</li>
      <li>Extract the archive to any folder.</li>
      <li>Double-click <code>PowerShield.exe</code>.</li>
      <li>If your system is missing the <strong>Microsoft .NET 8 Desktop Runtime</strong> or <strong>Windows App SDK 1.6 Runtime</strong>, the modern <strong>Prerequisites Setup</strong> window will appear automatically.</li>
      <li>Click <strong>"Install Missing Prerequisites"</strong> — the launcher will automatically download and install the required components silently.</li>
      <li>Click <strong>"Launch PowerShield"</strong> once complete.</li>
    </ol>
  </section>

  <hr>

  <section>
    <h2>📱 Mobile Companion</h2>
    <div class="mobile-card">
      <p><strong>PowerShield for Android:</strong> Android companion app featuring kernel cache purging, background app hibernation, battery health monitoring, and zero-telemetry device tuning.</p>
      <p><em>Repository:</em> <a href="https://github.com/ajtechs/powershield-android" target="_blank" rel="noopener">github.com/ajtechs/powershield-android</a></p>
    </div>
  </section>

  <hr>

  <section>
    <h2>🤝 Contributing, Support &amp; Feedback</h2>
    <ul>
      <li><strong>Bug Reports &amp; Feature Requests:</strong> Please file issues via the <a href="https://github.com/ajtechs/powershield-win/issues" target="_blank" rel="noopener">GitHub Issue Tracker</a>.</li>
      <li><strong>Source Code:</strong> <a href="https://github.com/ajtechs/powershield-win" target="_blank" rel="noopener">github.com/ajtechs/powershield-win</a></li>
      <li><strong>Star the Repo:</strong> If you find PowerShield useful, consider giving us a star ⭐ on GitHub!</li>
    </ul>
  </section>

  <footer class="footer">
    <p>PowerShield v1.0.0 &middot; Built with WinUI 3, Windows App SDK 1.6, and .NET 8</p>
  </footer>

</div>
</body>
</html>
