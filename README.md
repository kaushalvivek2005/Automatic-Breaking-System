# Automatic-Breaking-System

## 📌 Overview

This project presents a prototype of an **Automatic Braking System** designed to prevent collisions by automatically stopping a vehicle when an obstacle is detected.

The system uses an ultrasonic sensor to continuously monitor the distance between the vehicle and obstacles. When the distance falls below a predefined threshold, the system activates braking without driver input.

---

## 🎯 Objective

* Detect obstacles in real time
* Automatically stop the vehicle to avoid collisions
* Reduce dependency on human reaction

---

## ⚙️ System Architecture

The system consists of the following flow:

**Ultrasonic Sensor → Arduino Uno → Motor Driver → DC Motors → Buzzer**

* Sensor detects distance
* Arduino processes the data
* Motor driver controls motors
* Buzzer gives alert

---

## 🔧 Components Used

* Arduino Uno R3
* Ultrasonic Sensor (HC-SR04)
* Motor Driver
* DC Motors
* Buzzer
* Battery
* Switch
* Jumper Wires
* Wheels & Clamp

---

## 🧠 Working Principle

1. The ultrasonic sensor measures the distance of objects in front of the vehicle
2. Arduino continuously reads the sensor data
3. If the distance is less than or equal to a predefined value (≈20 cm):

   * Motors stop immediately
   * Buzzer turns ON
4. If no obstacle is detected:

   * Motors continue running

---

## 💻 Code Logic

```cpp id="corelogic"
if (distance <= brakeDistance) {
    stopMotors();
    digitalWrite(buzzerPin, HIGH);
} else {
    runMotorsForward();
    digitalWrite(buzzerPin, LOW);
}
```

---

## 🚀 Features

* Automatic obstacle detection
* Instant braking response
* Simple and low-cost implementation
* Real-time operation

---

## ⚠️ Limitations

* Uses fixed distance threshold
* Limited accuracy in certain conditions
* Not suitable for high-speed applications
* Depends on ultrasonic sensor performance

---

## 📊 Applications

* Basic vehicle safety systems
* Obstacle avoidance in robotics
* Educational embedded system projects

---

## 🏁 Conclusion

The project demonstrates a simple and effective **Automatic Braking System** using Arduino and ultrasonic sensing. It highlights how real-time detection and control can help prevent collisions and improve safety.

