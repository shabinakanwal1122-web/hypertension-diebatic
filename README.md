# HypoDiabetic Monitor

## Easiest setup (no GitHub, no server, free)
1. Go to app.netlify.com/drop and drop this ZIP file (or the unzipped folder).
2. Open the https link Netlify gives you, on your phone.
3. Get a free Google Gemini key: aistudio.google.com/apikey -> sign in -> Create API key -> copy.
4. In the app: Readings tab -> "AI for photo scans" -> paste the key -> Save and test.
5. Done. Meal photo scan, label scan and typed meals use the AI. The key stays on that phone.

Each phone that uses the app needs its own key (or use the server option below).

## Optional: shared server key (for many users)
Deploy from GitHub (drag-and-drop does not run the server function), then in Netlify:
Site configuration -> Environment variables -> ANTHROPIC_API_KEY = your Claude key -> Trigger deploy.
Phones without their own key then use the server.

## Files
- index.html: the app
- privacy.html: privacy policy (replace [YOUR CONTACT EMAIL])
- manifest.webmanifest, sw.js, icons/: installable app (PWA)
- netlify/functions/analyze.mjs, netlify.toml: optional server for the shared key
