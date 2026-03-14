# Mr.BJ — Blackjack AI Tutor Bot

<p align="center">
  <img src="bj.png" alt="Mr.BJ mascot" width="300"/>
</p>

An AI-powered Blackjack educational chatbot prototype built during a major field training program at the **University of Macau**. Mr.BJ teaches players how to play Blackjack through interactive, voice-enabled lessons — and emphasizes **responsible gambling** as a core part of the curriculum.

---

## Overview

Mr.BJ guides users through a 6-step learning journey covering Blackjack rules, betting strategies, probability, and responsible gambling practices. After completing the lessons, users can practice with an AI dealer in a simulated game environment.

The bot uses voice interaction (speech-to-text and text-to-speech) and avatar video narrations to create an engaging, accessible learning experience.

---

## Features

- **6-Step Progressive Learning System**
  | Step | Topic |
  |------|-------|
  | 0 | Basic Rules — objective, card values, ace mechanics |
  | 1 | Betting Methods — minimum bets, double down, split |
  | 2 | Gameplay Flow — dealing, turns, determining winners |
  | 3 | Probability & Strategy — basic strategy, Hi-Lo card counting |
  | 4 | Responsible Gambling — guidelines and self-awareness |
  | 5 | Practice Mode — play against an AI dealer |

- **Voice Interaction** — microphone input (STT via OpenAI Whisper) and spoken responses (TTS via OpenAI API)
- **Avatar Video Narrations** — pre-recorded video of the Mr.BJ character for each lesson step
- **GPT-4 Q&A** — ask questions at any point and get context-aware answers from the AI tutor
- **Voice Commands** — say "Hit" or "Stand" during gameplay, "Next Step" to advance lessons

---

## Tech Stack

| Category | Tools |
|----------|-------|
| Web UI | Streamlit |
| AI/LLM | OpenAI GPT-4 |
| Speech-to-Text | OpenAI Whisper (small model) |
| Text-to-Speech | OpenAI TTS API |
| Audio Processing | pydub, ffmpeg |
| Video Processing | imageio[ffmpeg] |
| Deep Learning | PyTorch (Whisper dependency) |

---

## Project Structure

```
macau_project/
├── made_thread.py           # Main Streamlit application (Mr.BJ bot)
├── prototype_pt_bot.py      # Secondary prototype using OpenAI Assistants API
├── requirements.txt         # Python dependencies
├── packages.txt             # System dependencies (ffmpeg)
├── bj.png                   # Mr.BJ mascot image
├── 0_step.mp3 ~ 5_step.mp3  # Audio narrations for each lesson step
└── result_voice_0_step.mp4  # Avatar video narrations for each lesson step
    ~ result_voice_5_step.mp4
```

---

## Getting Started

### Prerequisites

- Python 3.8+
- An OpenAI API key

### Installation

```bash
# Install system dependencies (macOS)
brew install ffmpeg

# Install Python dependencies
pip install -r requirements.txt
```

### Running the App

```bash
export OPENAI_API_KEY="your-api-key-here"
streamlit run made_thread.py
```

---

## Background

This project was developed as a prototype during a **major field training program at the University of Macau**. The goal was to explore how AI and voice interfaces can be used to create interactive educational tools in a gaming/hospitality context — while also promoting awareness of responsible gambling habits.

The project was presented as part of the program's final showcase, and upon completion, received a **letter of recommendation issued under the name of the University of Macau**.
