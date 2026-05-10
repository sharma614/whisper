# 🎙️ Whisper — Voice Note Summariser

A beautifully minimal, single-file voice note app that records your speech, transcribes it in the browser, and uses **Groq AI** (Llama 3.3 70B) to distil it into a clear summary.

**100% Free. No build step. No frameworks. Zero dependencies.**  
Drop `index.html` anywhere and it works.

---

## Features

- 🎤 **Voice recording** via the browser's built-in Web Speech API (no external STT service)
- 〰️ **Animated waveform** while recording
- 🤖 **AI summarisation** powered by [Groq](https://groq.com) (`llama-3.3-70b-versatile`) — **free tier, thousands of requests/day**
- 📋 **Structured summary** — one-line gist, key bullet points, mood/tone tags, and a next action step
- 📋 **One-click copy** of the full summary
- 💾 **History** — last 5 notes saved to `localStorage`
- 🔑 **API key** stored locally in `localStorage`, never sent anywhere except Groq's API
- 🎨 **Soothing UI** — dark background, soft blue accents, Lora + Inter fonts, fade-in animations

---

## Quick Start

1. Open `index.html` in **Chrome** or **Edge** (Chromium-based browser required for Web Speech API)
2. Get a **free** API key from [Groq Console](https://console.groq.com/keys) (no credit card required)
3. Paste your Groq API key (starts with `gsk_`) and click **Save**
4. Tap the **mic button** and speak
5. Tap again to stop, then click **✦ Summarise**

---

## Why Groq?

| Provider | Free Tier | Speed |
|---|---|---|
| **Groq** ✅ | ~14,400 requests/day | ⚡ Ultra-fast inference |
| Google Gemini | Limited / regional | Moderate |
| Anthropic Claude | ❌ Paid only | Moderate |

---

## Deploy

| Platform | Steps |
|---|---|
| **Netlify** | Drag the `whisper/` folder onto [app.netlify.com/drop](https://app.netlify.com/drop) |
| **GitHub Pages** | Push to a repo → Settings → Pages → Deploy from branch |
| **Local** | Just double-click `index.html` |

---

## Browser Support

| Browser | Recording | Summarisation |
|---|---|---|
| Chrome / Edge | ✅ | ✅ |
| Firefox | ❌ (no Web Speech API) | ✅ (manual transcript) |
| Safari | ⚠️ Partial | ✅ |

> **Tip:** You can always type or paste a transcript manually into the text box and still use the Summarise feature.

---

## Privacy

- Your voice is processed by the **browser's built-in speech engine** (Google's STT in Chrome).
- Only the **text transcript** is sent to Groq's API — no audio ever leaves your device.
- Your API key is stored only in your browser's `localStorage`.

---

## File Structure

```
whisper/
├── index.html   ← entire app (HTML + CSS + JS)
└── README.md
```

---

## License

MIT — free to use, modify, and deploy.
