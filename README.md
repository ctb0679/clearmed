# ClearMED

ClearMED is an AI assistant that turns your doctor’s notes into plain language. You upload a photo or PDF of a note, and it gives you a simple checklist, a short summary, and—if you like—an audio version you can listen to. You can also chat with it and ask questions, optionally about a scan you just did.

## What it does

- *Scan* — Snap or upload a doctor’s note. ClearMED sends it through an n8n workflow that pulls out diagnoses, MEDications, and things to watch for, then gives you a patient-friendly checklist and summary.
- *Results* — See your checklist, summary, and whether everything looks consistent (“Verified Safe” or “Needs Review”). You can play an audio summary too.
- *Chat* — Ask questions in your own words. If you’ve just run a scan, you can ask about that report and get answers in context.

## What we built it with

| Area | Tool |
|------|------|
| App | [Next.js](https://nextjs.org) (App Router), [React](https://react.dev) |
| Styling | [Tailwind CSS](https://tailwindcss.com) |
| Automation | [n8n](https://n8n.io) — workflow handles OCR, drafting, a safety check, and optional TTS |
| AI | OpenAI (in n8n and in the chat) |
| Audio | ElevenLabs (in n8n, optional) |

More on the workflow and how to set it up: [n8n/README.md](n8n/README.md).

## Get it running

bash
npm install
npm run dev


Then open [http://localhost:3000](http://localhost:3000).

Copy [.env.example](.env.example) to .env.local and fill in your n8n webhook URL (or base URL + API key + workflow ID) so scans can hit your workflow.
