# 🚍 TSRTC SmartTicket

> Intelligent bus ticketing system with QR validation and machine learning — built for the Hyderabad TSRTC network.

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.x-black?logo=flask)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey?logo=sqlite)
![scikit-learn](https://img.shields.io/badge/ML-scikit--learn-orange?logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Overview

**TSRTC SmartTicket** is a full-stack web application that lets passengers book bus tickets online and receive **QR-code-based tickets with dynamic expiry**, ensuring efficient and fraud-resistant travel across Hyderabad's TSRTC network.

The system integrates **machine learning models** to enhance decision-making — including fare prediction, crowd estimation, route recommendation, and peak-hour detection.

---

## 🖼️ Screenshots

> _Add screenshots or a demo GIF here._

---

## 🏗️ Architecture

The application follows a **monolithic full-stack architecture** with clear separation of concerns:

```
Frontend (HTML/JS/CSS)
       ↓
Backend (Flask REST APIs)
       ↓
Database (SQLite) + ML Layer (scikit-learn) + QR System
```

---

## 🧰 Tech Stack

| Layer     | Technology                                 |
|-----------|--------------------------------------------|
| Frontend  | HTML5, CSS3, JavaScript, Chart.js          |
| Backend   | Python, Flask, Flask-CORS                  |
| Database  | SQLite                                     |
| QR Code   | `qrcode`, Pillow                           |
| ML Models | scikit-learn (Linear Regression, Random Forest, Decision Tree) |

---

## 🎯 Features

### 🎫 Ticket Booking
- Supports multiple TSRTC routes with 10–20 stops
- Automatic fare calculation using ML
- QR code generation with **30-minute expiry**
- Real-time countdown timer with visual alerts

### 🛣️ Routes & Stops
- Forward and return journey toggle
- Live stop search functionality

### 📊 Ticket Management
- Booking history tracking
- Active vs. expired ticket status
- User analytics dashboard

### 🤖 Machine Learning
| Model | Algorithm | Purpose |
|-------|-----------|---------|
| Fare Prediction | Linear Regression | Estimate ticket cost |
| Crowd Estimation | Regression | Predict bus occupancy |
| Route Recommendation | Random Forest | Suggest optimal routes |
| Peak Hour Detection | Decision Tree | Flag high-traffic periods |

---

## 🔌 REST API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/routes` | Fetch available routes |
| POST | `/api/fare` | Predict fare |
| POST | `/api/book` | Book a ticket |
| GET | `/api/predict/*` | ML predictions |
| GET | `/api/bookings` | Ticket history |

---

## 🗂️ Project Structure

```
transport_ticketing/
├── backend/          # Flask app, routes, API logic
├── frontend/         # HTML, CSS, JS files
├── ml_models/        # Trained ML models
├── database/         # SQLite schema and seed data
├── requirements.txt
└── README.md
```

---

## ▶️ Getting Started

Follow these steps carefully to run the project on your laptop.

---

### Step 1 — Install Python

Make sure Python 3.10 or above is installed on your system.

- Download from: https://www.python.org/downloads/
- During installation on Windows, **check the box that says "Add Python to PATH"**
- To verify installation, open a terminal (Command Prompt on Windows, Terminal on Mac/Linux) and run:

```bash
python --version
```

You should see something like `Python 3.11.x`.

---

### Step 2 — Install Git

Git is needed to download (clone) the project.

- Download from: https://git-scm.com/downloads
- Install with default settings
- To verify, run:

```bash
git --version
```

---

### Step 3 — Clone the Repository

This downloads the project files to your laptop.

```bash
git clone https://github.com/your-username/transport_ticketing.git
```

> Replace `your-username` with the actual GitHub username.

---

### Step 4 — Open the Project Folder

```bash
cd transport_ticketing
```

---

### Step 5 — Install Dependencies

This installs all the Python libraries the project needs.

```bash
pip install -r requirements.txt
```

> If `pip` doesn't work, try `pip3 install -r requirements.txt`

---

### Step 6 — Run the Application

```bash
python run.py
```

> If `python` doesn't work, try `python3 run.py`

---

### Step 7 — Open in Browser

Once the server starts, open your browser and go to:

```
http://localhost:5000
```

You should see the TSRTC SmartTicket app running locally.

---

### Common Issues

| Problem | Fix |
|---------|-----|
| `python` not recognized | Reinstall Python and check "Add to PATH" |
| `pip` not recognized | Use `pip3` instead, or reinstall Python |
| Port 5000 already in use | Change the port in `run.py` to `5001` |
| Module not found error | Run `pip install -r requirements.txt` again |

---

## 🔐 Current Limitations

- No user authentication (planned)
- Basic input validation only
- SQLite limits production scalability

---

## 🚀 Planned Enhancements

### Scalability & Performance
- Migrate to PostgreSQL / MySQL
- Introduce Redis caching
- Migrate to FastAPI (async backend)

### Security
- JWT-based authentication
- Role-based access: Admin / User / Conductor
- HTTPS and API rate limiting

### Real-Time Features
- Live bus tracking via WebSockets
- ETA prediction and push notifications (ticket expiry, arrivals)

### Payments
- UPI / Card payment integration
- Payment confirmation before ticket generation

### QR Validation
- Conductor-side QR scanner app
- Real-time ticket validation

### ML Improvements
- LSTM for time-series crowd prediction
- Dynamic surge pricing model
- Automated model retraining pipeline
- Feature expansion: weather, events, holidays

### Frontend
- Responsive mobile-first UI
- Progressive Web App (PWA)
- Offline ticket access

---

## 🌟 Key Highlights

- Full-stack development (Frontend + Backend + ML)
- Solves a real-world public transport problem
- End-to-end API design and system architecture
- Machine learning integration with practical use cases
- Extensible, modular design ready for production upgrades

---

## 🤝 Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change, then submit a pull request.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
