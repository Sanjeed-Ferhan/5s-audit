# 5S Camera Audit

Mobile-friendly 5S tools that use your phone camera and AI vision (Google Gemini).

## Apps

- **`index.html` — Floor Scan.** Open the camera, point it at the floor/work area, and it scans live: it records 5S findings per pillar with severity, then generates a full 5S report (print / save PDF / download / CSV).
- **`checklist.html` — Guided Audit.** One screen at a time: take a photo per 5S standard, AI scores it 0-5, then a summary. Good for a structured checklist audit.

## Setup (once, on each phone)

1. Open the site on your phone.
2. Tap **AI key** / **AI key settings**.
3. Paste your Google Gemini API key (create one free at https://aistudio.google.com/apikey).
   It is stored only in your phone's browser (localStorage) and sent directly to Google.

Without a key the apps run in **demo mode** (simulated results) so you can try the flow.

## Notes

- Camera access requires HTTPS — GitHub Pages provides this.
- Data stays in your browser. Use the in-app CSV / report export to keep records.
- The API key is entered per device and is not stored in this repository.
