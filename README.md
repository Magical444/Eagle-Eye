# EAGLE EYE
Offline document intelligence, OCR and searchable archive management for Windows 10/11 (x64).

Eagle Eye scans a folder (NAS share, mapped drive or local disk), OCRs image-based PDFs and images locally with
Tesseract/OCRmyPDF (English, Urdu, Hindi), writes searchable PDFs into a separate output folder that mirrors the
source hierarchy, and indexes all text in a local SQLite FTS5 database. Original files are never modified.
After installation nothing needs the internet: no cloud OCR, no telemetry, no login.

Stack: Electron + React + TypeScript (electron-vite) / Python 3.11 worker (OCRmyPDF, PyMuPDF, Pillow) / SQLite FTS5.

## Quick start (development)
1. Install Node.js 20+, Python 3.11 x64, Tesseract (UB Mannheim build, with Urdu + Hindi data) and Ghostscript 64-bit.
2. `scripts\setup.cmd`  then  `scripts\check-system.cmd`  then  `scripts\start-eagle-eye.cmd`
3. Settings: choose source + output folders and OCR language, then Dashboard > Scan archive > Start processing.

## Build the installer
`scripts\build-windows.cmd` (build machine needs internet once; see docs/INSTALLATION.md). Output in `dist\`.

See `docs/` for the user manual, installation, troubleshooting, architecture and test plan.
