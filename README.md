<img width="935" height="623" alt="image" src="https://github.com/user-attachments/assets/91085fa2-9d82-48ea-b7a1-3659e0f325a1" />

# 🛠️ FreeRTOS Workshop Assistant

![Platform](https://img.shields.io/badge/Platform-ESP32-OLED?style=flat-square&color=24292e)
![Framework](https://img.shields.io/badge/Framework-Arduino-blue?style=flat-square)
![OS](https://img.shields.io/badge/OS-FreeRTOS-green?style=flat-square)
![Language](https://img.shields.io/badge/Language-C%2B%2B-red?style=flat-square)

A real-time environmental monitoring device designed as a **"Digital Swiss Army Knife"** for workshop environments. This project leverages the **ESP32 Dual-Core architecture** and **FreeRTOS** to monitor Temperature, Humidity, Sound, and Light levels simultaneously without system latency.

## 🎯 Project Motivation

Traditional embedded projects often rely on a single `loop()` structure, which becomes "blocked" when reading slow sensors (like the DHT series) or updating displays. This project solves these bottlenecks by:
* Implementing **Preemptive Multitasking** to ensure high-priority tasks are never delayed.
* Utilizing **Dual-Core Processing** to separate data acquisition from UI management.
* Demonstrating efficient **Resource Management** in a real-time environment.

## 🚀 Technical Highlights

* **Task Scheduling:** Independent tasks are created for sensor reading, display refresh, and user input handling, each with specific priorities.
* **Dual-Core Execution:** * **Core 0:** Dedicated to timing-critical sensor data acquisition.
    * **Core 1:** Handles the OLED display and user interface logic.
* **Inter-Task Communication:** Uses **Semaphores** to protect shared resources and prevent race conditions.
* **Non-Blocking Architecture:** High-speed response to environmental changes (like noise spikes or light fluctuations) even while performing slow temperature calculations.

## 📊 Monitored Parameters

* 🌡️ **Temperature & Humidity:** Climate monitoring via DHT sensors.
* 💡 **Light Intensity:** Real-time ambient light tracking using an LDR.
* 🔊 **Noise Levels:** Sound intensity analysis via an analog microphone module.

## 🛠️ Hardware Stack

* **MCU:** ESP32 (Dual-Core)
* **Display:** 0.96" OLED (I2C)
* **Sensors:** * DHT11/DHT22 (Climate)
    * LDR (Light)
    * Analog Microphone (Sound)
* **Peripherals:** Push buttons for mode switching and system reset.


