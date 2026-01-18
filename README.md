🐉 Comfy Gallery

Comfy Gallery is a universal, local-first gallery for browsing, searching, and managing ComfyUI outputs — images and videos — across multiple drives and folders, with full metadata, prompt, and workflow support.

Built for power users, artists, and studios running multiple ComfyUI setups.

✨ Key Features
🖼️ Media Browsing

View PNG, JPG, WebP, GIF, MP4, WebM, MOV, AVI outputs

High-performance thumbnail cache

Lightbox viewer with keyboard navigation

Video playback directly in the gallery

🧠 ComfyUI Metadata Support

Reads metadata from images and videos:

Prompt & negative prompt

Model name

Sampler, steps, CFG, seed

Resolution, file size, creation date

One-click workflow JSON download

🔍 Advanced Search & Filtering

Keyword search across:

Prompt & negative prompt

Model name

Filename

Seed & parameters

Filters:

File type (Image / Video)

Year & month (e.g. 2025 → January)

Model

Source folder

Sorting by date, name, or file size

📁 Multi-Folder & Multi-Drive Support

Add unlimited output folders

Works across different drives

Each source has:

Custom name

Color indicator

Visible full path

Missing folders are automatically flagged

♻️ Duplicate Detection

Fast hash-based duplicate detection

Duplicates hidden by default

Optional toggle to show duplicates

🔄 Refresh & Rescan

Quick Refresh → scans only new files

Full Rescan → rebuilds the index if needed

Designed for large archives (10k+ files)

🧭 Setup Wizard (First Launch)

Guided 3-step onboarding:

Welcome

Add output folders

Scan & launch

No config editing required

🧩 Technical Overview

Backend: Python + Flask

Database: SQLite

Frontend: Pure HTML / CSS / JS (no frameworks)

Video metadata: FFprobe (optional, recommended)

Thumbnail cache: Local filesystem

📂 Project Structure
comfy-gallery/
├── comfy_gallery.py        # Main Flask application
├── requirements.txt        # Python dependencies
├── start.bat               # Windows one-click launcher
├── README.md               # Documentation
├── LICENSE                 # MIT License
├── .gitignore
├── static/
│   └── logo.jpg            # Comfy Gallery logo
└── templates/
    ├── setup.html          # First-run setup wizard
    └── index.html          # Main gallery UI

🚀 Installation (Windows)
1️⃣ Download & Extract

Download the ZIP and extract it anywhere on your machine.

2️⃣ Start the App

Double-click:

start.bat


This will:

Create a virtual environment (if needed)

Install dependencies

Start the local server

3️⃣ Open in Browser

Your browser will open automatically, or visit:

http://localhost:8189

🧙 First-Time Setup

On first launch, you’ll see the Setup Wizard:

Welcome

Add your ComfyUI output folders

Example:

C:\ComfyUI\output
D:\AI\ComfyUI\renders
E:\Archive\2025


Launch Gallery

Folders can be added or removed later from the UI.

➕ Adding New Output Folders

From the gallery UI:

Click “+ Add” in the Sources panel

Paste the folder path

(Optional) Set a display name & color

Click Add & Scan

Files are never modified or deleted.

🔄 Keeping the Gallery Updated

🔄 Refresh
Scans only newly added files (fast)

📁 Rescan
Rebuilds the entire index (safe but slower)

⚙️ Optional Dependencies

For best video support, install FFmpeg:

👉 https://ffmpeg.org/download.html

If FFmpeg is not available:

Videos still play

Thumbnails fall back to placeholders

🔐 Privacy & Security

100% local

No cloud, no telemetry

No external services

All data stays on your machine

📜 License

MIT License — free for personal and commercial use.

🌱 Roadmap (Planned)

Scene / Shot / Episode tagging (S## / P##)

After Effects / Harmony project awareness

Prompt version comparison

Export galleries (HTML / ZIP)

Studio-level tagging & notes

👤 Author

Built by Bora Özkut
AI Artist & Generative Workflow Designer
