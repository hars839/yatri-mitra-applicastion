<div align="center">

# 🛺 Yatri-Mitra
### Shared Auto Tracker · Live Simulation

![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![MVVM](https://img.shields.io/badge/Architecture-MVVM-1D9E75?style=for-the-badge)
![API](https://img.shields.io/badge/Min_API-26-EF9F27?style=for-the-badge)
![VTU](https://img.shields.io/badge/VTU_MindMatrix-Project_%2384-0D1B2A?style=for-the-badge)

> *"Know before you go."* — Real-time shared auto tracking for small-town commuters.

</div>

---

## 📌 The Problem

In smaller towns, commuters have **no way of knowing** when the next shared auto will arrive — leading to wasted time, missed trips, and unpredictable commutes. Yatri-Mitra solves this with a live simulation tracker.

---

## 📱 App Screenshots

| Splash | Home | Live Simulation |
|--------|------|-----------------|
| ![Splash](screenshots/screen1_splash.png) | ![Home](screenshots/screen2_home.png) | ![Simulation](screenshots/screen3_simulation.png) |

| Stop Detail | Auto Detail | Arrival Alert |
|-------------|-------------|---------------|
| ![Stop](screenshots/screen4_stop.png) | ![Auto](screenshots/screen5_auto.png) | ![Alert](screenshots/screen6_alert.png) |

| Stats Dashboard | About |
|-----------------|-------|
| ![Stats](screenshots/screen7_stats.png) | ![About](screenshots/screen8_about.png) |

---

## ✨ Features

| Screen | Feature |
|--------|---------|
| 🌅 **Splash** | App intro with animated Get Started button |
| 🏠 **Home** | Route selection — Route 1 (Town Center → Railway) & Route 2 (Market → Bus Stand) |
| 🗺️ **Live Simulation** | Real-time auto-rickshaw movement on a custom Canvas route map |
| 📍 **Stop Detail** | Tap any stop to see approaching autos + passenger count |
| 🛺 **Auto Detail** | Tap any auto row to see speed, position, and next stop |
| 🔔 **Arrival Alert** | Green banner fires when auto is < 2 min from your stop |
| 📊 **Stats Dashboard** | Trip count, avg ETA, busiest stops, route progress bars |
| ℹ️ **About** | Problem statement, ETA formula, tech stack, impact goals |

---

## 🧮 ETA Logic

```
ETA (minutes) = Distance to Stop (km) ÷ Auto Speed (km/h) × 60
```

- Vehicles update position every **100ms**
- Speed multiplier: **×1 to ×5** via SeekBar
- Arrival alert triggers when **ETA < 2 minutes**

---

## 🏗️ Architecture

```
app/
├── SplashActivity.kt       → Screen 1: Splash
├── HomeActivity.kt         → Screen 2: Route Selection
├── MainActivity.kt         → Screen 3-6: Simulation + Alerts
├── StatsActivity.kt        → Screen 7: Trip Statistics
├── AboutActivity.kt        → Screen 8: About Page
├── SimulationViewModel.kt  → MVVM ViewModel (StateFlow)
├── RouteMapView.kt         → Custom Canvas View
├── Vehicle.kt              → Data model
└── Stop.kt                 → Data model
```

**Pattern:** MVVM · StateFlow · Coroutines · Custom Canvas

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Kotlin** | Primary language |
| **StateFlow** | Real-time vehicle position updates |
| **ViewModel** | Lifecycle-aware simulation state |
| **Canvas / View** | Custom route map with emoji auto icons |
| **MVVM** | Clean architecture separation |
| **Coroutines** | Non-blocking simulation loop |
| **CardView** | Route and stats cards |
| **ConstraintLayout** | Splash screen layout |

---

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog or later
- Min SDK: **API 26** (Android 8.0)
- Target SDK: **API 35**

### Run the App
```bash
git clone https://github.com/YOUR_USERNAME/yatri-mitra.git
cd yatri-mitra
```
Open in Android Studio → Click **▶ Run**

### Install APK Directly
Download [`YatriMitra.apk`](https://github.com/SahanaCodes7/Yatri-Mitra/releases/latest/download/YatriMitra.apk) and install on any Android 8.0+ device.

---

## 🎯 Impact Goals

- ✅ Reduce waiting time for **rural labor force and students**
- ✅ Make shared transport as **predictable as city metros**
- ✅ Help drivers optimize trips based on **passenger cluster data**
- ✅ Improve **fuel efficiency** by reducing idle waiting

---

## 🧪 Success Criteria Met

- [x] Vehicle icons move smoothly across screen without "jumping"
- [x] ETA counts down in real-time
- [x] App handles screen rotations (portrait locked)
- [x] Simulation Logic is fully documented

---

## 👨‍💻 Project Info

| Field | Value |
|-------|-------|
| **Project** | #84 |
| **Institution** | VTU · MindMatrix |
| **Category** | Android App Development using GenAI |
| **Theme** | Yatri-Mitra Shared Mobility |
| **Version** | 1.0 |

---

<div align="center">

**Built with ❤️ for rural commuters**

*Yatri-Mitra — Know before you go.*

</div>
