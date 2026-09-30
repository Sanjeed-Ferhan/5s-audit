# 5S Camera Audit

Camera + AI (Google Gemini) 5S auditing apps.

- **`/` (index.html) — Floor Scan:** open the camera, scan the floor, get findings and a full 5S report.
- **`/checklist.html` — Guided checklist:** one photo per 5S standard, AI scores 0-5, summary.

## Save results to a Google Sheet

1. Create a Google Sheet at https://sheets.new
2. **Extensions → Apps Script**, paste the `SheetSaver.gs` code, save.
3. **Deploy → New deployment → Web app** → Execute as **Me**, access **Anyone**.
   Copy the Web app URL (ends with `/exec`).
4. Open the app → **Google Sheet settings** → paste the URL.

Finished audits are appended automatically (tab **Audits**), and each finding is
logged (tab **Findings**). You can also tap **Save to Google Sheet** on the report.

## Gemini API key

Built into this build so it works on phones immediately. To use a different key,
open **AI key settings** in the app and paste a new one (stored in that browser only).
