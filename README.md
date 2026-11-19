<p align="center">
  <img src="assets/fortfocus-logo.png" alt="FortFocus Logo" width="450">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Windows-10%20%2F%2011%20(64--bit)-0078d4?style=flat-square&logo=windows" alt="Platform Supported">
  <img src="https://img.shields.io/badge/Version-v0.13.0-00b4d8?style=flat-square" alt="Current Release">
  <img src="https://img.shields.io/badge/License-Proprietary%20Freeware-blueviolet?style=flat-square" alt="Deployment License">
  <img src="https://img.shields.io/badge/Privacy-Local%20First%20(No%20Data%20Collected)-success?style=flat-square" alt="Privacy First">
</p>

# FortFocus — Fortified Productivity & Focus Enforcement for Windows

**FortFocus** is an advanced, tamper-resistant desktop productivity and focus enforcement suite for Windows. Designed for professionals, developers, and students who require uncompromising concentration, FortFocus combines deep OS-level distraction blocking with **JIMMY**, an intelligent, voice-enabled focus companion.

---

## Key Features

- **Hardened Distraction Blocking**
  - **Application Guard:** Blocks games, social media clients, and distraction executables during active sessions.
  - **Web Barrier:** Blocks distracting domains and websites at the network layer without requiring intrusive browser extensions.
  - **Tamper-Resistant Windows Service:** Runs as a dedicated background Windows service (`fortfocus-service`), ensuring focus enforcement cannot be trivially bypassed via Task Manager or process termination.

- **JIMMY — Intelligent Focus Companion**
  - **Holographic Interactive Avatar:** Real-time animated state visualizer responding to your productivity rhythms.
  - **Offline Voice Recognition:** Powered by embedded native Whisper (`whisper.cpp`) for fast, private, 100% offline speech-to-text.
  - **Adaptive Coaching & Guidance:** Optional natural-language AI integration (Google Gemini & Groq) providing personalized work-session breakdown, focus coaching, and task tracking.
  - **Hardware DPAPI Encryption:** All optional AI credentials are encrypted using Windows Data Protection API (DPAPI) and never stored in plaintext.

- **Configurable Session & Break Scheduling**
  - Flexible session lengths (Pomodoro or custom deep-work blocks).
  - Enforced rest intervals with automated break transitions.
  - Non-distracting system tray controls and real-time session HUD.

---

## System Requirements

| Specification | Requirement |
| :--- | :--- |
| **Operating System** | Windows 10 (64-bit, Version 1903+) or Windows 11 (64-bit) |
| **Architecture** | x86_64 / x64 |
| **Privileges** | Administrator rights (required once during setup to install the background service) |
| **Memory (RAM)** | 4 GB minimum (8 GB recommended when using voice recognition) |
| **Disk Space** | ~250 MB free space |
| **Network** | Offline-capable (Internet required only if enabling cloud AI coaching features) |

---

## Download & Verification

### Step 1: Download the Official Installer
Download the latest official installer package and verification hash from the **[Releases](https://github.com/rushirajkakade909-cell/FortFocus/releases)** tab:
- **Installer:** [`FortFocusSetup-0.13.0.exe`](https://github.com/rushirajkakade909-cell/FortFocus/releases/download/v0.13.0/FortFocusSetup-0.13.0.exe)
- **Checksum File:** [`FortFocusSetup-0.13.0.exe.sha256`](https://github.com/rushirajkakade909-cell/FortFocus/releases/download/v0.13.0/FortFocusSetup-0.13.0.exe.sha256)

### Step 2: Cryptographic Checksum Verification
To confirm installer integrity and ensure the binary has not been modified or corrupted, compute its SHA-256 hash in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\FortFocusSetup-0.13.0.exe
```

Expected SHA-256 digest:
```text
d1529e53544e249b1ba688d1be231e86a5b4b5c4145df48bef9667e5707e2592
```

---

## Installation & Setup

1. **Launch Installer:**  
   Run `FortFocusSetup-0.13.0.exe`.
2. **User Account Control (UAC):**  
   Click **Yes** when prompted to allow FortFocus to register and start the background enforcement service.
3. **Follow the Setup Wizard:**  
   Choose your installation directory and finish installation.

> [!NOTE]
> **Windows SmartScreen Notice**  
> Because FortFocus is a newly released independent application, Windows SmartScreen may present a blue dialog stating *"Windows protected your PC"*.
> 1. Click **More info**.
> 2. Click **Run anyway**.
> 
> *FortFocus executables are strictly audited, non-telemetry, and clean of third-party bundlers or adware.*

4. **Launch Application:**  
   Once setup completes, FortFocus will start in your Windows notification tray and display the dashboard.

---

## Quick Start Guide

1. **Configure Your Blocklist:**
   - Open FortFocus and navigate to the **Blocking** tab.
   - Add distracting applications (e.g., `discord.exe`, `steam.exe`) or target domains (e.g., `youtube.com`, `reddit.com`).
2. **Start a Focus Block:**
   - Set your session timer (e.g., 25 or 50 minutes) and click **Start Focus Session**.
   - Your blocklist is immediately activated and protected by the background service.
3. **Interact with JIMMY:**
   - Click the **JIMMY** tab to interact with your focus companion.
   - Use voice or text to check your session progress, set goals, or ask for break coaching.
4. **Configure AI Credentials (Optional):**
   - If you wish to enable conversational AI guidance, open **Settings $\rightarrow$ Credentials**.
   - Enter your personal Google Gemini or Groq API key.
   - Keys are immediately encrypted at rest using your Windows user DPAPI profile.

---

## Privacy & Security

- **Local-First Architecture:** All timers, application blocks, and speech recognition engines execute entirely on your local machine.
- **Zero Telemetry:** FortFocus does not transmit telemetry, tracking cookies, or usage analytics.
- **Hardware-Backed Encryption:** Any API keys provided for cloud LLM features are protected by Windows DPAPI encryption keys tied to your Windows user account.

---

## Support & Vulnerability Disclosure

If you encounter an issue or wish to report a security vulnerability, please refer to our [Security Policy](SECURITY.md) or open an issue on the [GitHub Issues](https://github.com/rushirajkakade909-cell/FortFocus/issues) page.
