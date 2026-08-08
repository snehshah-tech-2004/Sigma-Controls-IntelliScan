# Sigma Controls | IntelliScan 

![Version](https://img.shields.io/badge/version-1.3-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![License](https://img.shields.io/badge/license-Proprietary-red.svg)

**IntelliScan v1.3** is an advanced industrial telemetry and data acquisition software engineered by **Sigma Controls**. Designed for precision and reliability, it interfaces with Modbus/RS485 hardware to log, visualize, and report multi-channel sensor data in real-time. 

---

### ✨ Key Features & Capability Matrix

*   **Multi-Channel Acquisition:** Simultaneously track up to 24 channels per slave station. Supports unified tracking for industrial metrics including Temperature, Pressure, Humidity, Flow Speed, and Energy consumption (kWh).
*   **Dynamic Smart Instrumentation:** The dashboard automatically adapts channel widget icons (High-Temperature, Pressure, Humidity, Speed, Energy) depending on the channel's target parameter type.
*   **Intelligent Watchdog Loop:** A rugged asynchronous communication thread (`Worker`) features automatic Modbus connection recovery. If an RS485 line experiences dropouts, the system continuously auto-retries and safely resumes logging without crashing the main UI.
*   **Sensor Fault Code Isolation:** Detects and flags open or damaged sensor lines instantly. Open lines are displayed directly on the UI dashboard as a blinking `OPE` safety warning rather than invalid zero data.
*   **Dual-Layer Storage Architecture:** Features simultaneous logging to time-stamped CSV structured log files and a synchronized local SQLite database backend for maximum data redundancy.
*   **Accelerated Historical Replay:** Built-in interactive historical replay mode (triggered via `Ctrl+R`) loads saved data logs into the viewport. Allows engineers to fast-forward playbacks at 1x, 2x, or 10x speeds to watch machine runs unfold visually.
*   **Advanced Plotting Workspaces:** Equipped with hardware-accelerated twin plotting dashboards (`pyqtgraph`): a Full Run Historical View and a rolling "Last 10 Readings" transient analysis frame. Both grids feature manual time-range filters, start/stop boundary flags, and interactive crosshair hover coordinates.
*   **Interactive Permanent Data Markers:** Drop up to 5 individual structural markers onto analysis graphs via left-click for deep investigation. Supports complete drag-and-drop relocation, right-click erasure, and custom multi-channel selection dialog frames.
*   **Enterprise Reporting Engine:** Export publication-ready, landscape multi-channel trend lines and portrait tabular row books straight to PDF (`FPDF`). Supports customized company letterhead graphics (up to 980 x 230 pixels) and variable 3-line header descriptions.
*   **Automated Audit Logs:** Keeps a secure local log of all administrative actions, system updates, logins, and recovery events for verification.

---

### 🛠 Technology Stack

*   **GUI Framework:** PyQt5
*   **Hardware Communication:** pymodbus (Modbus RTU Serial)
*   **Real-Time Rendering:** pyqtgraph
*   **Historical Analysis & PDF Generation:** matplotlib, mplcursors, FPDF, Pillow (PIL)
*   **Data Processing:** pandas, numpy
*   **Security & Licensing:** winreg, hashlib, getmac

---

### 🎚️ License Tiers & Scale Limits

IntelliScan scales dynamically based on your license tier, which is verified via the Windows Registry and an encrypted hardware signature. Restricted IDs are securely locked out of the runtime selection panel.

| License Tier | Max Allowed Slaves | Targeted Environment | Feature Set Included |
| :--- | :--- | :--- | :--- |
| **Starter Plan** | **2 Slave IDs** (ID-1 to ID-2) | Small-Scale Test Labs | Active channels 1-24 per slave, full CSV logging, full dual-plot graphics, basic PDF reporting. |
| **Professional Plan** | **4 Slave IDs** (ID-1 to ID-4) | Medium Assembly Lines | All Starter features, extended slave limits, letterhead customization, advanced filtering tools. |
| **Enterprise Plan** | **8 Slave IDs** (ID-1 to ID-8) | Large-Scale Industrial Plants | Complete telemetry access, advanced data tips, multi-channel selection overlays, maximum reporting limits. |

---

### 📦 Compilation & Build Instructions

IntelliScan is distributed as a compiled Windows executable to ensure easy deployment in industrial environments. To build the executable from the `main_3.py` source, use the following PyInstaller command. 

*Note: This command aggressively excludes unnecessary machine-learning libraries to optimize the payload size.*

```bash
python -m PyInstaller main_3.py --onefile --windowed --icon=SIGMA_ICON.ico --name "Sigma Controls - IntelliScan v1.3" --optimize=2 --hidden-import=license_check --hidden-import=updater --hidden-import=id_sett --hidden-import=db_manager --hidden-import=login --hidden-import=ui_2 --hidden-import=pyqtgraph --hidden-import=matplotlib --hidden-import=pymodbus --hidden-import=mplcursors --hidden-import=getmac --exclude-module=keras --exclude-module=tensorflow --exclude-module=torch --exclude-module=torchvision --exclude-module=torchaudio --exclude-module=sklearn --exclude-module=PyQt6 --exclude-module=jupyter --exclude-module=jupyterlab --exclude-module=astropy --exclude-module=altair --exclude-module=docker --exclude-module=gTTS --exclude-module=pytesseract --exclude-module=ultralytics --exclude-module=twilio --collect-all=matplotlib --collect-all=pyqtgraph --add-data "SIGMA_ICON.svg;." --add-data "SIGMA_cache.png;." --add-data "license_check.py;." --add-data "updater.py;." --add-data "id_sett.py;." --add-data "login.py;." --add-data "ui_2.py;." --add-data "ico_rc.py;." --add-data "db_manager.py;." --distpath "Sigma Controls - IntelliScan v1.3" --clean --noconfirm
```

---

### 📥 Installation & Updates

1. Download the latest `Sigma.Controls.-.IntelliScan.v1.3.zip` from the **[Releases](../../releases)** tab.
2. Extract the contents to your local directory.
3. Run `Sigma Controls - IntelliScan v1.3.exe` and activate your license via the integrated fingerprinting system.

*Note: The software features an automated background updater that silently checks for new configurations or patches every 24 hours.*

---

### 📞 Support

For hardware integration, custom licensing overrides, or technical support, please contact Sigma Controls:
*   **Website:** [www.sigmacontrolsindia.com](https://www.sigmacontrolsindia.com)
*   **Email:** sales@sigmacontrolsindia.com
*   **Phone:** +91 95100 31871 | +91 79902 73727

---
*© 2026 Sigma Controls. All Rights Reserved.*
