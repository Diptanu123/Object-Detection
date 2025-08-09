# 🎯 Object Detecting Sensor with Arduino Uno

An **Arduino-based Object Detection System** that uses an **Ultrasonic Sensor** to measure distance and trigger a **Servo Motor** when an object comes within 50 cm.  
Perfect for automation, robotics, and smart security applications.

---

## 📌 Overview
This project detects objects using the **HC-SR04 Ultrasonic Sensor** and measures the distance in real-time.  
If an object comes within **50 cm**, the servo motor rotates **90°**.  
The system is **simple, affordable, and beginner-friendly**, yet has practical applications in automation and robotics.

---

## ✨ Key Features
- 📏 **Accurate Distance Measurement** using ultrasonic waves
- 🔄 **Automatic Servo Rotation** when an object is detected within range
- 🖥 **Real-time Distance Display** on Serial Monitor
- ⚡ **Fast and Reliable** object detection
- 🛠 **Easy to Build** with minimal components

---

## 🛠 Components Used
| Component | Quantity | Description |
|-----------|----------|-------------|
| Arduino Uno | 1 | Microcontroller board |
| Ultrasonic Sensor (HC-SR04) | 1 | Measures distance using sound waves |
| Servo Motor (SG90) | 1 | Rotates upon detection |
| Breadboard | 1 | For easy wiring |
| Jumper Wires | As required | For connections |
| USB Cable | 1 | To upload code and power Arduino |

---

## ⚙️ How It Works
1. The **HC-SR04 Ultrasonic Sensor** sends out ultrasonic pulses.
2. The sensor measures the time taken for the sound wave to bounce back from an object.
3. The Arduino calculates the **distance** using the time measurement.
4. If the distance is **≤ 50 cm**:
   - The **servo motor** rotates **90°**.
   - The distance is displayed on the Serial Monitor.
5. If the distance is **> 50 cm**, the servo returns to its initial position.

---

## 🔍 Applications
- 🤖 **Robotics** – Autonomous obstacle avoidance
- 🏠 **Smart Home** – Automatic door/gate opening
- 📦 **Inventory Systems** – Detecting items on conveyor belts
- 🚗 **Parking Assistance** – Measuring distance to obstacles
- 🔒 **Security Systems** – Motion and presence detection

---

## 🖥 Circuit Diagram
*(Insert your circuit diagram image here)*

**Ultrasonic Sensor Connections**  
| Sensor Pin | Arduino Pin |
|------------|-------------|
| VCC | 5V |
| GND | GND |
| Trig | 9 |
| Echo | 10 |

**Servo Motor Connections**  
| Servo Pin | Arduino Pin |
|-----------|-------------|
| VCC | 5V |
| GND | GND |
| Signal | 6 |

---

