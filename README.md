![Year](https://img.shields.io/badge/Developed-2022-blue)

# 🫀 IoT Based ECG Monitoring System

This project is a smart ECG monitoring system which is based on IoT Technology. By monitoring and analyzing the ECG signal at an initial stage, certain heart diseases can be identified and prevented. The system captures a human's heartbeat as data signals, processes them via a microcontroller, and transmits the data to an IoT platform for further analytics and visualization.

## 🛠️ Hardware Components
* **Microcontroller:** ESP32 Board
* **Sensors:** ECG Sensor (AD8232) with physical electrodes.
* **Accessories:** Breadboard, jumper wires, and a Data USB Cable.

## 💻 Software & Platform
* **Language:** C++ (Arduino Framework) utilizing the `WiFi.h` and `PubSubClient.h` libraries for MQTT communication.
* **IoT Cloud Platform:** Ubidots. This platform is used for sending data from the ESP32 to the cloud, triggering alerts based on that data, and visualizing it.

## 🚀 System Logic and Flow
1.  The system initializes and checks if a WiFi connection is established.
2.  Once connected to the MQTT broker (`industrial.api.ubidots.com`), the sensor starts transmitting data.
3.  Analog readings are captured from pin A0, converted to a string format, and uploaded to the Ubidots cloud payload.
4.  Based on experimental results, the system can classify the heartbeat rate: low (between 40 and 60), medium (between 60 and 100), and high (between 100 and 150).

## 🗂️ Project Documentation
* `ECG_ubidots.ino`: The main source code for the ESP32.
* `2022-11-10.jpg`: Image of the experimental hardware setup.
* `ECG_ESP32.jpg`: Flowchart demonstrating the program's execution loop.
