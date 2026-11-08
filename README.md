# Unprompted — Speaking & Communication Practice

A local-first speaking practice application built with React, TypeScript, Vite and Tailwind CSS. The interface follows the supplied mobile UI references: editorial serif headings, dark surfaces, rounded panels, compact navigation and a vivid accent. The default theme is purple on black; a light theme is available from the top bar.

## Included

- 100,000 generated speaking prompts: 50,000 off-the-cuff prompts and 50,000 prepared/deep-research prompts. The prompt library combines a curated subject taxonomy (including personalities, everyday topics, academic concepts and practical situations), multiple perspectives and prompt structures. Search and category filters are available.
- Practice modes: off the cuff, deep research/prepared, extended speaking and Q&A drill.
- Personal Q&A bank: add and remove your own prompts; saved in local storage.
- Free exercise formats: Explain Anything, Argue Both Sides, Storytelling Studio, Summarization Challenge, Vocabulary in Action, Interview Simulator, Presentation Practice and Meeting Simulator.
- Speaking frameworks, adjustable countdown timer, optional microphone recording and waveform level display.
- Lifetime practice-time counter: accumulates actual seconds while the practice timer is running, independent of microphone recording and saved audio. Deleting recordings does not reduce this counter. It is stored separately in local storage.
- Debate practice, self-assessment, reflection notes, progress view and local recording library.
- IndexedDB for audio recordings; recordings are not uploaded.

## Run locally

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
npm run preview
```

Vercel settings:
- Framework preset: Vite
- Build command: `npm run build`
- Output directory: `dist`

`vercel.json` includes an SPA fallback rewrite.

## Free / browser-only behaviour

The core application requires no login, paid API, hosted database or subscription. Recording requires microphone permission and a secure context (HTTPS or localhost). Actual recording MIME types depend on the browser. The app exports the browser's genuine recorded format; it never renames WebM/Opus to M4A. Browser storage can be cleared by the user or evicted by the browser, so export important recordings for backup.

The lifetime timer metric counts elapsed whole seconds while the in-app timer is running. It is independent of recording storage and is not decremented when audio is deleted. It is device/browser-local and can be reset if browser site data is cleared.
