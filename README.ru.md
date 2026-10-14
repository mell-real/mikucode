<div align="center">

[![RU](https://img.shields.io/badge/🇷🇺_Русский-current-cyan?style=for-the-badge)](README.ru.md)
[![EN](https://img.shields.io/badge/🇬🇧_English-switch-lightgrey?style=for-the-badge)](README..md)

# 🎀 MikuCode

**AI-ассистент в терминале для программирования, Windows и FL Studio**

[![Version](https://img.shields.io/badge/version-1.8-cyan?style=for-the-badge)](https://github.com/yourname/mikucode)
[![Python](https://img.shields.io/badge/python-3.10+-blue?style=for-the-badge&logo=python)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)

*MikuCode — это бесплатный AI-ассистент в вашем терминале, который пишет код, управляет Windows, создает музыку для FL Studio и запоминает контекст.*

[Установка](#-установка) • [Возможности](#-возможности) • [Команды](#-команды)

</div>

---

## ✨ Возможности

### 💻 Программирование
- **Пишет код** — HTML, Python, JavaScript, любые файлы
- **Создает проекты** — папки, файлы, структуру
- **Читает и редактирует** — работает с существующими файлами
- **Выполняет команды** — cmd, PowerShell

### 🎵 Музыка для FL Studio
- **Генерирует MIDI** — мелодии, бас, аккорды, ударные
- **Создает .flp** — из шаблона или заготовки
- **Управляет темпом** — BPM в запросе
- **Понимает ноты** — C4=60, A4=69, ударные (kick=36, snare=38)

### 🧠 Память и контекст
- **Долговременная память** — `~/.mikucode/memory/*.md`
- **Skills** — повторно используемые навыки (SKILL.md)
- **Сжатие истории** — экономия токенов
- **Сессии** — автосохранение и загрузка

### 🤖 Расширенные возможности
- **Субагенты** — параллельное выполнение подзадач
- **Хуки** — перехват вызовов инструментов
- **Права доступа** — 4 режима (default/plan/acceptEdits/bypass)
- **Мультипровайдерность** — Groq + собственные провайдеры

### 🎨 Интерфейс
- **Подсказки в реальном времени** — введите `/`
- **Выбор стрелками** — переключение моделей и провайдеров
- **Цветные рамки** — стиль Kimi Code
- **Строка состояния** — лимиты, история, память

---

## 🚀 Установка

### 1. Клонируйте репозиторий
```bash
git clone https://github.com/yourname/mikucode.git
cd mikucode
