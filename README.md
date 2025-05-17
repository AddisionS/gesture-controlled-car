# MPU6050 Gesture Controlled Car (ESP-NOW)
This project enables a gesture-controlled robotic car using two ESP32 boards. One ESP32 reads tilt gestures 
from an MPU6050 sensor and transmits directional commands wirelessly using ESP-NOW.
The second ESP32 receives these commands and drives a 4-wheel motor driver accordingly.

# Hardware Used
- ESP32 Dev Board
- MPU6050 IMU Sensor
- L298N Motor Driver
- DC Gear Motors

# How it works
- Sender
  - Reads MPU6050 angles (X, Y).
  - Interprets tilt direction (e.g., tilt forward = go forward).
  - Sends a struct containing boolean directions via ESP-NOW.
- Receiver
  - Receives direction struct.
  - Controls 4 motors via L298N or L293D based on received values.
