# TRUTHNET AI - Global Digital Truth Verification System

TRUTHNET AI is a full-stack forensic intelligence platform that verifies whether digital media is authentic or manipulated. It supports videos, images, audio, and social links from YouTube, Instagram, and X.

## Core Capabilities
- Deepfake video detection (face swap, GAN artifacts, frame manipulation)
- AI image detection (diffusion artifacts, synthetic textures, shadow inconsistencies)
- Voice cloning detection (spectrogram + synthetic voice signatures)
- Reverse media search (first-seen discovery from internal index + pluggable web providers)
- Metadata forensics (camera, timestamps, editing traces)
- Truth Score engine (multi-model weighted fusion)
- Evidence certificate generation (downloadable forensic report)
- Social media scanner (link ingestion and analysis)
- Global fake media dashboard (aggregated analytics)

## Monorepo Layout
```text
.
+-- backend/                  # FastAPI + AI forensic pipeline + PostgreSQL models
+-- frontend/                 # Next.js + Tailwind UI and dashboard
+-- infra/                    # Docker and deployment assets
+-- docs/                     # Architecture, setup, deployment docs
+-- docker-compose.yml        # Full local stack orchestration
+-- .env.example              # Shared environment template
```

## Quick Start
1. Copy env template and set values:
   - `copy .env.example .env`
2. Start stack:
   - `docker compose up --build`
3. Open apps:
   - Frontend: `http://localhost:3000`
   - Backend API docs: `http://localhost:8000/docs`

## Local Dev (without Docker)
### Backend
```powershell
cd backend
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

### Frontend
```powershell
cd frontend
npm install
npm run dev
```

## Documentation
- [Architecture](./docs/ARCHITECTURE.md)
- [Setup Guide](./docs/SETUP.md)
- [Deployment Guide](./docs/DEPLOYMENT.md)
- [API Reference](./docs/API.md)
