<div align="center">

# 🎙️ WhisperYT

**YouTube → Text transcription powered by OpenAI Whisper**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org)
[![Whisper](https://img.shields.io/badge/OpenAI-Whisper-412991.svg)](https://github.com/openai/whisper)
[![yt-dlp](https://img.shields.io/badge/yt--dlp-latest-red.svg)](https://github.com/yt-dlp/yt-dlp)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)

</div>

---

## 📋 Overview

WhisperYT is a lightweight CLI tool that downloads audio from any YouTube video (or accepts a local audio file) and transcribes it into a formatted `.txt` file with timestamps using OpenAI's Whisper model.

## ✨ Features

- 🎬 **YouTube Download** — Automatically extracts audio from any YouTube URL via `yt-dlp`
- 🗣️ **Speech-to-Text** — Accurate transcription using OpenAI Whisper (`medium` model by default)
- ⏱️ **Timestamps** — Output includes `[mm:ss - mm:ss]` segment-level timestamps
- 📁 **Local Files** — Also supports transcription of local `.wav`/`.mp3` files

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- [FFmpeg](https://ffmpeg.org/) installed and available in your `PATH`

### Installation

```bash
git clone https://github.com/ashenclock/WhisperYT.git
cd WhisperYT
pip install -r requirements.txt
```

### Usage

```bash
python stt.py
```

When prompted, enter either:
- A **YouTube URL** (e.g. `https://www.youtube.com/watch?v=...`)
- A **local file path** (e.g. `./my_audio.wav`)

### Output Example

```
TRANSCRIPTION WITH TIMESTAMPS
==================================================

[00:00 - 00:05] Hello and welcome to this tutorial.
[00:05 - 00:12] Today we'll be talking about machine learning.
...

==================================================
FULL TRANSCRIPTION:

Hello and welcome to this tutorial. Today we'll be...
```

## 📁 Project Structure

```
├── stt.py               # Main script (download + transcribe)
├── requirements.txt     # Python dependencies
├── LICENSE
└── README.md
```

## 🛠️ Configuration

You can change the Whisper model size by modifying the `model_name` parameter in `transcribe_audio()`:

| Model | Size | Speed | Accuracy |
|-------|------|-------|----------|
| `tiny` | 39M | ⚡⚡⚡ | ★☆☆ |
| `base` | 74M | ⚡⚡ | ★★☆ |
| `small` | 244M | ⚡ | ★★☆ |
| `medium` | 769M | 🐢 | ★★★ |
| `large` | 1550M | 🐌 | ★★★ |

## 📜 License

This project is licensed under the GPL-3.0 License — see the [LICENSE](LICENSE) file for details.
