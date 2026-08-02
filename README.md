# Sigma Controls | IntelliScan 

![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
![License](https://img.shields.io/badge/license-Proprietary-red.svg)

**IntelliScan** is an advanced industrial telemetry and data acquisition software developed by **Sigma Controls**. Designed for precision and reliability, it interfaces with Modbus/RS485 hardware to log, visualize, and report multi-channel sensor data in real-time.

---

### ✨ Key Features & Capability Matrix

* **Multi-Channel Acquisition:** Simultaneously track up to 24 channels per slave station. Supports unified tracking for industrial metrics including Temperature, Pressure, Humidity, Flow Speed, and Energy consumption (kWh).
* **Dynamic Smart Instrumentation:** The dashboard automatically adapts channel widget icons (High-Temperature, Pressure, Humidity, Speed, Energy) depending on the channel's target parameter type.
* **Intelligent Watchdog Loop:** A rugged communication thread features automatic Modbus connection recovery. If an RS485 line experiences dropouts, the system continuously auto-retries, auto-reconnects, and safely resumes logging without crashing.
* **Sensor Fault Code Isolation:** Detects and flags open or damaged sensor lines instantly. Open lines are displayed directly on the UI dashboard as a blinking `OPE` safety warning rather than invalid zero data.
* **Dual-Layer Storage Architecture:** Features simultaneous logging to time-stamped CSV structured log files and a synchronized local SQLite database backend for maximum data redundancy.
* **Accelerated Historical Replay:** Built-in interactive historical replay mode (triggered via `Ctrl+R`) loads saved data logs into the viewport. Allows engineers to fast-forward playbacks at 1x, 2x, or 10x speeds to watch machine runs unfold visually.
* **Advanced Plotting Workspaces:** Equipped with twin high-refresh plotting dashboards: a Full Run Historical View and a rolling "Last 10 Readings" transient analysis frame. Both grids feature manual time-range filters, start/stop boundary flags, and interactive crosshair hover coordinates.
* **Interactive Permanent Data Markers:** Drop up to 5 individual structural markers onto analysis graphs via left-click for deep investigation. Supports complete drag-and-drop relocation, right-click erasure, and custom multi-channel selection dialog frames that alert you if channel data points overlap at the selected timestamp.
* **Enterprise Reporting Engine:** Export publication-ready, landscape multi-channel trend lines and portrait tabular row books straight to PDF. Supports customized company letterhead graphics (up to 980 x 230 pixels) and variable 3-line header descriptions.
* **Automated Audit Logs:** Keeps a secure local log of all administrative actions, system updates, logins, and recovery events for verification.

---

### 🎚️ License Tiers & Scale Limits

IntelliScan scales dynamically based on your license tier verified via the Windows Registry and encrypted hardware signature. Restricted IDs are completely locked out of both the runtime selection panel and the configuration menu:

| License Tier | Max Allowed Slaves | Targeted Environment | Feature Set Included |
| :--- | :--- | :--- | :--- |
| **Starter Plan** | **2 Slave IDs** (ID-1 to ID-2) | Small-Scale Test Labs | Active channels 1-24 per slave, full CSV logging, full dual-plot graphics, basic PDF reporting. |
| **Professional Plan** | **4 Slave IDs** (ID-1 to ID-4) | Medium Assembly Lines | All Starter features, extended slave limits, letterhead customization, advanced filtering tools. |
| **Enterprise Plan** | **8 Slave IDs** (ID-1 to ID-8) | Large-Scale Industrial Plants | Complete telemetry access, advanced data tips, multi-channel selection overlays, maximum reporting limits. |

---

### 📦 Installation & Updates

IntelliScan is distributed as a compiled Windows executable. 
To install or update:
1. Download the latest `Sigma.Controls.-.IntelliScan.zip` from the **[Releases](../../releases)** tab.
2. Extract the contents to your desired local directory.
3. Run `Sigma Controls - IntelliScan v1.1.exe` and activate your license via the integrated fingerprinting system.

*Note: Existing users will receive update prompts automatically upon launching the software.*

---

### 📞 Support

For hardware integration, licensing, or technical support, please contact Sigma Controls:
* **Website:** [www.sigmacontrolsindia.com](https://www.sigmacontrolsindia.com)
* **Email:** sales@sigmacontrolsindia.com
* **Phone:** +91 95100 31871 | +91 79902 73727

---
*© 2026 Sigma Controls. All Rights Reserved.*
