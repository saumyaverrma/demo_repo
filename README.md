# AirGuard  
**Real-Time Air Quality Monitoring & Alert System**
Even in the same city, people experience different pollution exposure. Someone who spends more time outdoors breathes far more polluted air than someone mostly indoors. <br>
**AirGuard tracks every outdoor session using geofencing and combines duration × live AQI to calculate each user’s personal exposure score.**<br>
This app helps users understand how much polluted air they personally breathe every day using live AQI data and geofencing.  
At the end of the day, the app also generates a personalized recovery plan (breathing + diet suggestions) using the Gemini API.

---

## Table of Contents  
- [Project Overview](#project-overview)  
- [Key Features](#key-features)  
- [Tech Stack & Architecture](#tech-stack--architecture)  
- [System Diagram](#system-diagram)  
- [Installation & Setup](#installation--setup)  
- [Usage](#usage)  
- [Screenshots / Demo](#screenshots--demo)  
- [Directory Structure](#directory-structure)  
- [Future Enhancements](#future-enhancements)  
- [License](#license)

---

## Project Overview  
AirGuard is a cross-platform system designed to **monitor air-quality parameters in real time**, including PM levels, VOCs, CO₂ and general air pollution metrics.  
It provides a unified dashboard that works on **Android, iOS, Web, Windows, Linux, and macOS**, helping users track environmental conditions instantly and receive alerts when the air quality becomes unsafe.

---

## Key Features  
- Real-time sensor data visualization  
- AQI (Air Quality Index) calculations and trend charts  
- Threshold-based alerts and notifications  
- Multi-platform support (mobile + desktop + web)  
- Modular architecture allowing easy sensor expansion  
- Clean UI built with Flutter  
- Historical data visualization (if backend supports)

---

## Features (Detailed)

### **1. Real-Time AQI Tracking**
- Fetches live AQI from OpenAQ API  
- Shows current AQI and PM2.5 around the user  

---

### **2. Outdoor Exposure Timer**
- User sets home location  
- Geofence detects when user leaves/enters home  

```
Exposure = Time Outside × AQI
```

---

### **3. Daily Exposure Summary**
Displays:  
1. Today’s time outdoors  
2. Average AQI  
3. Total exposure score  

---

### **4. AI Recovery Plan (New Feature)**
At the end of the day, the app generates:  
- 2–4 minute breathing exercise  
- Two diet/home remedy suggestions  
- Short safety disclaimer  
- Powered by **Gemini API** (one call per day)

---

## Tech Stack & Architecture  

### **Tech Stack**  
- **Frontend:** Flutter (Dart)  
- **Platforms:** Android
- **Backend / DB:** Firebase / REST API / MQTT / Node.js / etc.  
- **Hardware / Sensors:** MQ-135, ESP32, PMS5003 (or your specific sensors)

---

### **Architecture Overview**

```
Sensors → Microcontroller → Cloud Database/API → AirGuard Apps
                                   ↘ Alert System
```

---

## System Diagram  

---

## Installation & Setup  

### **1. Clone the repository**
```bash
git clone https://github.com/retrospecs0801/AirGuard.git
cd AirGuard
```

---

### **2. Install dependencies**
```bash
flutter pub get
```

---

### **3. Configure environment**
1. Add sensor endpoints / backend URLs in your config file  <br>
2. Adjust alert thresholds as needed  

---

### **4. Run the application**
```bash
flutter run
```

---

### **5. Build for web**
```bash
flutter build web
```

---

## Usage  
1. Open the AirGuard application on your device  
2. Connect to the sensor backend / IoT device  
3. Monitor real-time air-quality metrics  
4. Check AQI, graphs, and historical data  
5. Receive alerts when levels exceed safety thresholds  
6. Adjust units, thresholds, and data sources in settings  

---

## Screenshots / Demo  

---

## Directory Structure  
```
AirGuard/
├── android/          ← Android project
├── ios/              ← iOS project
├── web/              ← Web build
├── linux/            ← Linux desktop build
├── macos/            ← macOS build
├── windows/          ← Windows build
├── lib/              ← Flutter/Dart app source
├── test/             ← Tests
├── docs/             ← Images, diagrams, documentation
├── pubspec.yaml
└── README.md
```
