<div align="center">

# 🔧 Hardware Design Portfolio

### Arham Amir — Electronics Engineering @ NED University, Karachi

[![KiCad](https://img.shields.io/badge/KiCad-9.0-blue?style=for-the-badge)](https://www.kicad.org/)
[![ESP32](https://img.shields.io/badge/ESP32-IoT-red?style=for-the-badge)](https://www.espressif.com/)
[![STM32](https://img.shields.io/badge/STM32-Embedded-03234B?style=for-the-badge)](https://www.st.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Arham_Amir-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/arham-amir)

> Production-grade PCB designs — schematic capture to fabrication-ready Gerbers.
> All boards designed in **KiCad 9** with full DRC/ERC compliance, BOM, and 3D renders.

</div>

---

## 📁 Repository Structure

```
hardware-portfolio/
│
├── 📂 01-STM32WB-4Layer-USB-RF/
├── 📂 02-ESP32-Power-Monitor/
├── 📂 03-ESP32-C3-IoT-DevBoard/
├── 📂 04-AC-Energy-Analyzer/
├── 📂 05-DeskBuddy-v2/
├── 📂 06-MSPM0-DevBoard/
├── 📂 07-ESP8266-Water-Controller/
├── 📂 08-ESP32-S3-IoT-Board/
├── 📂 09-STM32-BlackPill/
├── 📂 10-NE555-Analog-Automation/
├── 📂 11-LM386-Audio-Amplifier/
├── 📂 12-ESP32-S3-ENS210-Sensor/
│
└── README.md
```

Each project folder contains: `schematic/` · `pcb-layout/` · `gerbers/` · `bom/` · `3d-renders/`

---

## 🚀 Projects

---

### 1. STM32WB 4-Layer PCB — USB 2.0 + 2.4 GHz RF

> **Mixed-signal layout with dual ground planes, impedance-controlled USB, and RF-optimized routing.**

| MCU | Layers | Interface | Tool |
|---|---|---|---|
| STM32WB (Cortex-M4 + M0+) | 4-layer | USB Type-C FS + 2.4 GHz chip antenna | KiCad 9 |

- Stack-up: Signal / GND / GND / Power — dual ground planes for EMI shielding
- Impedance-controlled USB D+/D− via KiCad 9 field solver
- Uninterrupted ground under RF section · u.FL test point · ESD protection

📂 [`01-STM32WB-4Layer-USB-RF/`](./01-STM32WB-4Layer-USB-RF/)

---

### 2. ESP32 4-Layer Power Monitoring System

> **5-channel real-time energy monitoring with IoT web dashboard.**

| MCU | Channels | Interface | Tool |
|---|---|---|---|
| ESP32 WROOM | 5 (voltage + current + relay) | WiFi web dashboard | KiCad 9 |

- Precision current sensing with dedicated analog front-end
- Mixed-signal layout — analog sensing isolated from digital noise
- Thermal management and power plane partitioning

📂 [`02-ESP32-Power-Monitor/`](./02-ESP32-Power-Monitor/)

---

### 3. ESP32-C3 IoT Development Board

> **Custom dev board with 12V → 5V → 3.3V power chain and companion USB-to-UART programmer.**

| MCU | Power Input | Load | Tool |
|---|---|---|---|
| ESP32-C3 WROOM | 12V | 5A, T90 relay, fuse protected | KiCad 9 |

- Complete power chain: Boost → 5V, LDO → 3.3V
- Companion USB-to-UART programmer as a separate PCB
- Real-time IoT dashboard for load monitoring and control

📂 [`03-ESP32-C3-IoT-DevBoard/`](./03-ESP32-C3-IoT-DevBoard/)

---

### 4. AC Energy Analyzer

> **Standalone module measuring Vrms, Irms, power, power factor, and frequency on an OLED display.**

| MCU | Voltage Sense | Current Sense | Display |
|---|---|---|---|
| Arduino Nano | ZMPT101B | ACS712 | SH1106 OLED |

- Calibrated sensor front-end for accurate real-world measurements
- Multi-page OLED UI with chunked sampling for button responsiveness

📂 [`04-AC-Energy-Analyzer/`](./04-AC-Energy-Analyzer/)

---

### 5. DeskBuddy v2 — ESP32-C3 Smart Display

> **Desk companion with animated OLED eyes, weather, clock, and custom PCB replacing a pile of breakout boards.**

| MCU | Power IC | Sensor | Display |
|---|---|---|---|
| ESP32-C3 | IP5306 (charge + boost) | TTP223 touch (on-board) | OLED |

- IP5306 replaced three separate modules (charger + protection + boost)
- Live battery indicator · auto-syncing clock · real-time weather icons
- TTP223 touch sensor etched directly onto the board

📂 [`05-DeskBuddy-v2/`](./05-DeskBuddy-v2/)

---

### 6. MSPM0 Development Board (TI Cortex-M0+)

> **First TI MSPM0 design — clean power delivery, USB connectivity, and careful peripheral routing in KiCad 9.**

| MCU | Interface | Focus | Tool |
|---|---|---|---|
| TI MSPM0 (Cortex-M0+) | USB + UART | Decoupling, crystal layout, USB diff pairs | KiCad 9 |

- First design on the TI MSPM0 ecosystem
- Datasheet-compliant decoupling and crystal placement

📂 [`06-MSPM0-DevBoard/`](./06-MSPM0-DevBoard/)

---

### 7. ESP8266 Autonomous Water Controller

> **IoT water management system — prevents dry-running, overflow, and motor burnout with a non-blocking state machine.**

| MCU | Sensors | Interface | Cost |
|---|---|---|---|
| ESP8266 | Dual-level float sensors | Real-time web dashboard | ~$25 |

- Dual-sensor verification before motor activation
- 2-minute grace period + 30-minute cooldown for motor longevity
- Fail-safe redundancy · manual override via web UI

📂 [`07-ESP8266-Water-Controller/`](./07-ESP8266-Water-Controller/)

---

### 8. ESP32-S3 General-Purpose IoT Board (4-Layer)

> **Feature-rich 4-layer IoT platform with environmental sensing, expansion headers, and RGB indicator.**

| MCU | Sensor | Expansion | Stack-up |
|---|---|---|---|
| ESP32-S3 (8MB Flash) | Si7021 Temp/Humidity | QWIIC + SPI headers | 4-layer |

- USB-C for power and programming · BOOT/RESET buttons · RGB LED
- CP2104 USB-to-UART · power relay · fused power supply

📂 [`08-ESP32-S3-IoT-Board/`](./08-ESP32-S3-IoT-Board/)

---

### 9. STM32 "Black Pill" — 2-Layer Custom Board

> **First complete STM32 PCB — schematic to routed layout, DRC clean, ready for fabrication.**

| MCU | Interface | Layers | Tool |
|---|---|---|---|
| STM32F4xx | USB Micro Type-B | 2-layer | KiCad 9 |

- LDO 3.3V regulation · reset and BOOT configuration circuits
- Proper D+/D− routing · decoupling strategy throughout

📂 [`09-STM32-BlackPill/`](./09-STM32-BlackPill/)

---

### 10. NE555 Analog Automation Controller

> **Fully analog process automation — no microcontroller, just three NE555 ICs and transistor logic controlling AC loads.**

| ICs | Sensors | Outputs | Purpose |
|---|---|---|---|
| 3× NE555, BC547 | Conductivity probes | 5 relays | 30-min interval pump + tank-full detection |

- IC1: 30-minute astable interval · IC2: flow detection latch · IC3: final appliance state
- BC547 stage detects tank-full via top-level probes
- No code, no bootloader — pure analog logic

📂 [`10-NE555-Analog-Automation/`](./10-NE555-Analog-Automation/)

---

### 11. LM386 Audio Amplifier

> **University project — simulated, PCB-designed, and oscilloscope-verified audio amplifier.**

| IC | Verification | PCB |
|---|---|---|
| LM386 | Simulation + oscilloscope | Custom KiCad layout |

- Simulated before implementation · signal integrity verified at each stage
- Suitable for small speakers, guitar amps, and portable audio

📂 [`11-LM386-Audio-Amplifier/`](./11-LM386-Audio-Amplifier/)

---

### 12. ESP32-S3 + ENS210 Environmental Sensor Node

> **Compact IoT sensor node for precision temperature and humidity monitoring over I2C.**

| MCU | Sensor | Interface |
|---|---|---|
| ESP32-S3-Mini-1N8 | ENS210 | I2C · ultra-low power |

- Ideal for smart agriculture, weather stations, and indoor climate control

📂 [`12-ESP32-S3-ENS210-Sensor/`](./12-ESP32-S3-ENS210-Sensor/)

---

## 🛠 Tools & Stack

| Category | Details |
|---|---|
| PCB Design | KiCad 9 — Schematic, Layout, DRC, Gerber Export, 3D Viewer |
| Simulation | LTspice, Multisim |
| Microcontrollers | ESP32, ESP32-C3, ESP32-S3, STM32WB, STM32F4, MSPM0, ESP8266, Arduino Nano |
| Protocols | USB 2.0, I2C, UART, SPI, 2.4 GHz RF |
| Fabrication | Gerber files, BOM, Pick & Place ready |

---

## 📬 Contact

| | |
|---|---|
| 📧 Email | arhamamir117@gmail.com |
| 💼 LinkedIn | [linkedin.com/in/arham-amir](https://linkedin.com/in/arham-amir) |
| 🐙 GitHub | [github.com/arham-amir](https://github.com/arham-amir) |
| 📍 Location | Karachi, Pakistan |

---

<div align="center">

*All designs are original work. Gerbers, schematics, BOM, and 3D renders included in each project folder.*

⭐ Star this repo if you find it useful!

</div>
