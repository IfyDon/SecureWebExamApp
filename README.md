# 🔒 Secure Exam Web App

A secure, browser‑based examination system built with **Flask** (Python backend) and **HTML/CSS/JavaScript** frontend.  
It enforces fullscreen mode, prevents tab switching, disables copy/paste and keyboard shortcuts, monitors the camera, and saves results to an Excel file.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## ✨ Features

- **Fullscreen enforcement** – Exam runs in fullscreen; leaving fullscreen terminates the exam.
- **Tab / window change detection** – Switching tabs or losing focus ends the exam.
- **Right‑click disabled** – Prevents context menu.
- **Copy / paste disabled** – Blocks `Ctrl+C`, `Ctrl+V`, and mouse copy/paste.
- **Keyboard shortcuts blocked** – All `Ctrl`/`Cmd` combinations are disabled.
- **Camera monitoring** – Live video overlay (user must grant permission).
- **2‑minute timer** – Auto‑submits when time expires.
- **5 MCQ questions** – Pre‑loaded Python questions (easily customisable).
- **Excel result storage** – Scores are saved to `exam_results.xlsx` on the server.
- **Responsive design** – Works on any screen size.

---

## 🛠️ Technologies Used

| Layer       | Technology                                      |
|-------------|-------------------------------------------------|
| Backend     | Python 3.8+, Flask, openpyxl                   |
| Frontend    | HTML5, CSS3, JavaScript (vanilla)              |
| Security    | Browser Fullscreen API, Visibility API, Keyboard/ContextMenu prevention |
| Camera      | MediaDevices.getUserMedia                       |

---

## 📁 Project Structure

SecureWebExamApp/
├── app.py # Flask application (backend)
├── requirements.txt # Python dependencies
├── .gitignore # Ignore secret_key.txt, excel files, etc.
├── templates/
│ ├── register.html # Registration page
│ ├── exam.html # Exam page (questions, timer, camera)
│ └── result.html # Score display page
└── README.md # This file


---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- `pip` (Python package installer)
- A modern web browser (Chrome, Edge, Firefox) with camera access

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/IfyDon/SecureWebExamApp.git
   cd SecureWebExamApp

Create a virtual environment (recommended)
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

Install dependenies 
pip install -r requirements.txt

Run the app
python app.py
Open your browser and go to http://127.0.0.1:5000

🧪 How to Use

    Registration – Enter your name, class, and registration number. Read the rules and click START EXAMINATION.

    Exam – The browser will request fullscreen and camera access.

        Answer 5 MCQ questions.

        Timer counts down from 2 minutes.

        Use Previous / Next to navigate.

        SUBMIT EXAM or wait for time expiry.

        Any security violation (tab switch, fullscreen exit) immediately terminates the exam.

    Result – Your score and pass/fail status are shown. Results are automatically saved to exam_results.xlsx on the server.
