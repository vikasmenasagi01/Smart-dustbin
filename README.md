# 🗑️ Smart Dustbin Using Arduino Uno

<p align="center">
  <img src="smart dustbin working prototype.jpeg" alt="Smart Dustbin Working Prototype" width="650">
</p>

<h2 align="center">♻️ Automatic • Touchless • Smart Waste Management</h2>

<p align="center">
  <b>An Arduino Uno based smart dustbin that automatically opens its lid when an object or hand is detected nearby.</b>
</p>

---

## 📌 Project Overview

The **Smart Dustbin** is an Arduino Uno based automatic waste bin designed to provide a **touchless and hygienic waste disposal system**.

The system uses an **HC-SR04 ultrasonic sensor** to detect a hand or object near the dustbin. When an object is detected within a predefined distance, the Arduino Uno processes the sensor data and commands an **SG90 servo motor** to automatically open the lid.

A **16×2 I2C LCD display** shows the current status of the dustbin, while an optional **buzzer** provides an audio indication.

### ✨ Main Idea

> **Detect → Process → Open → Display → Close**

---

## 🎯 Objectives

- 🖐️ Enable touchless waste disposal
- 🧼 Improve hygiene and cleanliness
- ⚡ Automate the dustbin lid
- 📟 Display the dustbin status using an LCD
- 🔊 Provide optional audio feedback
- 🔧 Demonstrate practical Arduino and embedded-system concepts

---

# ⚙️ Components Used

| 🔧 Component | 📋 Purpose |
|---|---|
| 🔵 Arduino Uno | Main controller |
| 📡 HC-SR04 Ultrasonic Sensor | Detects hand/object |
| ⚙️ SG90 Servo Motor | Opens and closes the lid |
| 📺 16×2 I2C LCD | Displays dustbin status |
| 🔔 Buzzer | Optional audio indication |
| 🔋 5V Power Supply | Powers the system |
| 🗑️ Dustbin | Mechanical enclosure |
| 🔌 Jumper Wires | Circuit connections |

---

<h2>📐 Block Diagram</h2>

<img src="smart dustbin block diagram.jpeg" alt="Smart Dustbin Block Diagram" width="800">

### 🔗 System Flow

```text
        📡 HC-SR04
             │
             │ Object Detection
             ▼
      ┌───────────────┐
      │  Arduino Uno  │
      │   Processing  │
      └───────┬───────┘
              │
       ┌──────┼───────────┐
       │      │           │
       ▼      ▼           ▼
   ⚙️ Servo  📺 LCD     🔔 Buzzer
       │      │           │
       ▼      ▼           ▼
   Lid Open  Status     Audio
