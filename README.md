# 📝 WhisperYT

Simple CLI tool to transcribe audio from:

- YouTube URLs
- Local audio files

using OpenAI Whisper.

## ✨ Features

- Automatic YouTube audio download (`yt-dlp`)
- Timestamped transcript output
- Full merged transcript output
- Lightweight single-script workflow

## 📦 Requirements

- Python 3.8+
- `ffmpeg` installed and available in PATH

## 🚀 Installation

```bash
git clone https://github.com/ashenclock/WhisperYT.git
cd WhisperYT
pip install -r requirements.txt
```

## ▶️ Usage

```bash
python stt.py
```

When prompted, provide:

- a YouTube link, or
- a local file path (e.g. `.mp3`, `.wav`, `.m4a`)

## 📄 Output

The script creates:

- timestamped segments (`[mm:ss - mm:ss] ...`)
- full plain-text transcript

in `<input_name>_transcription.txt`.

## 🔗 Dependencies

- [openai-whisper](https://github.com/openai/whisper)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)

