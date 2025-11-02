# 🔌 HomePlugX

**HomePlugX** is a compact IoT smart plug built around the **ESP32** (or ESP32-S3) platform.  
It enables wireless control, timer, and scheduling of any 230 VAC appliance up to **10 A**, with built-in protection and energy monitoring capability.

---

## ⚙️ Features

- ✅ Wi-Fi control via ESP32 / ESP32-S3
- ⏱️ Timer and scheduling support (App-based)
- ⚡ Energy metering using HLW8012 / HLW8032
- 🔥 Relay control with transistor or MOSFET driver
- 🧰 Built-in surge and over-current protection
- 📱 Android app made using MIT App Inventor
- 💡 Compact, low-power, and safe for home use

---

## 🧩 Hardware Overview

| Section | Component | Function |
|----------|------------|-----------|
| **Power Input** | Fuse + MOV + NTC + X2 Cap | Surge & inrush protection |
| **AC-DC Conversion** | HLK-PM05 | 230 VAC → 5 VDC isolated |
| **Regulator** | SPX3819 / AMS1117 | 5 V → 3.3 V for ESP32 |
| **Relay** | HF46F (10 A) | Switches live line |
| **Driver** | 2N2222 / IRLML2502 | Relay drive transistor / MOSFET |
| **MCU** | ESP32-S3 Mini / ESP32-WROOM | Core controller with Wi-Fi + BT |
| **Energy Meter** | HLW8012 / HLW8032 | Measures current, voltage, power |
| **Enclosure** | Plastic housing | Insulated & compact plug body |

---

## 🔋 Electrical Ratings

| Parameter | Value |
|------------|--------|
| Input Voltage | 230 VAC ±10 % |
| Load Current | Up to 10 A (resistive) |
| Output Power | Up to 2.3 kW |
| Isolation | 3 kV (HLK-PM05) |
| Standby Power | < 1 W |

---

## 🧠 Software Features

- MQTT / HTTP communication  
- Local web control page  
- Countdown timer and real-time clock scheduling  
- OTA firmware update (optional)  
- Energy-usage reporting and overload cut-off  

---

## 🧰 Development Stack

- **Firmware:** Arduino IDE / ESP-IDF  
- **Mobile App:** MIT App Inventor  
- **PCB Design:** KiCad / EasyEDA  
- **Database / Visualization (optional):** InfluxDB + Grafana  
- **Version Control:** Git + GitHub  

---

## 🛠️ Getting Started

### 1. Hardware Setup
1. Assemble HLK-PM05, protection components, relay, and MCU as per schematic.  
2. Flash firmware using USB-to-UART converter.  
3. Power the board **only through isolation** during initial testing.

### 2. Firmware Flash
```bash
git clone https://github.com/yourusername/HomePlugX.git
cd HomePlugX
# open in Arduino IDE or ESP-IDF and upload
