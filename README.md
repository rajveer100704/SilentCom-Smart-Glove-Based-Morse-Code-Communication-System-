# 🕶️ SilentCom  
### Smart Glove-Based Morse Code Communication System for Soldiers  

[![Platform](https://img.shields.io/badge/Platform-ESP8266-blue)](https://en.wikipedia.org/wiki/ESP8266)
[![LoRa](https://img.shields.io/badge/Module-SX1278-green)](https://www.semtech.com/products/wireless-rf/lora-connect/sx1278#)
[![Language](https://img.shields.io/badge/Language-C%2B%2B%20%7C%20Arduino-orange)](#)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](#)
[![VIDEO Demo](https://img.shields.io/badge/Watch-Demo-red?logo=youtube)](#demo)

---

## 🔍 Overview
**SilentCom** is a **glove-integrated, silent communication system** designed for **soldiers and defense personnel** operating in covert or high-noise environments.  
It allows users to transmit **Morse code-based messages** using **finger taps**, which are converted into **encrypted LoRa signals** and sent over long distances — enabling **silent, reliable, and low-power communication**.

---

## 🎥 Project Demonstration

> 🎬 **YouTube Video:** [Watch the Live Demo](https://youtu.be/YOUR_VIDEO_LINK)

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

'''🛰️ The transmitter detects tap patterns → encodes as Morse → sends via LoRa SX1278 → receiver decodes and provides feedback.
