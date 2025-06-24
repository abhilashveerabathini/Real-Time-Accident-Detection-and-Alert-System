 
# 🚨 Real-Time Accident Detection and Alert System

A real-time surveillance solution designed to detect accidents from live CCTV or video streams using computer vision and deep learning techniques. Once an accident is detected, the system immediately triggers an alert to emergency responders, reducing response time and potentially saving lives.

#Requirements
1.Download and install Anaconda Distribution
2.Create account in Twilio which provides paid programmable communication tools, we can also use 7-days free trial

#Procedure
1.Download the files and extract it in "C:\Users\Admin" path.
2.Launch Jupyter notebook from anaconda Navigator.
3.Open the folder in Jupyter notebook.
4.Create Account in Twilio.
5.Get virtual phone number, account sid and auth token for your Twilio account.
6.Enter those details in "Accident Detection-Video.ipynb" program file.
7.Also enter the phone number which you have to send the SMS.
8.Now, Run the code.

#📌 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [How It Works](#-how-it-works)
- [Installation](#-installation)
- [Usage](#-usage)
- [Alert Mechanism](#-alert-mechanism)
- [Future Scope](#-future-scope)


# ✅ Features

- Real-time accident detection using CCTV/live video feed.
- Deep learning-based model for collision detection.
- Automated alert system via SMS or Email.
- Easy-to-use monitoring dashboard (optional frontend).
- Configurable alert contacts and detection thresholds.
- Logs every incident with timestamp for later analysis.



#🛠️ Tech Stack

| Component     | Technology              |
|---------------|--------------------------|
| Language      | Python                   |
| CV Model      | OpenCV, YOLOv5 / TensorFlow |
| Alerts        | Twilio (SMS) / SMTP (Email) |
| Deployment    | Localhost / Cloud /  |




#🧠 Architecture

The system follows a modular pipeline for real-time accident detection and alerting:

            ┌──────────────────────┐
            │   CCTV / Video Feed  │
            └────────┬─────────────┘
                     │
                     ▼
            ┌──────────────────────┐
            │  Frame Processing    │
            │   (OpenCV)           │
            └────────┬─────────────┘
                     │
                     ▼
            ┌──────────────────────┐
            │  Accident Detection  │
            │  (YOLO / CNN Model)  │
            └────────┬─────────────┘
                     │
                     ▼
            ┌──────────────────────┐
            │  Event Validation    │
            │ (Threshold Logic)    │
            └────────┬─────────────┘
                     │
         ┌───────────▼──────────────┐
         │     Alert System         │
         │ (Twilio / Email / API)   │
         └───────────┬──────────────┘
                     │
                     ▼
            ┌──────────────────────┐
            │  Emergency Services  │
            │  or Monitoring Team  │
            └──────────────────────┘


#🚀 How It Works
System continuously reads frames from CCTV or video input.
Deep learning model identifies unusual vehicle motion (sudden stops, collisions).
If an accident is detected:
Alert message is sent instantly to predefined contacts.
Logs the incident with date/time and snapshot (optional).


#⚙️ Installation
1. Clone the Repository
      git clone https://github.com/abhilashveerabathini/Real-Time-Accident-Detection-and-Alert-System.git
      cd real-time-accident-detection
2. Install Dependencies
      pip install -r requirements.txt
3. Run the Application
      python app.py

#🖥️ Usage
Replace video_source = 0 with your camera or video file.
Set emergency contact info in config.py or .env.
Monitor logs for alerts and detection timestamps.

#📬 Alert Mechanism
SMS Alerts: Integrated using Twilio API.
Each alert includes:
Time of incident
Location (if available)
Type of event
Optional image snapshot

#🔮 Future Scope
Add GPS and sensor data from vehicles for accuracy
Automatic call to emergency services (via VoIP)
Dashboard for authorities with live analytics
Multiple camera input support

