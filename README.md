# 🎮 xretro — Open Source Handheld Console (RK3566)

xretro is an open-source handheld gaming console project based on the Rockchip RK3566 platform.  
The goal of this project is to build a modular, upgradeable, and developer-friendly handheld console, while documenting the full hardware and software bring-up process.

---

## 📌 Overview

This project explores the design of a portable gaming console using a compute-module-based architecture.  
Unlike most commercial handhelds, xretro is designed with **modularity and long-term upgradeability** in mind.

The system is built around an RK3566 compute module, combined with a custom baseboard integrating display, controls, and peripherals.

---

## 🧠 Hardware Architecture

### Core Platform

- SoC: RK3566  
- Memory: LPDDR4 (200p, BGA200_15R00X10R00X0R90)  
- PMIC: RK817  
- Flash: eMMC (BGA200 package)  

The schematic design is based on:

- Tablet Schematics for RK3566

---

### 🧩 Modular Design (Key Feature)

The console adopts a **compute module + carrier board** architecture:

- Current module: Luckfox Core3566  
- Future upgrade path:
  - Swap compute module only  
  - Minimal hardware changes  
  - Software adaptation required  

This makes xretro different from most existing handheld consoles, which are typically monolithic designs.

---

### 🎮 Controls

- D-pad (left)  
- ABXY buttons (right)  
- Dual analog joysticks  
- L / R shoulder buttons  

Horizontal (landscape) layout for a classic handheld experience.

---

### 🖥 Display

- 3.5" MIPI DSI display  
- Resolution: 640 × 480  

This panel is similar to those used in devices such as:

- Anbernic RG353P  
- R36S  

Future plans include using a larger display for better user experience.

---

### 🔌 Peripherals

- microSD card  
- 3.5 mm audio jack  
- USB power supply  

Bluetooth is currently not included due to regulatory complexity (CE compliance concerns in EU).

---

## 💻 Software Stack

Planned software architecture:

- Base system:
  - Rockchip / Luckfox Linux (RK3566 support)
- Frontend:
  - EmulationStation (or similar)
- Features:
  - GPIO-based input mapping (buttons & joysticks)
  - Emulator integration  

---

## 🚧 Project Status

- [x] Hardware architecture defined  
- [x] Compute module integration (Luckfox Core3566)  
- [ ] Baseboard design  
- [ ] Display bring-up (MIPI DSI)  
- [ ] Input subsystem (GPIO / ADC)  
- [ ] Software integration  
- [ ] Mechanical design  

---

## 🎯 Goals

- Build a fully functional open-source handheld console  
- Document hardware bring-up (especially MIPI DSI debugging)  
- Provide a reusable reference design for RK3566-based devices  
- Enable future upgrades via modular architecture  

---

## 📷 Preview

Add images in `docs/images/` and reference them like this:

![front](docs/images/front.jpg)  
![back](docs/images/back.jpg)

---

## 🤝 Contributing

Contributions, discussions, and suggestions are welcome.

---

## 📄 License

TBD

---

## 🧠 Author Notes

This project is also a personal exploration of:

- Embedded Linux bring-up  
- Display interface debugging (MIPI DSI)  
- Modular hardware design  
