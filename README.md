# 🚦 AI-Based Dynamic Traffic and Emergency Control System

![Image](https://cdn.dribbble.com/userupload/24572162/file/original-727b886312cb10ab0d22d6b3ed6d54d1.png?format=webp\&resize=400x300\&vertical=center)

![Image](https://ars.els-cdn.com/content/image/1-s2.0-S2468227623004155-gr4.jpg)

## 🚑 Intelligent Signal Optimization with Real-Time Emergency Priority

An AI-powered traffic management system designed to dynamically optimize signal timings and provide automatic right-of-way to emergency vehicles using computer vision and real-time analytics.

Unlike traditional fixed-cycle traffic lights, this system continuously analyzes live traffic video to:

* Adjust green signal duration based on real demand
* Detect ambulances in real time
* Override normal signal flow to create a green corridor
* Safely restore standard operations after clearance

---

## 📌 Problem Context

Most urban intersections operate using static timing cycles. This leads to:

* Unequal green time distribution
* Long queues in peak hours
* Delayed ambulance response
* Inefficient road utilization

Research in adaptive traffic control shows measurable delay reduction compared to fixed timing systems, particularly in high-density intersections.

This project demonstrates a deployable AI-based alternative using vision-driven decision logic.

---

## 🧠 System Capabilities

### 🔍 Intelligent Traffic Analysis

* Real-time vehicle detection using YOLO (ONNX optimized)
* Lane-wise density estimation
* Adaptive green signal allocation
* Configurable signal phase logic

### 🚑 Emergency Priority Engine

* Ambulance detection using trained models
* Immediate phase override for priority clearance
* Safety-compliant transitions (yellow & all-red handling)
* Automatic recovery after emergency exit

### 🖥️ Monitoring Dashboard

* Live annotated video stream
* Vehicle counts and peak metrics
* Signal phase visualization
* Manual override and emergency simulation
* Real-time system status updates

---

## 🏗️ Architecture Overview

The system follows a modular architecture for scalability and maintainability.

### 1️⃣ AI Processing Layer (Python)

* OpenCV for frame capture
* YOLO detection via ONNX Runtime
* ByteTrack for object tracking
* Lane filtering & density computation
* Dynamic signal timing algorithm

### 2️⃣ Backend Communication Layer

* AIOHTTP server
* Python-SocketIO
* WebSocket streaming for low-latency updates

### 3️⃣ Frontend Visualization Layer

* React + Vite
* Tailwind CSS interface
* Zustand state management
* Live metrics rendering

---

## ⚙️ Technology Stack

| Layer           | Technologies               |
| --------------- | -------------------------- |
| Computer Vision | OpenCV, YOLO, ONNX Runtime |
| Tracking        | ByteTrack                  |
| Backend         | Python, AIOHTTP, Socket.IO |
| Frontend        | React, Tailwind            |
| Communication   | WebSockets, REST APIs      |

---

## 🚀 Installation & Setup

### 🔹 Requirements

* Python 3.10+
* Node.js (v18+ recommended)
* Git

---

### 🔹 Clone Repository

```bash
git clone https://github.com/DarshiniMahesh/AI-Based_Dynamic_Traffic_and_Emergency_Control_System.git
cd AI-Based_Dynamic_Traffic_and_Emergency_Control_System
```

---

### 🔹 Install Dependencies

```bash
pip install -r requirements.txt
```

If running frontend separately:

```bash
cd dashboard/frontend
npm install
```

---

### 🔹 Run the System

```bash
python run_dashboard.py
```

Open in browser:

```
http://localhost:5173
```

---

## 🎮 How to Use

### Live Monitoring

* Select video source
* Start detection
* Observe signal transitions
* Monitor lane congestion

### Simulation Controls

* Trigger ambulance event
* Reset system state
* Manually override signals

---

## 📂 Project Structure

```
AI-Based_Dynamic_Traffic_and_Emergency_Control_System/
│
├── core/
│   ├── detectors/
│   ├── trackers/
│   └── signal_logic/
│
├── dashboard/
│   ├── backend/
│   └── frontend/
│
├── traffic_signals/
├── run_dashboard.py
└── requirements.txt
```

---

## 📊 Performance Targets

| Parameter                  | Expected              |
| -------------------------- | --------------------- |
| Detection Latency          | < 100 ms per frame    |
| Signal Decision Delay      | < 1 second            |
| Emergency Trigger Response | Frame-level detection |
| WebSocket Update Speed     | Near real-time        |

⚠ Actual performance depends on camera resolution and hardware capability.

---

## 🔍 System Limitations

* Requires camera infrastructure
* Night/rain conditions may reduce detection accuracy
* No direct hardware controller integration yet
* Single-intersection deployment model

---

## 🔮 Future Enhancements

* Multi-intersection coordination
* Reinforcement learning-based signal optimization
* Edge device deployment (Jetson class devices)
* Audio siren detection fusion
* Integration with smart-city IoT infrastructure

---

## 📈 Real-World Impact Potential

If integrated with real traffic controllers:

* Reduced ambulance travel delay
* Lower vehicle idle time
* Reduced fuel consumption
* Improved urban mobility efficiency

---

## 🤝 Contributions

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

