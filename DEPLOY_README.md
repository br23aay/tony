# Deploying Tony to the cloud (phone access anywhere) — free

This puts Tony online 24/7 so you can open it from your phone at work or out and about,
running on your Claude / Grok / Groq / Gemini brain. It does NOT include the local Ollama
models, your indexed documents, or browser control — those stay on your laptop version.

---

## What the cloud version has vs. doesn't

INCLUDED (works in the cloud):
- Chat with cloud brains: Claude, Grok, Groq, Gemini (whichever keys you set)
- Live web search with sources
- Agent mode (web / python / read-webpage tools)
- The daily job-hunt shortlist
- Natural neural voice (edge-tts)

NOT included on a free host (needs your laptop):
- Local Ollama models (free hosts have no GPU / not enough RAM)
- Your private document brain (RAG) — those files live on your laptop
- Playwright browser control

So: laptop = full private Tony. Cloud = lighter Tony you can reach anywhere.

---

## Deploy on Render (free)

1. Put these files in a folder and push to a GitHub repo:
   - tony_server.py
   - tony.html
   - requirements.txt
   - Procfile

2. Go to https://render.com → sign up (free) → New → Web Service → connect your repo.

3. Settings:
   - Runtime: Python 3
   - Build command:  pip install -r requirements.txt
   - Start command:  python tony_server.py
   - Instance type:  Free

4. Add your API keys under "Environment" (the same names as on your laptop):
   - ANTHROPIC_API_KEY = your Claude key
   - XAI_API_KEY       = your Grok key
   - GROQ_API_KEY      = your Groq key   (optional)
   - GEMINI_API_KEY    = your Gemini key (optional)

5. Click Create. After it builds, Render gives you a URL like
   https://tony-xxxx.onrender.com  — open that on your phone. Bookmark it / add to home screen.

---

## Honest notes

- FREE TIER SLEEPS: after ~15 min idle, the first request takes ~30–60s to wake. Normal after that.
- Keys live as environment variables on Render — never put keys in the code or the repo.
- This is a personal-use setup on Flask's built-in server; fine for just you, not a public product.
- Pick a cloud brain in the dropdown (claude / grok / groq / gemini). Local "ollama" models
  won't appear in the cloud — that's expected.

---

## Railway / Hugging Face Spaces
Both also work on free tiers with the same files. Render is the simplest to start with.
