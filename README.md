# Object Detecting Sensor with Arduino Uno

## 📌 Overview
This project is an **Object Detection System** built using:
- Arduino Uno
- Ultrasonic Sensor (HC-SR04)
- Servo Motor (SG90)
- Jumper wires & Breadboard

The system **detects objects within 50 cm** using the ultrasonic sensor.  
When an object is detected, the servo motor **rotates by 90°**, and the distance is displayed in the serial monitor.

---

## 🚀 Features
- Detects objects within a configurable range (50 cm in this setup)
- Rotates servo motor by 90° when an object is detected
- Displays real-time distance measurement
- Simple, compact, and cost-effective

---

## 🛠 Components Required
- **Arduino Uno** (or compatible board)
- **Ultrasonic Sensor** (HC-SR04)
- **Servo Motor** (SG90 or similar)
- Breadboard
- Jumper wires
- USB cable for Arduino

---

## ⚙️ Circuit Diagram
| Ultrasonic Sensor Pin | Arduino Pin |
|-----------------------|-------------|
| VCC                   | 5V          |
| GND                   | GND         |
| Trig                  | 9           |
| Echo                  | 10          |

| Servo Motor Pin | Arduino Pin |
|-----------------|-------------|
| VCC             | 5V          |
| GND             | GND         |
| Signal          | 6           |

---

## 📄 Working Principle
1. **Ultrasonic Sensor** measures the distance to an object using sound waves.
2. If the distance is **less than or equal to 50 cm**, the Arduino:
   - Rotates the **servo motor** by 90°.
   - Displays the distance in the serial monitor.
3. If no object is detected within the range, the servo motor remains at its initial position.

---

## 📜 Arduino Code
```cpp
#include <Servo.h>

Servo myservo;

#define trigPin 9
#define echoPin 10
#define servoPin 6

void setup() {
  Serial.begin(9600);
  myservo.attach(servoPin);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
}

void loop() {
  long duration;
  int distance;

  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);

  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);
  distance = duration * 0.034 / 2;

  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");

  if (distance <= 50) {
    myservo.write(90);
  } else {
    myservo.write(0);
  }

  delay(500);
}
