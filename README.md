# Gemini---Jurify
🚀 JuriFy X — Supreme Legal Intelligence Console

JuriFy X is a hackathon-grade, AI-powered legal assistant built to deliver structured, actionable legal guidance with a futuristic neon-cyber interface.
It combines secure authentication, multilingual AI reasoning, gamification, analytics, and PDF exports — all without modern JS frameworks.

🧠 What is JuriFy X?

JuriFy X allows users to:

Enter real-world legal issues

Receive structured legal guidance (rights, steps, documents, notice)

Interact using voice or text

Track progress via XP, levels, and achievements

Maintain a secure, searchable legal history

Export professional legal notices as PDFs

All wrapped in a Marvel-level holographic neon UI.

✨ Core Features
🔐 Authentication & Security

JWT-based authentication

Secure password hashing (Werkzeug)

Token expiry & protected routes

SQLite persistence

🤖 AI Legal Engine

Powered by OpenRouter

Structured responses with 4 mandatory sections:

Your Rights

Immediate Steps

Required Documents

Formal Notice Format

Language-locked output (no disclaimers)

🌍 Multilingual Support (UI + AI)

English

Hindi

Marathi

Tamil

Bengali

Dynamic UI translation via i18n system.

🎮 Gamification System
⭐ XP Rules

+10 XP per AI query

+5 XP for summarizer usage

+5 XP for voice input

+1 XP per day login

Level up every 100 XP

🏅 Achievements

Bronze → 3 queries

Silver → 10 queries

Gold → 25 queries

Diamond → 50+ queries

XP and achievements are calculated from server-side history.

📊 Client-Side Analytics

Tracked locally (no external servers):

Issues processed

Languages used

Voice usage

Summarizer usage

Time spent in app

Visualized in a dedicated analytics panel.

📄 PDF Export

Client-side PDF generation using jsPDF

Exports only the Formal Notice section

Clean, professional formatting

Filename: jurifyx_notice.pdf

Title: JuriFy X Legal Notice

🎨 UI / UX Highlights

Neon gradient cyberpunk background

Glassmorphism hologram cards

Glow-on-hover buttons

Animated logo and transitions

Realtime AI typing animation

Sidebar with collapse animation

Floating labels & modal popups

🧱 Tech Stack
Backend

Python

Flask

SQLite

JWT Authentication

OpenRouter API

Frontend

HTML5

CSS3 (Cyberpunk / Neon Glow)

Vanilla JavaScript

Web Speech API

jsPDF

CDN Libraries Used

Animate.css

Hover.css

FontAwesome

Google Fonts (Orbitron / futuristic fonts)

📁 Project Structure (Max 10 Files)
backend/
├── app.py          # Flask app entry point
├── db.py           # SQLite & DB helpers
├── auth.py         # JWT authentication
└── ai_engine.py    # OpenRouter AI logic

public/
├── index.html      # Main UI
├── style.css       # Neon cyberpunk styling
├── script.js       # Core frontend logic
├── i18n.json       # Language translations
├── analytics.js    # Client-side analytics
└── audio.js        # Voice input handling

⚙️ Setup Instructions
1️⃣ Clone the Repository
git clone <repo-url>
cd jurifyx

2️⃣ Install Backend Dependencies
pip install flask flask-cors pyjwt requests werkzeug

3️⃣ Environment Variables

Set your OpenRouter API key:

OPENROUTER_API_KEY=your_api_key_here

4️⃣ Run the Application
python backend/app.py


Open in browser:

http://localhost:5000

🧪 Ideal Use Cases

Hackathons

Legal tech demos

AI product showcases

Portfolio projects

EdTech / LawTech experiments

🏆 Why JuriFy X Wins Hackathons

Zero framework bloat

Clean architecture

AI + UX + Gamification

Multilingual inclusivity

Secure + scalable foundation

Visually unforgettable

📜 License

This project is intended for educational and demonstration purposes only.

JuriFy X
⚖️ Justice. Intelligence. Futurism.
