<div align="center">

[![RU](https://img.shields.io/badge/🇷🇺_Русский-switch-lightgrey?style=for-the-badge)](README.ru.md)
[![EN](https://img.shields.io/badge/🇬🇧_English-current-cyan?style=for-the-badge)](README.md)

# 🎀 MikuCode

**Terminal AI assistant for coding, Windows automation, and FL Studio music production**

[![Version](https://img.shields.io/badge/version-1.8.2-cyan?style=for-the-badge)](https://github.com/mell_real/mikucode/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/license-Proprietary-red?style=for-the-badge)](LICENSE)
[![Model](https://img.shields.io/badge/model-mikuai--4--kyle-purple?style=for-the-badge)]()
[![Groq](https://img.shields.io/badge/powered%20by-Groq-orange?style=for-the-badge)](https://groq.com)
[![YOLO](https://img.shields.io/badge/YOLO-mode-red?style=for-the-badge)]()

*Free. No credit card. No VPN.*

[Download](#-download) • [Quick Start](#-quick-start) • [Features](#-features) • [Commands](#-commands) • [YOLO](#-yolo-mode) • [FAQ](#-faq)

</div>

---

## 📥 Download

Latest release: **[v1.8.2](https://github.com/mell_real/mikucode/releases/latest)**

| Platform | File | Status |
|----------|------|--------|
| 🪟 **Windows** | `MikuCode.exe` | ✅ Stable |
| 🐧 **Linux** | `MikuCode.AppImage` | 🧪 Testing |
| 🍎 **macOS** | — | ⏳ Planned |

> **Note:** This is a closed-source project. Only compiled binaries are distributed.

### Windows
1. Download `MikuCode.exe` from [Releases](https://github.com/mell_real/mikucode/releases)
2. Run it. No installation needed (portable).
3. On first launch, Windows Defender may warn — click **More info** → **Run anyway**.

### Linux
1. Download `MikuCode.AppImage`
2. Make it executable: `chmod +x MikuCode.AppImage`
3. Run: `./MikuCode.AppImage`

---

## ✨ Features

### 💻 Coding
- **Writes code** — HTML, Python, JavaScript, any files
- **Creates projects** — folders, files, structure
- **Reads and edits** — works with existing files
- **Runs commands** — cmd, PowerShell (Windows) / bash (Linux)

### 🎵 FL Studio Music
- **Generates MIDI** — melodies, bass, chords, drums
- **Creates .flp** — from template or stub
- **Controls tempo** — BPM in the request
- **Understands notes** — C4=60, A4=69, drums (kick=36, snare=38, hat=42)

### 🧠 Memory & Context
- **Long-term memory** — `~/.mikucode/memory/*.md`
- **Skills** — reusable SKILL.md
- **History compression** — token saving
- **Sessions** — autosave and load

### 🌍 Localization
- **EN / RU** — switch on the fly with `/lang`
- **Model responds** in the user's language
- **Everything saved** — language persists between runs

### 🔥 YOLO Mode
- **No confirmations** — acts immediately
- **No questions** — makes assumptions
- **Auto-retry** — tries alternatives on failure
- **30 turns** instead of 10

### 🎨 Interface
- **Real-time hints** — type `/`
- **Arrow selection** — models and providers
- **Colored borders** — Kimi Code style
- **Status line** — limits, history, memory, YOLO

---

## ⚡ Quick Start

### 1. Get a free Groq API key
Register at [console.groq.com](https://console.groq.com) — **no credit card required**.

### 2. Run MikuCode
- **Windows:** double-click `MikuCode.exe`
- **Linux:** `./MikuCode.AppImage`

### 3. Paste your key
On first launch, the app will ask for your Groq API key. It's saved to `~/.mikucode/config.json`.

### 4. Start using
Type `/help` to see all commands.

---

## 🎮 Commands

| Command | Description |
|---------|-------------|
| `/help` | Show help |
| `/model` | Select model (arrow keys) |
| `/provider` | Providers: `select` / `add` / `remove` |
| `/fl` | FL Studio: `midi` / `flp` / `template` |
| `/sessions` | Sessions list, `load <id>` |
| `/settings` | Settings (tempo, history, template) |
| `/thinking` | Level: `low` / `medium` / `high` |
| `/stats` | Full stats + limits |
| `/memory` | Memory: `save <name> <text>` |
| `/skill` | Skills: `create <name> <description>` |
| `/hook` | Show active hooks |
| `/permissions` | Mode: `default` / `plan` / `acceptEdits` / `bypass` |
| `/compact` | Compress history manually |
| `/export` | Export dialog to txt |
| `/lang` | Switch language: `ru` / `en` |
| `/yolo` | YOLO mode: `on` / `off` |
| `/clear` | Clear screen |
| `/exit` | Exit (saves session) |

---

## 🔥 YOLO Mode

YOLO is a **no-confirmation mode**. The agent executes everything immediately, asks nothing, stops for nothing.

```
/yolo on    # Enable
/yolo off   # Disable
```

**What changes:**
- Turn limit: 10 → 30
- No clarifying questions
- Auto-retry on failures
- Agent acts instead of asking

⚠️ **Dangerous:** in YOLO mode, the model can run `del /f /q` without warning. Use with caution.

The status line shows `🔥 YOLO` while the mode is on. The setting is **saved** in `~/.mikucode/config.json`.

---

## 💡 Examples

### Create an HTML page
```
> create folder Test on desktop with index.html saying "Hello world" and open it
```
MikuCode creates the folder, writes the HTML, and opens it in your browser.

### Write a lo-fi track
```
> make a lo-fi track 80 BPM on desktop
```
MikuCode generates MIDI, creates the .flp, and opens FL Studio.

### Save to memory
```
> remember: I prefer dark theme and Python 3.12
```
MikuCode saves the preference for future sessions.

### Switch language
```
> /lang en
Language changed to en (Language saved)
```

---

## 🏗️ Data Structure

All user data is stored in `~/.mikucode/`:

```
~/.mikucode/
├── config.json         # Language, model, provider, settings
├── memory/             # Memory fragments (*.md)
├── skills/             # Skills (SKILL.md)
├── sessions/           # Saved sessions (*.json)
└── hooks/              # Hooks (*.py)
```

**Windows:** `C:\Users\<You>\.mikucode\`
**Linux:** `/home/<you>/.mikucode/`

### Uninstall
Delete the `~/.mikucode` folder. That's it — MikuCode is portable.

---

## 🔧 Configuration

### Settings (via `/settings`)
| Key | Default | Description |
|-----|---------|-------------|
| `thinking` | `low` | Reasoning level: low / medium / high |
| `default_tempo` | `120` | Default BPM for MIDI |
| `fl_template` | `""` | Path to empty.flp template |
| `max_history` | `8` | Messages kept in context |
| `permission_mode` | `default` | default / plan / acceptEdits / bypass |
| `yolo` | `false` | No-confirmation mode |

### Groq Free limits
- **Requests/day:** 1,000
- **Tokens/min:** 8,000
- **Tokens/day:** 200,000

---

## 🎯 Models

| Display name | Real model | Provider |
|--------------|------------|----------|
| `mikuai-4-kyle` | openai/gpt-oss-120b | Groq |
| `mikuai-4-kyle-mini` | openai/gpt-oss-20b | Groq |
| `mikuai-3-legacy` | llama-3.3-70b-versatile | Groq |

---

## 🆚 Comparison with Claude Code

| Feature | Claude Code | MikuCode |
|---------|-------------|----------|
| Free | ❌ | ✅ |
| Works without VPN | ❌ | ✅ |
| FL Studio | ❌ | ✅ |
| Memory | ✅ | ✅ |
| Skills | ✅ | ✅ |
| Subagents | ✅ | ✅ |
| Hooks | ✅ | ✅ |
| YOLO mode | ✅ (dangerous) | ✅ |
| MCP | ✅ | ⚠️ planned |
| Hints | ✅ | ✅ |
| Claude models | ✅ | ❌ (Groq only) |
| Open source | ❌ | ❌ |

---

## ❓ FAQ

**Q: Is MikuCode free?**
A: Yes, 100% free. No credit card, no subscription, no hidden limits.

**Q: Is it open source?**
A: No, MikuCode is closed-source. Only compiled binaries are distributed.

**Q: How to get an API key?**
A: [console.groq.com](https://console.groq.com) → Sign up → API Keys → Create.

**Q: Does it work on Linux?**
A: Yes, AppImage build is in testing. macOS is planned.

**Q: Can I connect Claude/GPT-4?**
A: Yes, via `/provider add` — any OpenAI-compatible endpoint.

**Q: Where are settings stored?**
A: `~/.mikucode/config.json` (language, model, provider, YOLO).

**Q: How to delete everything?**
A: Delete the `~/.mikucode` folder.

**Q: Why does Windows Defender warn me?**
A: Because the .exe isn't code-signed (code signing costs ~$300/year). Click "More info" → "Run anyway". The binary is safe.

**Q: Can I get a virus from MikuCode?**
A: No. MikuCode only executes commands that you (or the AI on your behalf) explicitly request. All data stays local. The only network traffic goes to Groq API.

---

## 🗺️ Roadmap

- [x] EN/RU localization
- [x] YOLO mode
- [x] Persistence (config.json)
- [x] Sessions with save/load
- [x] Hooks from files
- [x] Windows binary (.exe)
- [ ] Linux binary (.AppImage)
- [ ] macOS binary (.dmg)
- [ ] Code signing (Windows)
- [ ] MCP integration
- [ ] Plugins
- [ ] Web UI
- [ ] Voice input

---

## ⚠️ Security

MikuCode runs **any** commands and writes files **without confirmation** (in `default` mode). This is dangerous if you don't trust the model.

**Recommendations:**
- Use `/permissions plan` for safe mode
- Do not run as administrator
- Do not give access to system folders (`C:\Windows`)
- In YOLO mode — extra caution

### What MikuCode sends to the cloud
- Your prompts (to Groq API for processing)
- Tool call results (file contents, command output) — to give the model context
- **Nothing else.** No telemetry, no analytics, no user tracking.

### What stays local
- Config, memory, sessions, skills, hooks — all in `~/.mikucode/`
- Your API key — stored locally in `config.json`

---

## 📝 License

**Proprietary / Freeware.** Free to use, but source code is not distributed.

You may:
- ✅ Use MikuCode for personal and commercial purposes
- ✅ Share the binary with others
- ✅ Report bugs and suggest features

You may NOT:
- ❌ Decompile, reverse-engineer, or modify the binary
- ❌ Redistribute as your own product
- ❌ Remove copyright notices

---

## 🙏 Credits

- [Groq](https://groq.com) — free GPT-OSS models
- [Rich](https://github.com/Textualize/rich) — terminal UI library
- [prompt_toolkit](https://github.com/prompt-toolkit/python-prompt-toolkit) — interactive hints
- [MIDIUtil](https://github.com/MarkCWirt/MIDIUtil) — MIDI generation
- [pyflp](https://github.com/demberto/PyFLP) — FL Studio parsing
- [PyInstaller](https://pyinstaller.org) — binary packaging

---

<div align="center">

**Made with 💙 for those who love code and music**

⭐ Star the project if it helped!

[⬆ Back to top](#-mikucode)

</div>
