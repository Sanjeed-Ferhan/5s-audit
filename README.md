# 5S Camera Audit

Camera + AI (Google Gemini) 5S auditing app.

**The app now runs on Google Apps Script** so that it requires Google sign-in and
only approved people can use it. This GitHub Pages site is just a landing page
with a button that opens the app.

## Where things are

- **App (use this):** the Apps Script Web App URL (`.../exec`).
- **Reports/data:** saved to the Google Sheet the Apps Script is bound to.
- **Landing:** this page (`index.html`) just links to the app.

## Setup (Apps Script app)

1. Create a Google Sheet, then **Extensions → Apps Script**.
2. Paste **`App.gs`** (from the project) as the code.
3. Add an HTML file named exactly **`AppIndex`** and paste **`AppIndex.html`**.
4. **Project Settings → Script properties → Add:** `GEMINI_API_KEY` = your key.
5. **Deploy → New deployment → Web app**:
   - Execute as: **Me**
   - Who has access: **Anyone with Google account**
   - Deploy, authorize, copy the **Web app URL** (`.../exec`).
6. Put that URL in the button in `index.html` (hosted here).

## Approving users

- The admin email (`ADMIN_EMAIL` in `App.gs`) is always allowed.
- When someone without access opens the app they tap **Request access**.
  The request is logged in the **Access Requests** tab and emailed to the admin.
- To approve: add the person's email to the **Allowed Users** tab
  (`Email | Name | Added`). They can then use the app.

## Tabs created automatically

- **Allowed Users** – who may use the app.
- **Access Requests** – pending/processed requests.
- **Audits** – one row per finished audit.
- **Findings** – one row per finding.

## Notes

- The Gemini API key and the analysis prompt live only on the server (never in
  the browser).
- Camera works because Apps Script serves over HTTPS.
