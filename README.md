<a href="https://colab.research.google.com/github/TejazerX/BinBuddy/blob/main/BinBuddy_real_time_object_detection_and_classification.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# ♻️ BinBuddy – Smart Waste-Sorting Robot

BinBuddy is an intelligent, autonomous robot built for real-time waste detection, classification, and sorting. Using state-of-the-art AI (YOLOv11), a range of advanced sensors, and off-road capabilities, BinBuddy is designed to assist in automated, sustainable waste management.

---

## 🚀 Features

- 🧠 **YOLOv11 AI** for object detection and classification (Dry, Wet, Metal waste).
- 🔧 **Sorting Mechanism** using a robotic arm and conveyor belt.
- 🌐 **Real-time Streaming & Detection** via Google Colab + ESP8266.
- 📡 **Wireless Communication** via mobile hotspot and socket communication.
- ⚙️ **Sensors Array:**
  - 3 × Ultrasonic sensors
  - 3 × Infrared sensors
  - 1 × Rain sensor
  - 1 × Color sensor
  - 1 × Proximity metal detector
  - 1 × Moisture sensor
- 🌞 **Solar-powered module** for green energy.
- 🛞 **Off-road capable wheels** for terrain adaptability.

---

## 🧠 Architecture

1. **YOLOv11 model** runs in real-time on Google Colab using webcam video stream.
2. **Object detection** gives bounding box & label → Calculates object's center.
3. Sends `label` and `coordinates` to **ESP8266** using Python sockets.
4. ESP8266 receives data and guides the robot via **Arduino** based movement.
5. **Sensors** assist in precise waste categorization before sorting.

---

## 🔌 Hardware Components

- Arduino Uno / Mega
- ESP8266 (NodeMCU or ESP-01)
- Servo Motors for Arm
- Conveyor Belt Mechanism
- Solar Panel (for backup power)
- Wheelbase with Off-road Support
- All sensors listed above

---

## 💻 Software Stack

- Python (Google Colab)
- YOLOv11 (via Ultralytics)
- Socket programming for communication
- Arduino IDE for microcontroller logic
- HTML / JS for real-time video capture
- PIL, NumPy, Base64 for image processing

---

## 📦 Setup Instructions

1. **Train or load YOLOv11 model** and upload to Colab.
2. Open the `.ipynb` notebook with the badge above.
3. Run all cells to activate webcam + inference loop.
4. Make sure your phone hotspot is running (ESP and PC should be on same LAN).
5. Flash the **ESP8266 socket server code**.
6. Connect **Arduino to ESP8266** using Serial (via logic level shifter).
7. Flash **Arduino movement code**.
8. The robot will now move towards detected waste and sort it automatically.

---
