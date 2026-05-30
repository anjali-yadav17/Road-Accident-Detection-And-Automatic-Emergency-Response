# 🚨 Road Accident Detection & Automatic Emergency Response System

An Android application that automatically detects road accidents using smartphone sensors and instantly alerts emergency contacts with the user's live location. The system aims to reduce emergency response time and improve road safety by providing automated SOS assistance during critical situations.

---

## 📱 Features

### 🚗 Real-Time Accident Detection
- Uses the device's Accelerometer Sensor to monitor sudden impacts.
- Detects potential accidents based on configurable impact thresholds.
- Prevents false triggers using cooldown mechanisms.

### 📍 Live Location Tracking
- Retrieves the user's current GPS location using Google's Fused Location Provider.
- Generates a Google Maps location link for accurate emergency assistance.

### 🚨 Automatic SOS Alerts
- Sends emergency SMS messages to registered contacts.
- Includes the user's live location in the alert message.
- Supports multiple emergency contacts.

### ⏳ SOS Countdown Timer
- Provides a configurable countdown before sending alerts.
- Allows users to cancel false accident detections.

### 🔔 Foreground Monitoring Service
- Runs continuously in the background.
- Uses Android Foreground Services for reliable accident monitoring.
- Displays persistent notifications while monitoring is active.

### 📜 Incident History
- Maintains a history of detected incidents.
- Records alert status:
  - Processing
  - Sent
  - Cancelled

### ⚙️ User Customization
- Adjustable accident sensitivity.
- Configurable SOS delay timer.
- Emergency contact management.

---

## 🏗️ System Architecture

```text
Accelerometer Sensor
        ↓
Accident Detector
        ↓
Accident Detection Service
        ↓
Countdown Timer
        ↓
Emergency Manager
        ↓
GPS Location Fetch
        ↓
SMS Alert with Location
        ↓
Emergency Contacts
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Kotlin | Android Development |
| Jetpack Compose | Modern UI Development |
| Android Foreground Service | Continuous Monitoring |
| SensorManager | Accident Detection |
| Fused Location Provider | Live Location Tracking |
| SMS Manager | Emergency Alerts |
| SharedPreferences | Local Data Storage |
| Material Design 3 | User Interface |
| Navigation Compose | Screen Navigation |

---

## 📂 Project Structure

```text
app/
│
├── MainActivity.kt
│   └── Main UI and Navigation
│
├── AccidentDetector.kt
│   └── Accelerometer-based accident detection
│
├── AccidentDetectionService.kt
│   └── Background monitoring service
│
├── EmergencyManager.kt
│   └── Location retrieval and SMS handling
│
└── ui/theme/
    └── App theme and styling
```

---

## 🔑 Permissions Required

The application requires the following Android permissions:

```xml
ACCESS_FINE_LOCATION
ACCESS_COARSE_LOCATION
SEND_SMS
FOREGROUND_SERVICE
POST_NOTIFICATIONS
VIBRATE
```

---

## 🚀 How It Works

### Step 1: Register Emergency Contacts
Users add emergency contact numbers within the application.

### Step 2: Start Monitoring
The foreground service begins monitoring accelerometer sensor data.

### Step 3: Accident Detection
When acceleration exceeds the configured threshold, an accident event is triggered.

### Step 4: SOS Countdown
A countdown timer starts, allowing the user to cancel if no accident occurred.

### Step 5: Emergency Alert
If not cancelled:
- Current GPS location is fetched.
- SMS alerts are sent to all emergency contacts.
- Incident history is updated.

---

## 📸 Screens Included

- Splash Screen
- Onboarding Screen
- Dashboard
- Emergency Contacts Management
- Settings
- Incident History
- Accident Detection Alert Dialog
- Success Confirmation Screen

---

## 💡 Future Enhancements

- Automatic Emergency Calling
- Cloud Database Integration
- Real-Time Hospital Notification
- Crash Severity Analysis using Machine Learning
- Integration with Smart Wearables
- Emergency Contact Verification
- Voice-Based SOS Trigger

---

## 🎯 Use Case

This application can be used by:

- Daily commuters
- Bike riders
- Car drivers
- Delivery personnel
- Emergency response systems
- Fleet management solutions

---

## 👩‍💻 Developed By

**Anjali Yadav**

Android Application developed as a road safety solution using sensor-based accident detection and automated emergency response mechanisms.

---

## 📜 License

This project is developed for educational and research purposes.

Feel free to use, modify, and enhance the project for learning and innovation.
