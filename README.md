🕋 Custom Digital Clock PCB (ESP32 + Arduino Nano)

Custom Digital Clock PCB is an advanced iteration of the Jakarta Dishub Digital Clock project, originally developed during an internship at Pusdatin Jakarta Dishub. This version has been completely redesigned using a self-made custom PCB to ensure a cleaner, sturdier, and more efficient build—eliminating the need for breadboards or messy jumper wires ⚡.

🖼️ Visual Preview

Schematic Design

PCB Routing (2D)





3D View (Front)

3D View (Back)





💡 Overview

This system displays real-time clock, date, temperature, humidity, and motivational quotes on a P10 LED Panel. Additionally, it features automatic Adzan audio playback via the DFPlayer Mini and provides a Wi-Fi-based web interface for remote configuration and monitoring 🌐.

The project utilizes a dual-microcontroller architecture:

ESP32 → Acts as the main controller handling IoT tasks (Wi-Fi, Web Server, Sensors).

Arduino Nano → Acts as a dedicated display controller specifically for the P10 HUB12 panel multiplexing.

🎓 First PCB Learning Experience

This project represents my first experience designing and manufacturing a PCB from scratch using KiCad 10.0.1 🧠. From schematic capture and netclass configuration to manual trace routing, every step was an independent learning process to understand industrial hardware development workflows.

Every iteration served as a valuable lesson in improving future PCB designs—optimizing for efficiency, safety, and production readiness ⚙️.

🧩 In short: This project is not just about building a functional device; it is about learning how electronics and PCB design converge in a professional environment.

⚙️ Main Features

Feature

Description

🕐 Real-Time Clock

Precise time and date synchronization using the DS3231 RTC module.

🌡️ Environment Monitoring

Real-time DHT22 sensor data processed accurately by the ESP32.

🔊 Auto Adzan Audio

Automatic MP3 playback from an SD card during prayer times.

💬 Dynamic Quotes

Displays motivational quotes fetched from online APIs.

🌐 Web Interface

Local web dashboard for configuration (SSID, Time sync, etc.).

🔌 Custom PCB

All components integrated into a professional, single-board solution.

🧰 Key Components

ESP32 Dev Board (Main Logic & IoT)

Arduino Nano (P10 Display Driver)

DHT22 (Temperature & Humidity Sensor)

DS3231 RTC (Real-Time Clock Module)

DFPlayer Mini (MP3 Audio Player)

P10 HUB12 LED Panel (Primary Display)

Custom 2-Layer PCB

💻 Firmware & Testing

Preparation: Connect both the ESP32 and Arduino Nano to your PC.

Flash ESP32: Upload the main_esp32.ino sketch (Select ESP32 Dev Module).

Flash Nano: Upload the display_nano.ino sketch (Select Arduino Nano).

SD Card: Place the required Adzan audio files in the designated folder on the SD card.

Power Up: Connect a stable 5V power supply to the provided terminal block.

Connection: Access the local IP address shown on the display to open the Web Interface 🎉.

👨‍💻 Developer

Natanael Siwalette
Focus: Embedded Systems, IoT, and Real-Time Monitoring Systems

📫 LinkedIn | 💻 Portfolio

📜 License

This project is open-source for educational, research, and prototyping purposes. Feel free to use or modify it, provided that proper credit is given 🙌
