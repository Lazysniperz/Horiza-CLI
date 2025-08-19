
---

# ⚡ Horiza CLI – Local Voice-Controlled AI Assistant

Horiza CLI is your **terminal-native, voice-activated AI assistant**, powered entirely by **local LLMs via Ollama**.
Think of it as Jarvis, but **offline, hackable, and built for devs**. It listens for a wake word, understands your voice, calls tools when needed, and even talks back using TTS.

No cloud. No lag. Just **your AI, on your machine.**

---

## 🚀 Features

* 🗣 **Voice-activated** — Wake it up with `Horiza`
* 🧠 **Runs fully local** — Powered by Any AI By ollama but tested with **Horiza**
* 🔧 **Tool-calling** — Extend with LangChain (e.g., get time, run commands, etc.)
* 🔊 **Talks back** — Text-to-speech responses via `pyttsx3`
* 🌍 **Example built-in tool** — Get the current time in any city
* 🔐 **Optional hybrid mode** — Integrate with OpenAI API if you want
* 🖥 **Terminal-first design** — Lightweight, hackable, and fast

---

## ▶️ How It Works

### 🔹 Startup & Model Setup

* Loads a local Ollama model (`qwen3:1.7b`) via `ChatOllama`
* Registers tools (like `get_time`) with LangChain

### 🔹 Wake Word Detection

* Listens through your mic (`device_index=0` by default)
* Activates conversation mode when it hears **“Horiza”**

### 🔹 Voice Command Handling

* Records & transcribes your spoken command
* Passes it to the LLM → which may invoke a tool
* Replies using `pyttsx3` with customizable voices

### 🔹 Timeout

* If inactive for **30s**, resets back to wake word listening

---

## 🤖 Getting Started

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Pull the model (Qwen3:1.7B)

```bash
ollama pull qwen:1.7b
```

### 3. Run Horiza CLI

```bash
python main.py
```

That’s it — say **“Horiza”** and start talking! 🦾

## ⚡ Why Horiza CLI?

Because assistants like this should be:
✅ **Local-first** – Your data, your rules
✅ **Hackable** – Add any tool you want
✅ **Lightweight** – Works on everyday machines
✅ **Fun** – Who doesn’t want their own Jarvis?

---

✨ *Built by Sniper (Ahmed Shafiq) — Lazy but Precise™*

---
