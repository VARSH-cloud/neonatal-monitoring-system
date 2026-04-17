SMART WEARABLE NEONATAL APNEA DETECTOR WITH PREDICTIVE ANALYSIS
Neonatal apnea is a life‑threatening condition in which breathing stops for several seconds, especially in premature infants. Early detection can prevent serious complications or death. A real-time neonatal monitoring system designed to detect sleep apnea in infants using hardware sensors integrated with a web-based dashboard. The system enables continuous tracking of breathing patterns, instant detection of abnormalities, and timely alerts to ensure neonatal safety.

Overview
This project combines hardware sensing, real-time data processing, and a modern web dashboard to monitor multiple infants simultaneously. It provides healthcare professionals with a simple and effective interface to observe breathing patterns and respond quickly to critical situations. The system is designed to support NICUs and resource‑constrained hospitals by offering a low‑cost alternative to high‑end commercial monitors.

Features
Real-Time Monitoring Continuous tracking of breathing rate from hardware sensors.

Multi-Baby Tracking Monitor up to 10 infants simultaneously on a single dashboard.

Apnea Detection & Alerts Instant visual + sound alerts when abnormal breathing is detected (e.g., breathing rate below threshold).

Live Dashboard Clean UI displaying breathing values, status, and system overview.

Data Visualization Graphs (e.g., trend plots) for analyzing breathing patterns over time.

Priority Highlighting Critical cases are automatically highlighted for immediate attention.

Last Alert Tracking Displays time since last apnea event for each infant.

System Architecture
Sensors → Microcontroller → Data Processing → Backend API → Web Dashboard → Alerts
The sensor data from the infant (respiration / ECG / pressure) is captured by a microcontroller (Arduino/ESP32), sent to a Flask backend, and then pushed to a React dashboard for real‑time visualization and alerts.

Tech Stack
Frontend
React (Vite): Fast, modern component‑based UI with hot‑reload.
Tailwind CSS: Utility‑first styling for responsive layouts.
Chart.js / Recharts: Real‑time graphs for breathing trends.
Backend
Python (Flask): Lightweight backend serving a REST API for the frontend.
REST API: Exposes /api/babies endpoint returning current breathing status for all infants.
Hardware
Respiration Sensor: Flex sensor placed on a chest belt to detect chest expansion/contraction for breathing‑rate estimation.
Blood Oxygen & Heart‑Rate Sensor: MAX30100 pulse‑oximetry module (PPG‑based) for heart rate and SpO₂.
Microcontroller: ESP32 (WiFi‑enabled) for sensor data acquisition, processing, and transmission to the backend.
Cooling / Object Temperature: TEC1‑12706 Peltier module (used optionally for infant‑surface temperature sensing or local cooling in your specific setup).
Output Indicators: Buzzer and LED for local audio‑visual alerts when apnea or abnormal HR/SpO₂ is detected.
Passive Components: 4 kΩ and 1 kΩ resistors used in voltage‑divider or bias circuits for the flex sensor and other analog inputs.
Power System: Li‑Po battery with a charging module for portable, continuous operation of the ESP32‑based unit.
Interfacing: Jumper wires for all connections between ESP32, sensors, buzzer, LED, and Peltier module.
Installation & Setup
Clone Repository
git clone https://github.com/VARSH-cloud/neonatal-monitoring-system/edit/main/README.md
cd neonatal-monitoring-system
Install Frontend Dependencies
npm install
Run Frontend
npm run dev
Open in browser: http://localhost:

Run Backend (Flask)
python app.py
API Integration
Frontend fetches real-time data from:

http://
Example response:

{
  "babies": [
    { "id": 1, "breathing": 45, "status": "NORMAL" },
    { "id": 2, "breathing": 12, "status": "APNEA" }
  ]
}
Demo Features
Simulated real‑time data using pre‑defined dataset or generated values.
Alert triggering on low breathing values (below apnea threshold).
Dynamic UI updates every second for live monitoring.
Visual highlighting of critical infants on the dashboard during apnea events.
Use Case
This system is designed for:

Neonatal Intensive Care Units (NICU)
Hospitals with limited monitoring resources
Remote infant health monitoring (e.g., tele‑NICU or rural clinics)
In India, where many NICUs are understaffed and high‑end monitors are costly, this low‑cost system can help reduce workload and improve early detection of apnea.
Note
This is a prototype system developed for demonstration and educational purposes. It is not intended for direct clinical use without further validation, regulatory approval, and medical supervision. The current version relies on simulated data and basic threshold‑based detection.

Future Enhancements
AI‑based apnea prediction: Integrate a lightweight ML model to predict apnea events before they occur.
Mobile app integration: Build Android/iOS apps for nurses and parents to receive alerts.
Cloud data storage: Store patient data and breathing trends in the cloud for long‑term analysis.
SMS / notification alerts: Send SMS or push notifications to caregivers during critical events.
Patient history and reports: Generate printable or digital reports for doctors and parents.
Contributors
Team Name: ZENITH
Team Members: SUMERA BEGUM, SANJAY JONATH S, VARSHINI M, LAKSHAN
License
This project is open-source and available for educational and research purposes.

Tagline
Ensuring infant safety through real‑time monitoring and intelligent alerts for neonatal sleep apnea.
