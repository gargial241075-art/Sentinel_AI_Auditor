<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=220&section=header&text=VAULT_SENTINEL&fontSize=72&fontColor=00F5FF&fontAlignY=38&desc=AI+Audit+%26+Deepfake+Detection+Platform&descAlignY=58&descSize=20&animation=fadeIn" width="100%"/>

<br/>

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Python-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-CSS-38bdf8?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Framer Motion](https://img.shields.io/badge/Framer-Motion-FF0055?style=for-the-badge&logo=framer&logoColor=white)](https://www.framer.com/motion/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org/)

<br/>

[![Status](https://img.shields.io/badge/⚡_STATUS-IN_DEVELOPMENT-00F5FF?style=flat-square)](#)
[![Frontend](https://img.shields.io/badge/Frontend-COMPLETE-00e676?style=flat-square)](#)
[![Backend](https://img.shields.io/badge/Backend-COMPLETE-00e676?style=flat-square)](#)
[![Integration](https://img.shields.io/badge/Integration-IN_PROGRESS-ffaa00?style=flat-square)](#)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&size=16&pause=1200&color=00F5FF&center=true&vCenter=true&multiline=false&repeat=true&width=500&height=40&lines=SENTINEL+PROTOCOL+ACTIVE...;MULTI-LAYER+CRYPTOGRAPHIC+ANALYSIS...;NEURAL+SHIELD+L3+ENGAGED...;VAULT+ENCRYPTION+VERIFIED." alt="Typing SVG" />

<br/>

> **An enterprise-grade AI platform for deepfake forensics and AI model integrity auditing.**
> Built with a glassmorphism dark UI, real-time WebSocket log streaming, and a modular FastAPI backend.

</div>

---

## 🖼️ Screenshots

<div align="center">

| Detection Hub — Upload | Detection Hub — Analytics |
|:---:|:---:|
| ![Detection Hub](./screenshots/detection-hub-1.png) | ![Detection Analytics](./screenshots/detection-hub-2.png) |

| AI Audit — Model Workspace | AI Audit — Parameters |
|:---:|:---:|
| ![AI Audit](./screenshots/ai-audit-1.png) | ![AI Parameters](./screenshots/ai-audit-2.png) |

</div>

> 📌 *Add your screenshots to a `/screenshots` folder in the repo root and rename them accordingly.*

---

## ✨ What does it do?

Vault Sentinel is split into **two completely independent workspaces**:

### 🎭 Deepfake Check — Detection Hub
Analyse any media file for signs of AI manipulation using multi-layer forensic techniques.

| Input | Analysis |
|-------|----------|
| 🎬 **Video** | Frame-by-frame neural decomposition, eyeblink rate verification, lip-sync phase-shift analysis |
| 🎙️ **Audio** | MFCC fingerprinting, spectral centroid analysis, voice clone detection |
| 🖼️ **Image** | ELA (Error Level Analysis), GAN artefact probability, edge density profiling |
| 📄 **Text** | Type-token ratio, semantic coherence scoring, AI-generation probability |

**Output:** Authenticity Score (0–100), Threat Level (Low / Medium / High), Radar chart across 5 dimensions, real-time Process Log stream.

---

### 🧠 AI Audit — Model Compliance Workspace
Audit AI models and datasets against global safety and fairness standards.

| Category | Parameters Checked |
|----------|--------------------|
| ⚖️ **Bias Analysis** | Demographic Parity · Semantic Alignment · Cross-Regional Sensitivity |
| 🔒 **Safety & Privacy** | PII Leakage Scanning · Prompt Injection Resistance · Adversarial Robustness |
| ⚡ **Performance & Logic** | Hallucination Threshold · Reasoning Consistency · Throughput Efficiency |

**Output:** Bias Score, Safety Index, Performance Score, Overall Grade (A–F), Recommendations list, HMAC-signed Integrity Certificate (PASS / FAIL).

---

## 🏗️ Project Structure

```
vault-sentinel/
│
├── 📂 sentinel-v3/                     ← Next.js Frontend
│   ├── app/
│   │   ├── page.tsx                    ← Main dashboard (mode orchestrator)
│   │   ├── layout.tsx                  ← Font + metadata setup
│   │   └── globals.css                 ← Glassmorphism design tokens
│   ├── components/sentinel/
│   │   ├── header.tsx                  ← Mode switcher (Deepfake / AI Audit)
│   │   ├── sidebar.tsx                 ← Navigation + Enterprise badge
│   │   ├── detection-hub.tsx           ← Media upload + Video/Audio/Image/Text tabs
│   │   ├── process-log.tsx             ← Real-time scanning step timeline
│   │   ├── audit-analytics.tsx         ← Authenticity score gauge + radar chart
│   │   ├── company-workspace.tsx       ← Model/dataset upload + parameter toggles
│   │   ├── audit-parameters.tsx        ← 3-column Bias/Safety/Performance grid
│   │   ├── certification-card.tsx      ← PASS / FAIL certificate display
│   │   ├── dimension-scores.tsx        ← Animated progress bars
│   │   ├── diagnostics-panel.tsx       ← [SYS] [SEC] [AUD] live log panel
│   │   └── radar-chart.tsx             ← SVG radar / pentagon chart
│   ├── hooks/
│   │   └── useSentinel.ts              ← React hook: API calls + WS stream state
│   ├── lib/
│   │   └── sentinel-api.ts             ← Typed API client for all endpoints
│   └── package.json
│
└── 📂 sentinel-backend/                ← FastAPI Backend (Python)
    ├── main.py                         ← App entry point + CORS config
    ├── requirements.txt
    ├── .env.example
    ├── core/
    │   ├── config.py                   ← Pydantic settings (reads .env)
    │   └── logging.py                  ← Structured logging setup
    ├── models/
    │   └── schemas.py                  ← All Pydantic request/response models
    ├── routers/
    │   ├── detect.py                   ← POST /detect/media
    │   ├── audit.py                    ← POST /audit/model
    │   ├── logs.py                     ← WS  /logs/stream
    │   └── report.py                   ← GET /report/certificate
    ├── services/
    │   ├── media_analyzer.py           ← OpenCV + Librosa + Pillow analysis engines
    │   ├── model_auditor.py            ← Pandas + sklearn compliance audit
    │   └── certificate_service.py      ← HMAC-SHA256 certificate generation
    └── utils/
        ├── file_handler.py             ← Upload validation, MIME check, temp storage
        └── hashing.py                  ← SHA256 + HMAC signing helpers
```

---

## 🛠️ Tech Stack

<div align="center">

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| Next.js | 15 (App Router) | Framework |
| TypeScript | 5 | Type safety |
| Tailwind CSS | 3 | Styling |
| Framer Motion | Latest | Animations & transitions |
| Recharts | Latest | Radar chart visualisations |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| FastAPI | 0.115.5 | REST + WebSocket API framework |
| Uvicorn | 0.32.1 | ASGI server |
| OpenCV | 4.10.0 | Video frame analysis |
| Librosa | 0.10.2 | Audio feature extraction |
| Pillow | 11.0.0 | Image ELA analysis |
| Pandas | 2.2.3 | Dataset bias audit |
| scikit-learn | 1.5.2 | Statistical scoring |
| Pydantic | 2.9.2 | Data validation + settings |
| cryptography | 43.0.3 | HMAC-SHA256 certificate signing |

</div>

---

## 🚀 Setup & Installation

### Prerequisites
```
Node.js  ≥ 18.0
Python   ≥ 3.10
pnpm or npm
```

---

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/vault-sentinel.git
cd vault-sentinel
```

---

### 2️⃣ Frontend Setup

```bash
cd sentinel-v3
pnpm install        # or: npm install
pnpm dev            # Starts at http://localhost:3000
```

---

### 3️⃣ Backend Setup

> ⚠️ **Important:** You must `cd` into the `sentinel-backend` folder before running any pip commands. Running pip from the parent folder is the most common cause of `requirements.txt not found` errors.

```bash
# Navigate INTO the backend folder first
cd sentinel-backend

# Verify requirements.txt is visible
ls                    # macOS / Linux → you should see main.py, requirements.txt ...
dir                   # Windows

# Create a virtual environment
python -m venv venv

# Activate it
source venv/bin/activate          # macOS / Linux
venv\Scripts\activate             # Windows CMD
venv\Scripts\Activate.ps1         # Windows PowerShell

# Install all dependencies (must be inside sentinel-backend/)
pip install -r requirements.txt

# Copy environment config
cp .env.example .env
# Open .env and set CERT_SECRET_KEY to any random string

# Start the API server
uvicorn main:app --reload --port 8000
```

Backend API docs: **http://localhost:8000/docs**

---

### 4️⃣ Connect Frontend to Backend

**Add to** `sentinel-v3/.env.local`:
```env
NEXT_PUBLIC_SENTINEL_API_URL=http://localhost:8000
```

**Copy the integration files** (if not already present):
```bash
# From the project root
cp sentinel-backend/frontend-integration/sentinel-api.ts  sentinel-v3/lib/
cp sentinel-backend/frontend-integration/useSentinel.ts   sentinel-v3/hooks/
```

**Run both servers** (two separate terminals):
```bash
# Terminal 1 — Frontend
cd sentinel-v3
pnpm dev

# Terminal 2 — Backend
cd sentinel-backend
source venv/bin/activate
uvicorn main:app --reload --port 8000
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/detect/media` | Upload video / audio / image / text for deepfake analysis |
| `POST` | `/audit/model` | Upload model file or dataset for compliance audit |
| `WS` | `/logs/stream` | Real-time WebSocket log stream |
| `GET` | `/report/certificate` | Generate HMAC-signed Integrity Certificate |
| `POST` | `/report/verify` | Verify a certificate's signature |
| `GET` | `/health` | Liveness probe |

### Example: Detect Media
```bash
curl -X POST http://localhost:8000/detect/media \
  -F "file=@your_video.mp4" \
  -F "media_type=video"
```

**Response:**
```json
{
  "job_id": "3f7a9c...",
  "authenticity_score": 87.4,
  "threat_level": "Low",
  "is_deepfake": false,
  "confidence": 0.748,
  "radar_dimensions": {
    "accuracy": 88.1,
    "safety": 82.3,
    "bias": 75.0,
    "privacy": 85.6,
    "transparency": 70.2
  }
}
```

### WebSocket Stream
```javascript
const ws = new WebSocket(
  'ws://localhost:8000/logs/stream?job_type=media&media_type=video'
);
ws.onmessage = (e) => {
  const entry = JSON.parse(e.data);
  // { type, step, progress, tag, message, status, timestamp }
};
```

---

## 📊 Development Status

```
██████████████████████░░░  88% Complete
```

| Module | Status |
|--------|--------|
| Detection Hub UI | ✅ Complete |
| AI Audit Mode UI | ✅ Complete |
| Glassmorphism Design System | ✅ Complete |
| Framer Motion Animations | ✅ Complete |
| FastAPI Backend — All Endpoints | ✅ Complete |
| WebSocket Log Streaming | ✅ Complete |
| HMAC Certificate Generation | ✅ Complete |
| Typed API Client (`sentinel-api.ts`) | ✅ Complete |
| React Hook (`useSentinel.ts`) | ✅ Complete |
| Frontend ↔ Backend Integration | 🔄 In Progress |
| Real ML Model Integration | 🔜 Planned |
| Docker Deployment | 🔜 Planned |

---

## 🔮 Roadmap

- [ ] Complete full frontend ↔ backend integration
- [ ] Integrate FaceForensics++ deepfake detection model
- [ ] Add AASIST voice anti-spoofing for audio analysis
- [ ] Integrate AI Fairness 360 for real bias metrics
- [ ] JWT authentication layer
- [ ] PDF certificate download
- [ ] Docker Compose one-command setup
- [ ] Deploy to cloud (Vercel + Railway / Render)

---

## 🔧 Troubleshooting

**`requirements.txt not found`**
```bash
# Make sure you are INSIDE the sentinel-backend folder
cd sentinel-backend
pip install -r requirements.txt
```

**`ModuleNotFoundError` after installing**
```bash
# Make sure your virtual environment is activated
source venv/bin/activate      # macOS / Linux
venv\Scripts\Activate.ps1     # Windows PowerShell
```

**CORS error in browser**
```bash
# Confirm the backend is running on port 8000
# Confirm .env.local has:
NEXT_PUBLIC_SENTINEL_API_URL=http://localhost:8000
```

**WebSocket not connecting**
```bash
# Check the backend URL uses ws:// not http://
# sentinel-api.ts automatically converts http → ws
```

---

## 👩‍💻 About

<div align="center">

Built by **Gargi Gupta**

*B.Tech AI/ML · Baderia Global Institute of Engineering and Management, Jabalpur*

[![GitHub](https://img.shields.io/badge/GitHub-@yourusername-181717?style=flat-square&logo=github)](https://github.com/yourusername)

</div>

---

## 📄 License

```
MIT License — free to use, fork, and build on.
```

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&animation=fadeIn" width="100%"/>

**If this project helped you or you found it interesting, drop a ⭐**

*Made with 💙, way too much caffeine, and a deep distrust of unverified media.*

</div>
