# 💓 Heart Rate Reactive Fluid Dress

A wearable tech fashion project that pumps colored fluid through tubes on a dress in sync with the wearer's heart rate. Built for a fashion design college project.

---

## 🎯 Project Overview

This project combines biometric sensing and fashion design. A pulse sensor reads the wearer's heart rate and controls a peristaltic pump that pushes colored fluid through transparent silicone tubes sewn into a dress. The fluid flows faster when the heart beats faster, creating a visual representation of the wearer's heartbeat.

---

## 🎥 Demo

> Place finger on sensor → fluid starts flowing through dress tubes in sync with heartbeat!

---

## 🧰 Components

| Component | Specification |
|---|---|
| Microcontroller | Arduino Nano R3 (ATmega328P) |
| Heart Rate Sensor | MAX30102 Pulse Oximeter |
| MOSFET | IRLZ44N (Logic Level) |
| Pump | Peristaltic Dosing Pump 5V/6V |
| Power | Powerbank (5V) + 4x AA batteries |
| Tubing | Silicone tube (3-5mm inner diameter) |
| Fluid | Distilled water + red/orange food coloring |

---

## 📐 Circuit Wiring

### Power
- Powerbank USB → Arduino USB port
- 4x AA batteries (+) → IRLZ44N Drain
- 4x AA batteries (-) → Arduino GND

### Heart Rate Sensor (MAX30102)
- VIN → Arduino 3.3V
- GND → Arduino GND
- SDA → Arduino A4
- SCL → Arduino A5
- INT → Arduino D2

### Pump Control (IRLZ44N)
- Gate → Arduino D3~
- Drain → AA battery + AND Pump RED wire
- Source → Arduino GND
- Pump BLACK → Arduino GND

### Common GND
All GND pins connected together:
- Arduino GND
- AA battery (-)
- IRLZ44N Source
- Pump BLACK wire

---

## 📚 Libraries Required

Install via Arduino IDE → Sketch → Include Library → Manage Libraries:

- **SparkFun MAX3010x Pulse and Proximity Sensor Library** by SparkFun Electronics

---

## ⚙️ Arduino IDE Settings

- Board: **Arduino Nano**
- Processor: **ATmega328P (Old Bootloader)**
- Baud Rate: **115200**

---

## 🔌 How It Works

```
Finger on sensor
      ↓
MAX30102 reads IR value
      ↓
Arduino calculates BPM
      ↓
PWM signal sent to IRLZ44N Gate
      ↓
IRLZ44N switches pump ON/OFF
      ↓
Fluid flows through dress tubes
      ↓
Visual heartbeat on dress! 💓
```

---

## ⚠️ Important Notes

- MAX30102 must be connected to **3.3V only** — never 5V (will damage sensor)
- All GND pins must be connected together (common ground)
- Keep finger **still** on sensor for accurate BPM reading
- Wait 15-20 seconds for BPM to stabilize
- Use **fresh Duracell AA batteries** for best pump performance
- Arduino Nano clone requires **CH340 driver** on Windows

---

## 🔋 Battery Life

Using fresh Duracell AA batteries:
- Total current draw: ~550mA
- Battery capacity: ~3000mAh
- Estimated runtime: **3-4 hours** ✅

---

## 👗 Fashion Integration

- Silicone tubes routed through dress structure
- Arduino + batteries hidden in waistband
- Sensor attached to finger or wrist
- Fluid: distilled water + red/orange food coloring
- Rocker switch for ON/OFF control

---

## 🛒 Where to Buy (India)

- **Robocraze.com** — Arduino Nano, MAX30102, IRLZ44N
- **Amazon India** — Peristaltic pump, silicone tubing
- **Local electronics shop** — AA batteries, food coloring

---

## 👨‍💻 Built With

- Arduino IDE 2.0
- SparkFun MAX30105 Library
- C++ (Arduino)

---

## 📄 License

MIT License — free to use and modify for educational purposes.

---

## 🙏 Acknowledgements

Built as a collaboration project of Dept of ECE, SOET CMR UNIVERSITY and School of fashion designing , SOD CMR UNIVERSITY


