# 🏠 Indoor Smart Security & Environmental Monitoring System

## 📌 Overview

The **Indoor Smart Security & Environmental Monitoring System** is an IoT-based prototype that integrates **Arduino UNO** and **Wemos D1 ESP8266** using a **Master–Slave architecture** to provide real-time indoor security monitoring and environmental awareness.

The Arduino UNO is responsible for sensor processing and actuator control, while the ESP8266 provides Wi-Fi connectivity and hosts a local web dashboard for remote monitoring and alarm control. Communication between both microcontrollers is implemented using the **I2C protocol**, creating a modular and scalable IoT system.

---

## ✨ Features

* 🚨 Human presence detection using an HC-SR04 ultrasonic sensor
* 🌡 Real-time temperature monitoring
* 🔴 Automatic visual and audible alarm system
* 🌬 Automatic cooling fan activation during overheating
* 📟 Live sensor readings displayed on a 16x2 I2C LCD
* 🌐 Local web dashboard for remote monitoring
* 📡 Wi-Fi connectivity via ESP8266
* 🔄 Remote alarm trigger and reset through a web browser
* 🔗 Master–Slave communication using I2C

---

## 🏗 System Architecture
<img width="528" height="505" alt="Screenshot 2026-07-22 at 2 25 25 PM" src="https://github.com/user-attachments/assets/76ade595-18b5-4069-b6e6-8c179e7937ba" />

### Master Controller

**Wemos D1 ESP8266**

* Hosts local Wi-Fi Access Point
* Runs embedded web server
* Displays web dashboard
* Requests telemetry from Arduino
* Sends remote alarm commands

### Slave Controller

**Arduino UNO**

* Reads sensor data
* Processes security logic
* Controls LEDs, buzzer, LCD, and cooling fan
* Responds to commands received through I2C

---

## ⚙ Hardware Components

| Component                 | Function                             |
| ------------------------- | ------------------------------------ |
| Arduino UNO               | Sensor processing & actuator control |
| Wemos D1 ESP8266          | Wi-Fi & Web Dashboard                |
| HC-SR04 Ultrasonic Sensor | Human presence detection             |
| TMP36 Temperature Sensor  | Ambient temperature monitoring       |
| Push Button               | Manual emergency alarm               |
| Potentiometer             | Alarm reset & LCD adjustment         |
| 16x2 I2C LCD              | System status display                |
| Red LED                   | Alert indicator                      |
| Green LED                 | Safe status indicator                |
| Piezo Buzzer              | Audible alarm                        |
| Mini DC Fan               | Automatic cooling                    |

---

## 🌐 Web Dashboard

The ESP8266 hosts a **local web dashboard** without requiring any cloud platform.

Dashboard features include:

* Live temperature reading
* Ultrasonic distance
* Potentiometer voltage
* Current system status
* I2C communication status
* Alarm ON/OFF controls
* Wi-Fi information

Users simply connect to the ESP8266 Wi-Fi hotspot and open the dashboard from any web browser on the same network.

---

## 🔄 System Workflow

1. Arduino initializes all sensors and actuators.
2. Temperature sensor performs baseline calibration.
3. Ultrasonic sensor continuously monitors for human presence.
4. Temperature sensor monitors environmental conditions.
5. Arduino updates LEDs, LCD, buzzer, and cooling fan accordingly.
6. Sensor data is transmitted to the ESP8266 via I2C.
7. ESP8266 updates the web dashboard in real time.
8. Users can remotely trigger or clear alarms through the dashboard.

---

## 💻 Technologies Used

* Arduino IDE (C/C++)
* Arduino UNO
* Wemos D1 ESP8266
* I2C Communication Protocol
* HTML & CSS
* Embedded Web Server
* Wi-Fi Access Point
* Tinkercad Simulation

---

## 📸 Project Demonstration



Uploading WhatsApp Video 2026-07-06 at 11.12.37 (1).mp4…


