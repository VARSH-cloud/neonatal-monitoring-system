# 🍼 Neonatal Sleep Apnea Monitoring System

A real-time neonatal monitoring system designed to detect sleep apnea in infants using hardware sensors integrated with a web-based dashboard. The system enables continuous tracking of breathing patterns, instant detection of abnormalities, and timely alerts to ensure neonatal safety.

---

## 🚀 Overview

This project combines **hardware sensing**, **real-time data processing**, and a **modern web dashboard** to monitor multiple infants simultaneously. It provides healthcare professionals with a simple and effective interface to observe breathing patterns and respond quickly to critical situations.

---

## ✨ Features

* 🔴 **Real-Time Monitoring**
  Continuous tracking of breathing rate from hardware sensors.

* 👶 **Multi-Baby Tracking**
  Monitor up to 10 infants simultaneously on a single dashboard.

* 🚨 **Apnea Detection & Alerts**
  Instant alerts (visual + sound) when abnormal breathing is detected.

* 📊 **Live Dashboard**
  Clean UI displaying breathing values, status, and system overview.

* 📈 **Data Visualization**
  Graphs for analyzing breathing trends over time.

* ⚠️ **Priority Highlighting**
  Critical cases are automatically highlighted for immediate attention.

* 🕒 **Last Alert Tracking**
  Displays time since last apnea event for each infant.

---

## 🧠 System Architecture

```
Sensors → Microcontroller → Data Processing → Backend API → Web Dashboard → Alerts
```

---

## 🛠️ Tech Stack

### Frontend

* React (Vite)
* Tailwind CSS
* Chart.js / Recharts

### Backend

* Python (Flask)
* REST API

### Hardware

* Respiration / ECG / Pressure Sensors
* Microcontroller (Arduino / ESP32)

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

---

### 2️⃣ Install Frontend Dependencies

```bash
npm install
```

---

### 3️⃣ Run Frontend

```bash
npm run dev
```

👉 Open in browser:
`http://localhost:5173`

---

### 4️⃣ Run Backend (Flask)

```bash
python app.py
```

---

## 🔌 API Integration

Frontend fetches real-time data from:

```bash
http://127.0.0.1:5000/babies
```

Example response:

```json
{
  "babies": [
    { "id": 1, "breathing": 45, "status": "NORMAL" },
    { "id": 2, "breathing": 12, "status": "APNEA" }
  ]
}
```

---

## 🧪 Demo Features

* Simulated real-time data using dataset
* Alert triggering on low breathing values
* Dynamic UI updates every second

---

## 🎯 Use Case

This system is designed for:

* Neonatal Intensive Care Units (NICU)
* Hospitals with limited monitoring resources
* Remote infant health monitoring

---

## ⚠️ Note

This is a **prototype system** developed for demonstration and educational purposes. It is not intended for direct clinical use without further validation and regulatory approval.

---

## 🏆 Future Enhancements

* 🤖 AI-based apnea prediction
* 📱 Mobile app integration
* ☁️ Cloud data storage
* 🔔 SMS / notification alerts
* 🧾 Patient history and reports

---

## 👨‍💻 Contributors

* Team Members: *[Add your names here]*

---

## 📌 License

This project is open-source and available for educational and research purposes.

---

## 💡 Tagline

**Ensuring infant safety through real-time monitoring and intelligent alerts.**
