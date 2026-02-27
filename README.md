🚀 CivicShield AI

AI-Powered Cyber Resilience Platform

Built by Divyansh Gupta

⸻

🔥 Overview

CivicShield AI is an intelligent cyber security platform designed to:
	•	🔍 Detect vulnerabilities (SQLi, XSS, Injection flaws)
	•	🎯 Perform attack surface analysis
	•	🛡️ Detect phishing threats
	•	📊 Calculate real-time Cyber Risk Score
	•	📈 Provide executive security dashboard
	•	📄 Generate professional PDF pentest reports
	•	🔐 Secure APIs with JWT authentication

It transforms raw scan data into actionable intelligence.

⸻

🧠 Why CivicShield AI?

Traditional scanners dump findings.

CivicShield AI:
	•	Prioritizes risk
	•	Quantifies impact
	•	Visualizes threat trends
	•	Converts technical findings into executive insights

Built for modern cyber defense.

⸻

🏗️ System Architecture
flowchart TD

User -->|Login/Register| AuthAPI
User -->|Start Scan| ScanAPI
User -->|Phishing Check| PhishingAPI
User -->|View Dashboard| Dashboard

ScanAPI --> ScanEngine
PhishingAPI --> PhishingDetector

ScanEngine --> Database
PhishingDetector --> Database

Database --> Dashboard
Database --> ReportGenerator

ReportGenerator --> PDFReport

🧩 Internal Architecture

flowchart LR

subgraph Backend
    A[FastAPI App]
    B[Auth Module]
    C[Scan Engine]
    D[Phishing Detector]
    E[Risk Engine]
    F[PDF Generator]
end

subgraph Database
    G[(Scan Table)]
    H[(Vulnerability Table)]
    I[(User Table)]
end

A --> B
A --> C
A --> D
C --> G
C --> H
D --> H
A --> E
E --> H
A --> F
F --> H

https://chatgpt.com/s/m_69a211bc83a48191a5928d2a5f3e745d

📊 Dashboard Intelligence Flow

sequenceDiagram
    participant User
    participant FastAPI
    participant Database
    participant RiskEngine
    participant ChartJS

    User->>FastAPI: GET /dashboard
    FastAPI->>Database: Fetch scan + vuln data
    Database-->>FastAPI: Data
    FastAPI->>RiskEngine: Calculate risk score
    RiskEngine-->>FastAPI: Score + Label
    FastAPI-->>User: Render dashboard.html
    User->>ChartJS: Render charts

⚙️ Tech Stack

Layer
Technology
Backend
FastAPI
Database
SQLAlchemy + SQLite
Auth
JWT + bcrypt
Visualization
Bootstrap + Chart.js
Reporting
Custom PDF Generator
Security
Custom Scan Engine


🛡️ Core Features

✅ Automated Scan Engine
	•	SQL Injection Detection
	•	XSS Detection
	•	Parameter Fuzzing
	•	Endpoint Discovery

✅ Phishing Detection
	•	URL heuristic analysis
	•	Suspicious pattern detection

✅ Risk Scoring Engine

Weighted severity model:

Critical × 10
High × 6
Medium × 3
Normalized to 0–100

✅ Executive Dashboard
	•	Risk distribution pie chart
	•	7-day scan trend
	•	Latest vulnerabilities
	•	Dynamic risk score
	•	Auto-refresh

✅ PDF Report Generator
	•	Target summary
	•	Findings
	•	Risk breakdown
	•	Professional formatting

⸻
'''
📂 Project Structure

attack_surface_analyzer/
│
├── main.py
├── analyzer/
│   ├── engine.py
│   ├── phishing_detector.py
│   └── pdf_report_generator.py
│
├── api/
│   └── auth.py
│
├── database/
│   ├── db.py
│   └── models.py
│
├── templates/
│   └── dashboard.html
│
├── static/
│
└── README.md
'''
🔐 API Endpoints

Method
Endpoint
Description
GET
/dashboard
Security dashboard
POST
/register
Create user
POST
/login
JWT login
POST
/scan
Start vulnerability scan
POST
/phishing/check
Phishing detection
GET
/scans
List scans
GET
/scan/status/{id}
Scan status
GET
/scan/results/{id}
Scan results
GET
/report/{id}
Generate PDF report

🧪 How to Run

git clone https://github.com/Divyansh2602/civicshield-ai.git
cd civicshield-ai

python -m venv .venv
.venv\Scripts\activate

pip install -r requirements.txt

python -m uvicorn main:app --reload

http://127.0.0.1:8000/dashboard

📈 Example Risk Output
	•	Critical: 138
	•	High: 378
	•	Medium: 338
	•	Risk Score: 50 / 100 (HIGH)

Dynamic, normalized, realistic.

🧠 Future Enhancements
	•	AI-powered exploit prediction
	•	CVSS scoring integration
	•	Real-time WebSocket updates
	•	Role-based access control
	•	Threat intelligence feeds
	•	Multi-tenant deployment
