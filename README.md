🐉 Comfy Gallery

A universal, local-first gallery for browsing, searching, and managing ComfyUI outputs (images & videos) across multiple folders and drives, with full prompt, metadata, and workflow support.
Designed for power users, AI artists, and studios running multiple ComfyUI setups.

✨ Features
🖼️ Image & Video Support
PNG, JPG, WebP, GIF, MP4, WebM, MOV, AVI

🧠 ComfyUI Metadata Parsing
Prompt & negative prompt
Model name
Sampler, steps, CFG, seed
Resolution, file size, creation date

📥 Workflow Extraction
Download embedded ComfyUI workflow JSON with one click
🔍 Advanced Search & Filtering
Keyword search across:
Prompt
Negative prompt
Model name
Filename
Seed & parameters
Filters:
File type (image / video)
Year & month
Model
Source folder
Sorting by date, name, size

📁 Multi-Folder / Multi-Drive Support

Unlimited output folders

Each folder has:

Custom name
Color indicator
Visible full path
Missing folders are automatically flagged
♻️ Duplicate Detection
Fast hash-based detection
Duplicates hidden by default
Optional toggle to show duplicates

🔄 Refresh & Rescan
Quick refresh → scans only new files
Full rescan → rebuilds entire index

🧙 Setup Wizard

First-run onboarding

No manual config editing required

📦 Installation
Method 1: Download Release (Recommended)

# Download the latest release from GitHub
# Extract the ZIP anywhere on your machine
# Run the application
```
python comfy_gallery.py
```

Method 2: Clone from GitHub
```bash
git clone https://github.com/your-username/comfy-gallery.git
cd comfy-gallery
```
```bash
python -m venv .venv
source .venv/bin/activate
```
pip install -r requirements.txt
```
```bash
starty.bat
```
🚀 First-Time Setup (Setup Wizard)

On first launch, Comfy Gallery automatically opens a 3-step setup wizard:

Welcome

Add ComfyUI Output Folders

Scan & Launch Gallery

Example folder paths:

C:/ComfyUI/output
D:/AI/ComfyUI/renders
E:/Comfyui-Outputs/2026

🎯 Usage
Web Interface
# Open in your browser
http://localhost:8189
From the UI you can:

Browse all outputs in a grid

Click any image or video to open the lightbox

View full prompt & parameters

Download workflow JSON

Copy prompt to clipboard

🔍 Search & Filters
Keyword Search

Searches across:

Prompt

Negative prompt

Model

Filename

Seed & parameters
Filters

File Type: Image / Video

Year: 2024 / 2025 / 2026

Month: January → December

🔄 Refresh & Rescan
Model: FLUX, SDXL, Z-Image, etc.
# Quick refresh (new files only)
curl http://localhost:8189/api/refresh
# Full rescan (rebuild index)
curl http://localhost:8189/api/scan


📁 Folder Management (API)
Validate a folder

curl -X POST http://localhost:8189/api/sources/validate \
  -H "Content-Type: application/json" \
  -d '{
    "path": "E:/ComfyUI/output"
  }'
  
Add a folder

curl -X POST http://localhost:8189/api/sources/add \
  -H "Content-Type: application/json" \
  -d '{
    "path": "E:/ComfyUI/output",
    "name": "Main ComfyUI",
    "color": "#8b5cf6"
  }'

Remove a folder (files are NOT deleted)
curl -X POST http://localhost:8189/api/sources/remove \
  -H "Content-Type: application/json" \
  -d '{
    "path": "E:/ComfyUI/output"
  }'

┌─────────────────────────┐
│   ComfyUI Output Files  │
│ (PNG / GIF / MP4 etc.)  │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│     Comfy Gallery        │
│  - Metadata parsing     │
│  - Prompt extraction    │
│  - Workflow JSON        │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│   Web Gallery UI         │
│  - Search / Filter       │
│  - Lightbox viewer       │
│  - Workflow download     │
└─────────────────────────┘

🛠️ Requirements

Python 3.10+

ComfyUI (for generating outputs)

Optional (Recommended)
# FFmpeg for video thumbnails
ffmpeg -version


Install if missing:

# macOS
brew install ffmpeg

# Ubuntu / Debian
sudo apt install ffmpeg

# Windows (Chocolatey)
choco install ffmpeg

🧹 Reset / Clean Start
# Stop the app first (Ctrl+C)

rm -f gallery.db
rm -rf static/galleryout
rm -f config.json

python comfy_gallery.py

🤝 Contributing

Contributions are welcome:

Bug reports

Feature requests

UI improvements

Metadata extensions

Studio / pipeline features

📄 License

MIT License — see LICENSE for details.

🙏 Credits

Created by Bora Özkut
AI Artist & Generative Workflow Designer

⭐ If you find Comfy Gallery useful, consider starring the repository.

