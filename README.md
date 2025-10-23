# 🕋 Custom Digital Clock PCB (ESP32 + Arduino Nano)

**Custom Digital Clock PCB** is a further development of the *Jakarta Dishub Digital Clock* project that was previously made during an internship at Pusdatin of Jakarta Dishub.
This version is completely redesigned using a **self-made custom PCB** to make it cleaner, sturdier, and more efficient — without relying on breadboards or messy jumper cables anymore ⚡.

---

## 💡 Overview

This system displays **time, date, temperature, humidity, and motivational quotes** in real-time on a **P10 LED Panel**.
It can also **play the adzan audio automatically** via the **DFPlayer Mini**, and provides a **Wi-Fi-based web interface** for configuration and monitoring 🌐.

The project uses two microcontrollers:

* **ESP32** → as the *main controller* and IoT handler
* **Arduino Nano** → as the *display controller* for the P10 HUB12 panel

---

## 🎓 First PCB Learning Experience

This project marks my **first experience designing and creating a PCB from scratch using KiCad 9.0.3** 🧠.
From **schematic design, netclass setup, routing, to DRC/ERC validation**, everything was done independently as part of the learning process to understand how real hardware development works in practice.

Any mistakes or revisions made along the way serve as valuable lessons to improve future PCB designs — making them more efficient, safer, and production-ready ⚙️.

> 🧩 In short: this project isn’t just about making a functional device — it’s about learning how electronics and PCB design work together in the real world.

---

## ⚙️ Main Features

| Feature                                   | Description                                      |
| ----------------------------------------- | ------------------------------------------------ |
| 🕐 **Real-Time Clock**                    | Displays time and date using DS3231 RTC          |
| 🌡️ **Temperature & Humidity Monitoring** | DHT22 sensor data processed by ESP32             |
| 🔊 **Automatic Adzan Audio**              | DFPlayer Mini plays audio from SD card           |
| 💬 **Dynamic Quotes**                     | Displays motivational quotes from an online API  |
| 🌐 **Web Interface**                      | Local web page for configuration & monitoring    |
| 🔁 **I²C Communication**                  | ESP32 sends data to Nano for P10 display updates |
| 🔌 **Custom PCB**                         | All components integrated on a single board      |

---

## 🧰 Main Components

| Component               | Function                                           |
| ----------------------- | -------------------------------------------------- |
| **ESP32 Dev Board**     | Main controller handling Wi-Fi, sensors, and audio |
| **Arduino Nano**        | Controls the P10 HUB12 display                     |
| **DHT22**               | Temperature & humidity sensor                      |
| **DS3231 RTC**          | Accurate real-time clock module                    |
| **DFPlayer Mini**       | Automatic adzan audio player                       |
| **P10 HUB12 LED Panel** | Main display for time and information              |
| **Speaker**             | Audio output from DFPlayer Mini                    |
| **Custom PCB**          | Integrates all electronic components neatly        |

---

## 🪛 PCB Design Information

* Designed using **KiCad 9.0.3**
* Includes **separate netclasses** for power, data, and DFPlayer audio lines
* Wider power and ground traces for current stability ⚡
* **ERC & DRC** checks show only minor warnings (no critical errors)
* Layout arranged for compactness, easy assembly, and clean routing

> 🎯 The main goal of this PCB design is not just functionality, but to train a deep understanding of **how schematics, netclasses, and physical layouts connect together**.

---

## 💻 How to Upload & Test Firmware

1. **Prepare the boards:** Connect both ESP32 and Arduino Nano to your PC.
2. **Flash ESP32:** Upload the `main_esp32.ino` using Arduino IDE (select board: *ESP32 Dev Module*).
3. **Flash Nano:** Upload the `display_nano.ino` sketch (select board: *Arduino Nano* with old bootloader if needed).
4. **Insert SD Card:** Place the adzan audio files inside the DFPlayer Mini’s SD card.
5. **Power Up:** Supply 5V power — check the OLED/P10 panel for startup info.
6. **Connect Wi-Fi:** Access the local IP shown on screen to open the web interface 🎉.

> 💡 Tip: Make sure the DFPlayer Mini’s RX/TX pins are connected correctly to the ESP32, and the P10 panel’s HUB12 connector aligns with the Nano’s pinout.

---

## 👨‍💻 Developer

**Natanael Siwalette**
Unemp😢😭
Focus: Embedded Systems, IoT, and Real-Time Monitoring Systems

📫 [LinkedIn](https://www.linkedin.com/in/natanael-siwalette)
💻 [Portfolio](https://natael221.github.io/)

---

## 📜 License

This project is open for **educational, research, and prototype development purposes**.
Feel free to use or modify it, as long as proper credit is given 🙌.

---
