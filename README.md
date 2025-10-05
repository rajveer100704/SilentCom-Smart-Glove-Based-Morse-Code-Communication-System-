# 🕶️ SilentCom  
### Smart Glove-Based Morse Code Communication System for Soldiers  

[![Platform](https://img.shields.io/badge/Platform-ESP8266-blue)](https://en.wikipedia.org/wiki/ESP8266)
[![LoRa](https://img.shields.io/badge/Module-SX1278-green)](https://www.semtech.com/products/wireless-rf/lora-connect/sx1278#)
[![Language](https://img.shields.io/badge/Language-C%2B%2B%20%7C%20Arduino-orange)](#https://docs.arduino.cc/arduino-cloud/guides/arduino-c/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](#https://opensource.org/license/mit)
[![VIDEO Demo](https://img.shields.io/badge/Watch-Demo-red?logo=youtube)](https://drive.google.com/file/d/1w4CoAyrYkdDPH6CXtkASXW0NoOLKaA-y/view?usp=drivesdk)

---

## 🔍 Overview
**SilentCom** is a **glove-integrated, silent communication system** designed for **soldiers and defense personnel** operating in covert or high-noise environments.  
It allows users to transmit **Morse code-based messages** using **finger taps**, which are converted into **encrypted LoRa signals** and sent over long distances — enabling **silent, reliable, and low-power communication**.

---

## 🎥 Project Demonstration

> [![SilentCom Demo](https://img.youtube.com/vi/YOUR_VIDEO_ID_HERE/0.jpg)](https://drive.google.com/file/d/1w4CoAyrYkdDPH6CXtkASXW0NoOLKaA-y/view?usp=drivesdk))

---

## ⚙️ Features
- 🔦 **Tap-to-Transmit Input** — Ambient light sensor detects tap gestures as Morse code.  
- 🧠 **Finite State Machine (FSM) Morse Parser** — Converts tap sequences into symbols and text.  
- 📡 **LoRa + ESP8266 Communication** — Enables encrypted, long-range data transmission.  
- 🔐 **Encrypted Messaging** — Adds a security layer to prevent data interception.  
- 🔋 **Deep Sleep + Wake-on-Tap** — Power-optimized for long field operations.  
- 💡 **LED/Haptic Feedback** — Confirms message transmission and acknowledgment.  

---

## 🧩 Hardware Setup

| Component | Description |
|------------|-------------|
| **ESP8266 NodeMCU** | Main controller for transmission & signal logic |
| **LoRa SX1278 Module** | Handles encrypted long-range wireless data |
| **Ambient Light Sensor** | Detects tap gestures (replacing FSR sensor) |
| **Arduino Uno** | Simulates receiver side with LED feedback |
| **LED / Buzzer / Vibration Motor** | Provides feedback confirmation |
| **Power Source** | 3.3V or 5V Li-ion module |
| **Glove Assembly** | Mounts sensors and modules for wearable form |

---

## 🧠 System Architecture

```text
[Tap / Light Sensor] 
        ↓
[Morse FSM Parser]
        ↓
[Encoded Message]
        ↓
[LoRa Transmitter → Receiver]
        ↓
[LED / Haptic Feedback]

🛰️ The transmitter detects tap patterns → encodes as Morse → sends via LoRa SX1278 → receiver decodes and provides feedback.
---

# 🚀 Getting Started

### 🔧 Prerequisites
- Arduino IDE
- ESP8266 board package
- LoRa Library (by Sandeep Mistry)
- Basic Morse understanding

### 📥 Setup
```bash
# Clone repository
git clone https://github.com/rajveer100704/SilentCom.git
cd SilentCom

1.Open SilentCom.ino in Arduino IDE
2.Connect ESP8266 + LoRa SX1278
3.Upload transmitter and receiver code
4.Test tap detection and LoRa communication in Serial Monitor

---

##🔋 Power Optimization

SilentCom uses:

Deep Sleep cycles between messages
Interrupt-based tap wake-up
Optimized LoRa duty cycles
Result → ultra-low power consumption suitable for long missions.

🔒 Future Enhancements

📲 Android App for Morse-to-Text decoding
🧭 Multi-node mesh network for team comms
🎧 Richer haptic patterns for different message types
⚙️ AES-level encryption layer for tactical security

