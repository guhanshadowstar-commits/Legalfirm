# Prudent Legal Services — Website

A 4-page luxury site (Home, About, Services, Appointment) built as a single
HTML file. The gold "Lady Justice" figure is fixed on screen and glides
smoothly to a new spot whenever you switch pages — that's why it's built as
one file with instant page-switching instead of 4 separate files that reload.

## Run it locally (pick one)

**Option A — just double-click**
Open `index.html` directly in your browser. Everything works except you'll
see `file://` in the address bar.

**Option B — proper local server (recommended)**
```
python3 serve.py
```
Then visit **http://localhost:8000**. This is closer to how it'll behave on
a real domain, and avoids occasional browser restrictions on local files.

If you don't have Python's `webbrowser` auto-open working, just open
http://localhost:8000 manually after running the command.

## What to customize before sending this to a client / going live

- Swap the placeholder email/phone (`info@prudentlegal.example`, `+91 00000 00000`)
  for K. Shankar's real contact details — search the file for those strings.
- The appointment form doesn't submit anywhere yet — it's a front-end demo.
  Easiest fix: connect it to an n8n workflow (Webhook → Gmail/WhatsApp), the
  same pattern you used for the PG bill system.
- All text is in plain English inside `index.html` — search for the line you
  want to change and edit directly, no build tools involved.

## Files

- `index.html` — the entire site (structure, styling, animation)
- `serve.py` — one-command local server
- `README.md` — this file
