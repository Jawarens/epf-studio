# EPF STUDIO

An interactive visualizer, logic engine analyzer, and CAN bus signalbank matrix decoder for Addio EPF vehicle control profiles and systems.

<p align="center">
  <a href="https://ko-fi.com/F0T028FQJQ">
    <img src="https://ko-fi.com/img/githubbutton_sm.svg" alt="ko-fi" />
  </a>
</p>

---

## 🚀 Quick Start (Single-File / Zero Installation)

This project is built as a **100% self-contained single-file application**:
- Double-click **`Run_EPF_Studio.bat`** (or open [`index.html`](index.html) directly in any modern web browser: Edge, Chrome, Firefox, Safari).
- **Clean Runtime Startup**: Launches directly into a sleek, clean workspace ready for your own Addio EPF vehicle files.
- **No dependencies, no runtime installations, and no internet connection required.**

---

## 🌟 Key Features

1. **Universal Addio EPF XML Decoder & Runtime Visualizer**:
   - Clean, neutral startup state: drop any `.epf` or `.xml` file to automatically decode hardware modules, pinouts, and logic trees.
   - Dynamic hardware node reconstruction for Master, Slave, Switch Panels, and Input Units.
   - Built-in on-demand demo: click **`↺ Demo`** in the top bar to test with the bundled multi-node fleet sample.
   - Live drag-and-drop file zone allowing you to load multiple profile configurations simultaneously.

2. **🌲 VU Logic Port Tree (`Hotkey: V`)**:
   - Visualizes all 16 Virtual Output gates (VU1–VU16).
   - Port conditions dynamically display satisfied checkmarks (`✓ 1`) and blocked crosses (`❌ 0`).
   - Animated directional flow arrows show active signal paths vs. red blocked interlock paths.
   - Dedicated filter chains for **🚨 Blue Emergency Chain**, **⚠️ Amber Warning Chain**, and **✈️ Runway / Priority Sequences**.
   - Integrated live test toolbar for toggling input pins (`HK B1`, `HK B2`, `In 5`, `In 6`, `In 7`, `In 8`).

3. **📊 CAN Signalbank Matrix (`Hotkey: M`)**:
   - Full 35-slot CAN ID broadcast map between Master Node 91 and Slaves 92 & 93.
   - Live signal value updates during interactive simulation.
   - Multi-profile diff comparison and raw XML section inspector.

4. **⚡ Live Interactive Logic Simulator**:
   - Toggle switches on the breadboard or activate operational presets:
     - `1`: Roof Blue Strobes
     - `2`: Directional Blue Strobes
     - `3`: Front Flasher Strobes
     - `4`: Amber Hazard Warning
     - `0`: Reset All Inputs (All Off)
   - Dynamic wire glow and current pulse visualization.

5. **🎛️ Section & Tracking Filters (`Hotkey: F`)**:
   - Dynamically pack, filter, and isolate Hand Controller (HK) keys, 22-channel input unit ports, terminal pins, and switch panels.

6. **🌐 Full Bilingual Support**:
   - Toggle seamlessly between **🇸🇪 Svenska** and **🇬🇧 English**.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :---: | :--- |
| **`V`** | Toggle **🌲 VU Port Tree** modal |
| **`M`** | Toggle **📊 CAN Matrix & Multi-File** modal |
| **`F`** | Toggle **🎛️ Section & Tracking Filters** drawer |
| **`Escape`** | Close whichever modal or drawer is open |
| **`R`** | Reset canvas pan and zoom |
| **`1` – `4`** | Activate operational lighting presets |
| **`0`** | Reset all inputs and presets |

---

## ☕ Support the Project

If this tool helps with your vehicle control and CAN diagnostics, please consider supporting development!

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F0T028FQJQ)
