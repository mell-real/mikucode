<div align="center">

[![RU](https://img.shields.io/badge/🇷🇺_Русский-switch-lightgrey?style=for-the-badge)](README.ru.md)
[![EN](https://img.shields.io/badge/🇬🇧_English-current-cyan?style=for-the-badge)](README..md)

# 🎀 MikuCode

**Terminal AI assistant for coding, Windows, and FL Studio**

[![Version](https://img.shields.io/badge/version-1.8.2-cyan?style=for-the-badge)](https://github.com/yourname/mikucode)
[![Python](https://img.shields.io/badge/python-3.10+-blue?style=for-the-badge&logo=python)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![Model](https://img.shields.io/badge/model-mikuai--4--kyle-purple?style=for-the-badge)]()
[![Groq](https://img.shields.io/badge/powered%20by-Groq-orange?style=for-the-badge)](https://groq.com)
[![YOLO](https://img.shields.io/badge/YOLO-mode-red?style=for-the-badge)]()

*MikuCode is a free AI assistant in your terminal that writes code, controls Windows, creates music for FL Studio, and remembers your context.*

[Installation](#-installation) • [Features](#-features) • [Commands](#-commands)

</div>

---

## ✨ Features

### 💻 Coding
- **Writes code** — HTML, Python, JavaScript, any files
- **Creates projects** — folders, files, structure
- **Reads and edits** — works with existing files
- **Runs commands** — cmd, PowerShell

### 🎵 Music for FL Studio
- **Generates MIDI** — melodies, bass, chords, drums
- **Creates .flp** — from template or stub
- **Controls tempo** — BPM in the request
- **Understands notes** — C4=60, A4=69, drums (kick=36, snare=38)

### 🧠 Memory and context
- **Long-term memory** — `~/.mikucode/memory/*.md`
- **Skills** — reusable SKILL.md
- **History compression** — token saving
- **Sessions** — autosave and load

### 🤖 Advanced features
- **Subagents** — parallel subtasks
- **Hooks** — intercept tool calls
- **Permissions** — 4 modes (default/plan/acceptEdits/bypass)
- **Multi-provider** — Groq + custom

### 🎨 Interface
- **Real-time hints** — type `/`
- **Arrow selection** — models and providers
- **Colored borders** — Kimi Code style
- **Status line** — limits, history, memory

---

## 🚀 Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourname/mikucode.git
cd mikucode
