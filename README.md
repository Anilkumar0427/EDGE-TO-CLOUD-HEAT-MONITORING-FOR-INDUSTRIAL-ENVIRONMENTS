# Edge-to-Cloud Heat Monitoring for Industrial Environments

## 📌 Overview

**Edge-to-Cloud Heat Monitoring for Industrial Environments** is an IoT-based embedded system designed to monitor temperature and detect gas/smoke in industrial areas. The system uses an **LPC2148 ARM7 microcontroller** to collect sensor data locally (edge layer) and periodically uploads it to the cloud using an **ESP-01 Wi-Fi module**.

The project provides real-time environmental monitoring, cloud-based data logging, and emergency alerts to improve industrial safety and equipment reliability. 

---

## 🚀 Features

* 🌡️ Real-time temperature monitoring using LM35 sensor
* ☁️ Cloud data upload using ESP-01 Wi-Fi module
* 📊 Temperature logging to ThingSpeak cloud platform
* 🚨 Gas/Smoke detection using MQ-2 sensor
* 🔔 Automatic buzzer activation during gas leakage
* 📟 LCD display for local monitoring
* ⏱️ RTC-based periodic cloud updates (every 3 minutes)
* 📈 Historical data analysis through cloud dashboard
* 🏭 Suitable for industrial safety monitoring

---

## 🛠 Hardware Requirements

* LPC2148 ARM7 Microcontroller
* LM35 Temperature Sensor
* MQ-2 Gas/Smoke Sensor
* 16x2 LCD Display
* ESP-01 Wi-Fi Module
* Buzzer
* DB9 Cable / USB-UART Converter
* Power Supply Unit



---

## 💻 Software Requirements

* Embedded C
* Keil uVision Compiler
* Flash Magic



---

## ⚙️ System Architecture

```text
      +-------------+
      |   LM35      |
      +------+------+
             |
             v
      +-------------+
      |  LPC2148    |
      +------+------+----------------+
             |                       |
             v                       v
      +-------------+         +-------------+
      |    LCD      |         |   Buzzer    |
      +-------------+         +-------------+
             |
             v
      +-------------+
      | MQ-2 Sensor |
      +-------------+
             |
             v
      +-------------+
      | ESP-01 WiFi |
      +------+------+
             |
             v
      +-------------+
      | ThingSpeak  |
      |   Cloud     |
      +-------------+
```

---

## 🔄 Working Principle

1. LPC2148 continuously reads temperature data from the LM35 sensor.
2. Temperature values are displayed locally on the LCD.
3. Using the built-in RTC, temperature data is uploaded to the ThingSpeak cloud every 3 minutes.
4. MQ-2 sensor continuously monitors gas and smoke levels.
5. If gas/smoke is detected:

   * Buzzer is activated.
   * Alert message is sent to the cloud immediately.
6. When the environment becomes normal:

   * A recovery message is sent to the cloud.
7. Cloud data can be used for monitoring, logging, and analysis.



---

## 📂 Project Modules

### LCD Driver

* Displays temperature and system status.

### ADC Driver

* Reads analog values from LM35 and MQ-2 sensors.

### UART Driver

* Communication between LPC2148 and ESP-01.

### ESP-01 Driver

* Sends sensor data to ThingSpeak cloud.

### RTC Module

* Controls periodic data transmission.

### Alert System

* Activates buzzer during hazardous conditions.

---

## 📊 Cloud Platform

The project uses **ThingSpeak** for:

* Data collection
* Real-time monitoring
* Data visualization
* Historical analysis
* Alert logging



---

## 🎯 Applications

* Industrial Heat Monitoring
* Factory Safety Systems
* Boiler Temperature Monitoring
* Warehouse Environment Monitoring
* Fire and Smoke Detection Systems
* Smart Manufacturing Plants

---

## 🔮 Future Enhancements

* Mobile Application Integration
* SMS/Email Alert System
* Multiple Sensor Support
* Predictive Maintenance Analytics
* MQTT-Based Communication
* AI-Based Anomaly Detection

---

## 📸 Expected Output

* Real-time temperature displayed on LCD
* Temperature data uploaded to ThingSpeak every 3 minutes
* Gas/Smoke alerts sent instantly to cloud
* Buzzer activated during hazardous conditions
* Historical cloud dashboard for monitoring and analysis

---

## 👨‍💻 Author

**Anil Kumar**

Embedded Systems & IoT Project using **LPC2148 ARM7**, **ESP-01 Wi-Fi**, **ThingSpeak Cloud**, **LM35**, and **MQ-2 Sensors**.

---
