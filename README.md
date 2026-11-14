<div align="center">

# Radiant Hajira — Digital Staff Attendance System
### Cloud-Connected Attendance Tracking & Automated Reporting Platform

[![Live Application](https://img.shields.io/badge/Live_App-Launch_Portal-2563eb?style=for-the-badge&logo=githubpages&logoColor=white)](https://shohidulrpl.github.io/attendance/)
[![Automation](https://img.shields.io/badge/Workflows-n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](#system-architecture)
[![Database](https://img.shields.io/badge/Cloud_DB-Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](#tech-stack)
[![Reporting](https://img.shields.io/badge/Logs-Google_Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)](#tech-stack)

</div>

---

### Overview
**Radiant Hajira** is a lightweight, browser-based staff attendance management system built to replace manual paper registers and repetitive spreadsheet data entry. Staff members can log daily check-ins and check-outs from any mobile or desktop browser, while an automated cloud pipeline validates entries, stores records in real time, and updates structured attendance reports.

**Live Deployment:** [https://shohidulrpl.github.io/attendance/](https://shohidulrpl.github.io/attendance/)

---

### Key Features
* **Fast Web Interface:** Mobile-responsive, zero-install frontend hosted on GitHub Pages for quick daily check-in and check-out access.
* **Real-Time Cloud Synchronization:** Instant submission handling via webhooks with persistent storage in **Firebase**.
* **Automated Spreadsheet Reporting:** Automatically formats and appends daily attendance logs into **Google Sheets** for HR and management review.
* **Timestamp & Status Validation:** Captures accurate submission timestamps and categorizes attendance statuses (On-Time, Late, Leave, Absent) without manual calculation.
* **Low-Maintenance Architecture:** Serverless frontend paired with modular **n8n** automation workflows for high reliability and zero server overhead.

---

### System Architecture

```text
┌─────────────────────────────┐
│   Web Frontend (HTML/JS)    │
│  Hosted on GitHub Pages     │
└──────────────┬──────────────┘
               │ HTTPS POST (JSON Payload)
               ▼
┌─────────────────────────────┐
│   n8n Automation Engine     │
│  Webhook & Validation Logic │
└──────┬───────────────┬──────┘
       │               │
       ▼               ▼
┌─────────────┐ ┌─────────────────────┐
│  Firebase   │ │   Google Sheets     │
│  Cloud DB   │ │  Automated Reports  │
└─────────────┘ └─────────────────────┘
```

---

### Tech Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Hosting:** GitHub Pages
* **Workflow Automation:** n8n (Webhooks & Scheduled Triggers)
* **Backend & Storage:** Firebase Realtime Database / Firestore, Google Sheets API

---

### Deployment & Configuration
1. **Frontend Hosting:** Static assets are served directly from the `main` branch via **GitHub Pages**.
2. **Webhook Integration:** Form submissions send structured JSON payloads (`staff_id`, `action`, `timestamp`, `device_meta`) to an **n8n** webhook endpoint.
3. **Data Persistence:** The n8n workflow writes verified logs to **Firebase** and syncs daily summary rows to **Google Sheets**.

---

### Author
**Md. Shohidul Islam**  
Web App Developer & Workflow Automation Engineer — Chattogram, Bangladesh  
* **Portfolio:** [shohidulrpl.github.io/portfolio](https://shohidulrpl.github.io/portfolio/)  
* **GitHub:** [@shohidulrpl](https://github.com/shohidulrpl)
