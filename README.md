# ClipForge — AI-assisted clipping MVP

## Features
- Local video upload and preview
- Manual trim start/end controls
- 9:16, 1:1, and 16:9 canvas formats
- Custom caption overlay
- Browser WebM export (real-time; browser support varies)
- Transcript-based highlight suggestion cards
- User prompt for topic/clip goal
- Heuristic highlight scores and editable clip selection
- Responsive landing page and editor

## Honest AI status
The highlight finder does **not** call a real AI model. It scores pasted transcript segments using transparent keyword, punctuation, length, number, and user-topic heuristics. It can help shortlist transcript moments but does not truly understand semantics or predict virality. It cannot transcribe audio/video automatically. True automatic clipping requires a transcription model (e.g. Whisper), a semantic model for ranking, and a robust video rendering pipeline (e.g. FFmpeg), either locally or on a backend. A public server with AI/GPU processing may not stay within a free tier.

## Run locally
1. Extract this ZIP.
2. Open `index.html` in a recent browser, or serve the folder with:
   `python -m http.server 8000`
3. Visit `http://localhost:8000`.
4. Upload a video, paste its transcript into AI Clip Finder, click **Find highlights**, select a suggestion, adjust the cut, then export.

## Publish free with GitHub Pages
1. Create a GitHub account and a public repository named `clipforge`.
2. Upload `index.html`, `style.css`, and `app.js` to the repository root.
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch**, branch `main`, folder `/(root)`, and save.
5. Wait for the public URL to appear in Pages settings.

This is a static site and does not need an API key. Repository source is public. Check the host's current terms/limits.

## Before charging users
- Add a privacy policy, terms, contact/support, and copyright/takedown process.
- Do not market heuristic ranking as genuine AI or guaranteed virality.
- Add upload limits and abuse protection if you later accept server-side uploads.
- Add authentication, secure storage, payment integration, and server-side jobs only when justified by demand.
- Make sure users have rights to videos they process.
