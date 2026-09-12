Triage Assistant 🩺

A lightweight web app for preliminary medical triage:

- *Instant AI results* from free-text symptoms (Google Gemini API)
- *Photo upload* of the affected area (drag & drop or tap) — sent to the AI for context
- *English / हिन्दी language switch* — the whole UI and AI answers translate
- *Text-to-speech* — results are read aloud automatically, with a Listen/Stop button, in the selected language

> ⚠️ Disclaimer: preliminary guidance only, not a substitute for professional medical advice.

## Run

No build tools or npm needed — only Python (already installed):

bash
cd triage-app
python -m http.server 8734


Then open http://localhost:8734

## First-run setup

On first use the app asks for a *free Google Gemini API key* (get one at https://aistudio.google.com/apikey). The key is stored only in your browser's localStorage.

## Files

| File | Purpose |
|------|---------|
| index.html | Page structure |
| styles.css | Styling (responsive, mobile-friendly) |
| i18n.js | English + Hindi strings, language switching |
| triage.js | Gemini API integration (JSON-structured triage output) |
| app.js | UI wiring: upload, analyze, render, speech synthesis |

## Notes

- Severity levels: emergency 🚨 / urgent ⚠️ / see_doctor 🏥 / routine ✅
- Hindi text-to-speech needs a Hindi voice installed on the device (standard on Android/Windows; optional on some desktops — the app falls back gracefully)
- Everything runs client-side; no server or database required
