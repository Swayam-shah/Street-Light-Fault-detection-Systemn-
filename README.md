# Street Light Fault Detection and Monitoring System


## Overview
This project aims to develop a **smart street light fault detection and monitoring system** using IoT Technology. The system uses an **ESP32 microcontroller**, **LDR sensor**, and **IR sensor** to detect faults in street lights and send real-time notifications to authorized personnel via the **Blynk app**.

## Features
- Real-time monitoring of street light status.
- Fault detection (e.g., malfunctioning bulbs, electrical failures).
- Automatic light control based on ambient light and object detection.
- Remote management via the Blynk app.

## Table of Contents
1. [System Architecture](#system-architecture)
2. [Components Used](#components-used)
   - [ESP32 Microcontroller](#esp32-microcontroller)
   - [LDR Sensor](#ldr-sensor)
   - [IR Sensor](#ir-sensor)
3. [How It Works](#how-it-works)
4. [Results](#results)
5. [Future Work](#future-work)



## System Architecture
The system consists of the following components:
- **ESP32 Microcontroller**: Connects the system to Wi-Fi and processes sensor data.
- **LDR Sensor**: Measures ambient light intensity to determine if the street light should be on or off.
- **IR Sensor**: Detects objects near the street light, which can trigger the light.
- **Blynk App**: Provides a user-friendly interface for real-time monitoring and control.

## Components Used

### 1. ESP32 Microcontroller
The **ESP32** is a powerful, low-cost, low-power microcontroller with integrated Wi-Fi and Bluetooth capabilities. It is widely used in IoT projects due to its versatility and ease of use.

#### Key Features of ESP32:
- **Dual-Core Processor**: The ESP32 has two 32-bit cores, which allow for multitasking and efficient processing.
- **Wi-Fi and Bluetooth**: Built-in Wi-Fi (802.11 b/g/n) and Bluetooth (Classic and BLE) enable seamless connectivity.
- **GPIO Pins**: The ESP32 has multiple General-Purpose Input/Output (GPIO) pins, which can be used to connect sensors, LEDs, and other peripherals.
- **Analog-to-Digital Converter (ADC)**: The ESP32 has a 12-bit ADC, which is used to read analog signals from sensors like the LDR.
- **Low Power Consumption**: The ESP32 is designed for low-power applications, making it ideal for IoT devices.

#### Role in the Project:
- The ESP32 acts as the brain of the system, processing data from the **LDR** and **IR sensors**.
- It connects to the **Blynk app** via Wi-Fi to send real-time data and receive commands.
- It controls the street light (LED) based on sensor inputs and detects faults.

### 2. LDR Sensor (Light Dependent Resistor)
- **Function**: Measures the intensity of light.
- **Working**: The resistance of the LDR decreases as light intensity increases. It is used to detect whether it is day or night.


### 3. IR Sensor (Infrared Sensor)
- **Function**: Detects objects or obstacles near the street light.
- **Working**: The IR sensor emits infrared light and detects reflections from objects. It is used to trigger the street light when an object is detected.


## How It Works
1. The **LDR sensor** continuously monitors ambient light levels. If the light level falls below a threshold (indicating nighttime), the system activates the street light.
2. The **IR sensor** detects objects near the street light. If an object is detected, the light remains on; otherwise, it turns off.
3. The **ESP32 microcontroller** processes the sensor data and sends it to the **Blynk app** for real-time monitoring.
4. If a fault is detected (e.g., the light does not turn on when it should), the system sends an alert to the Blynk app.

## Results
- **Real-Time Monitoring**: The Blynk app displays real-time sensor data and street light status.
- **Fault Detection**: The system successfully detects faults, such as when the street light does not turn on during nighttime.
- **Energy Efficiency**: The system reduces energy consumption by automatically turning off lights when not needed.

## Future Work
- Integrate the system with other smart city technologies (e.g., traffic management, environmental monitoring).
- Develop predictive maintenance models to anticipate and prevent failures.
- Optimize energy efficiency by adjusting brightness levels based on real-time condition.




