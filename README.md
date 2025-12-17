# JuriFy - AI-Powered Legal Intelligence

## ✨ Features

- 🤖 **AI-Powered Analysis** - Uses Google Gemini AI to analyze legal issues
- 🔐 **User Authentication** - Secure JWT-based login/registration system
- 🌍 **Multi-Language Support** - Available in English, Hindi, Marathi, Tamil, and Bengali
- 🎮 **Gamification** - XP system, levels, and achievement badges
- 📜 **Query History** - Save and search past legal queries
- 🎤 **Voice Input** - Speak your legal issue instead of typing
- 📄 **PDF Export** - Export legal notices as PDF documents
- ⚡ **Smart Caching** - Reduces API calls and saves quota
- 🆓 **Free Tier** - Try 5 queries/day without registration

## 🖼️ Screenshots

The app features a cyberpunk-themed UI with:
- Animated Vanta.js NET background on login
- Neon glow effects and glass morphism design
- Responsive two-panel layout for input/output

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Google Gemini API Key ([Get one here](https://makersuite.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/jurifyx.git
   cd jurifyx
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   # Primary API key (required)
   GEMINI_API_KEY=your_gemini_api_key_here
   
   # Backup API keys (optional) - auto-fallback when quota exhausted
   GEMINI_API_KEY_2=your_second_api_key
   GEMINI_API_KEY_3=your_third_api_key
   
   SECRET_KEY=your_secret_key_for_jwt
   CACHE_EXPIRY_HOURS=48
   ```

4. **Run the application**

   python app.py


5. **Open in browser**

   http://localhost:5000


## 📁 Project Structure

```
jurifyx/
├── app.py                 # Flask backend (API, auth, AI processing)
├── jurifyx.db            # SQLite database
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (create this)
├── view_db.py           # Database viewer utility
├── public/
│   ├── index.html       # Main HTML file
│   ├── style.css        # Cyberpunk CSS theme
│   ├── script.js        # Frontend JavaScript
│   └── i18n.json        # Translations (5 languages)
└── README.md
```

## 🔧 Configuration

| Environment Variable | Description | Default |
|---------------------|-------------|---------|
| `GEMINI_API_KEY` | Your Google Gemini API key | Required |
| `SECRET_KEY` | JWT secret for authentication | Auto-generated |
| `CACHE_EXPIRY_HOURS` | Hours before cached responses expire | 48 |

## 📡 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/register` | Register new user |
| POST | `/auth/login` | Login and get JWT token |

### Legal Analysis
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/process` | Analyze legal issue (authenticated) |
| POST | `/free/process` | Analyze legal issue (free tier) |
| POST | `/free/status` | Check free tier usage |

### History & XP
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/history` | Get user's query history |
| GET | `/xp` | Get user's XP and badges |
| DELETE | `/history/:id` | Delete history item |

### Cache Management
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/cache/stats` | Get cache statistics |
| POST | `/cache/clear` | Clear all cache |

## 🗄️ Database Schema

The app uses SQLite with 5 tables:

- **users** - User accounts (id, name, email, password)
- **history** - Query history with AI responses
- **xp_events** - XP tracking for gamification
- **cache** - API response caching
- **free_usage** - Free tier rate limiting

View database contents:

python view_db.py


## 🎯 AI Response Format

JuriFy analyzes legal issues and returns 4 sections:

1. **Your Rights** - Legal rights related to the issue
2. **Immediate Steps** - Actionable steps to take
3. **Required Documents** - Documents needed for the case
4. **Formal Notice** - Professional legal notice template

## 🌐 Supported Languages

| Code | Language |
|------|----------|
| en | English |
| hi | Hindi (हिंदी) |
| mr | Marathi (मराठी) |
| ta | Tamil (தமிழ்) |
| bn | Bengali (বাংলা) |

## 🏆 Gamification System

- **XP Rewards**: Earn XP for each query (10 XP fresh, 2 XP cached)
- **Bonus XP**: +5 for using summarize, +5 for voice input
- **Levels**: Level up every 100 XP
- **Badges**: 🥉 Bronze (3 queries), 🥈 Silver (10), 🥇 Gold (25), 💎 Diamond (50)

## 🔑 Multi-API Key Fallback

JuriFy supports up to 3 Gemini API keys with automatic fallback:

- When the first API key's quota is exhausted, it automatically switches to the second
- When the second is exhausted, it switches to the third
- Helps maximize uptime and handle high traffic
- Get multiple free API keys from [Google AI Studio](https://makersuite.google.com/app/apikey)

```env
GEMINI_API_KEY=your_primary_key
GEMINI_API_KEY_2=your_backup_key
GEMINI_API_KEY_3=your_third_key
```

## ⚡ Caching System

- Responses are cached for 48 hours by default
- Cache saves API quota and speeds up repeated queries
- Use "Force Fresh" button to bypass cache
- Cache indicator shows if response is from cache or fresh

## 🆓 Free Tier

- 5 queries per day without registration
- Resets automatically after 24 hours
- Always uses cache to conserve API quota
- Register for unlimited access

## 🛠️ Tech Stack

**Backend:**
- Python 3.8+
- Flask (web framework)
- SQLite (database)
- PyJWT (authentication)
- Google Generative AI (Gemini)

**Frontend:**
- Vanilla JavaScript
- CSS3 with custom properties
- Vanta.js (animated backgrounds)
- Font Awesome (icons)
- jsPDF (PDF export)

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## ⚠️ Disclaimer

JuriFy provides AI-generated legal information for educational purposes only. It is not a substitute for professional legal advice. Always consult a qualified lawyer for legal matters.


🚀 JuriFy X — Supreme Legal Intelligence Console

JuriFy X is a hackathon-grade, AI-powered legal assistant built to deliver structured, actionable legal guidance with a futuristic neon-cyber interface. It combines secure authentication, multilingual AI reasoning, gamification, analytics, and PDF exports — all without modern JS frameworks.

🧠 What is JuriFy X?

JuriFy X allows users to:

Enter real-world legal issues

Receive structured legal guidance (rights, steps, documents, notice)

Interact using voice or text

Track progress via XP, levels, and achievements

Maintain a secure, searchable legal history

Export professional legal notices as PDFs

All wrapped in a Marvel-level holographic neon UI.

✨ Core Features 🔐 Authentication & Security

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

🎮 Gamification System ⭐ XP Rules

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

🧱 Tech Stack Backend

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

📁 Project Structure (Max 10 Files) backend/ ├── app.py # Flask app entry point ├── db.py # SQLite & DB helpers ├── auth.py # JWT authentication └── ai_engine.py # OpenRouter AI logic

public/ ├── index.html # Main UI ├── style.css # Neon cyberpunk styling ├── script.js # Core frontend logic ├── i18n.json # Language translations ├── analytics.js # Client-side analytics └── audio.js # Voice input handling

⚙️ Setup Instructions 1️⃣ Clone the Repository git clone cd jurifyx

2️⃣ Install Backend Dependencies pip install flask flask-cors pyjwt requests werkzeug

3️⃣ Environment Variables

Set your OpenRouter API key:

OPENROUTER_API_KEY=your_api_key_here

4️⃣ Run the Application python backend/app.py

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

JuriFy X ⚖️ Justice. Intelligence. Futurism.
