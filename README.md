# ⚔️ Duel Agent Simulation

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![LLaMA](https://img.shields.io/badge/LLaMA%203-8B-6C63FF?style=for-the-badge)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**A multi-agent debate arena powered by LLaMA 3 — watch two AI personas argue it out.**

[🤗 Live Demo on Hugging Face](https://huggingface.co/spaces/bhavnaa22/duel-agent-simulation) · [🐛 Report Bug](https://github.com/bhavnaa22/duel-agent-simulation/issues)

</div>

---

## 🎯 What is This?

Two AI agents, one debate topic, zero mercy. You pick the personas (Philosopher vs. Comedian? Scientist vs. Poet?), set the number of turns, and watch them go. Each agent maintains its character and responds to the other across multiple rounds — built on LLaMA 3 via Together AI.

Deployed as a Streamlit app on **Hugging Face Spaces** using Docker.

## ✨ Features

- 🎭 **Fully customizable personas** — any character, any style
- 🔄 **Multi-turn conversations** — agents respond to each other, not just a prompt
- 🚀 **Live on Hugging Face Spaces** — no setup needed to try it
- 🐳 **Dockerized** — reproducible, portable, production-ready
- ⚡ **Powered by LLaMA 3 (8B)** via Together AI

## 🏗️ Architecture

```
User Input (persona 1, persona 2, turns)
        │
        ▼
  Streamlit UI  ──►  Agent Loop
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
         Agent 1               Agent 2
      (LLaMA 3 via         (LLaMA 3 via
       Together AI)         Together AI)
              │                     │
              └──────────┬──────────┘
                         ▼
                   Duel transcript
```

## 🚀 Run Locally

```bash
git clone https://github.com/bhavnaa22/duel-agent-simulation
cd duel-agent-simulation
pip install -r requirements.txt
streamlit run src/streamlit_app.py
```

Or with Docker:
```bash
docker build -t duel-agent .
docker run -p 8501:8501 duel-agent
```

Set your Together AI API key:
```bash
export TOGETHER_API_KEY=your_key_here
```

## 📁 Project Structure

```
duel-agent-simulation/
├── src/
│   └── streamlit_app.py    # Main Streamlit app
├── Dockerfile              # Docker config for HF Spaces
├── requirements.txt
└── README.md
```

## 🔧 Tech Stack

| Component | Technology |
|-----------|-----------|
| UI | Streamlit |
| LLM | LLaMA 3 (8B) via Together AI |
| Deployment | Hugging Face Spaces |
| Containerization | Docker |
| Language | Python 3.10+ |
