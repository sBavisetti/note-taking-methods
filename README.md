# Note-Taking Methods — 10 Formats, One Topic

> Ten note-taking strategies demonstrated on a single subject — **Large Language Models** — so you can compare formats side by side and pick what works for how you think.

---

## What This Is

This is a collection of **10 standalone HTML notes**, each covering a different aspect of Large Language Models while demonstrating a different note-taking strategy. Open `index.html` in any browser — no build step, no dependencies, no server required.

Each page is fully self-contained, has a **light/dark theme toggle**, and follows the same design system (sky-blue accent, Inter + JetBrains Mono typography).

---

## The 10 Methods

| # | Method | LLM Topic | What Makes It Distinct |
|---|--------|-----------|------------------------|
| 01 | **Cornell** | Core Architecture | Cue column + notes + summary; built-in self-quiz blur mode |
| 02 | **Outline** | Training Pipeline | 4-level Roman-numeral hierarchy from data prep to deployment |
| 03 | **Mind Map** | The LLM Ecosystem | SVG radial diagram — 8 branches around a central LLM hub |
| 04 | **Charting** | Model Comparison | Side-by-side table: GPT-4o · Claude · Gemini · Llama · Mistral |
| 05 | **Sentence** | Key Facts & Timeline | 40 numbered one-idea-per-line facts across 5 topic groups |
| 06 | **Boxing** | Applications by Domain | Card-grid boxes grouped by domain (dev, healthcare, research…) |
| 07 | **Zettelkasten** | Core Concepts Network | 15 atomic cards (Z-001–Z-015) with clickable cross-links |
| 08 | **Flow Notes** | Inference Process | SVG flow diagram: prompt → tokenizer → transformer → output |
| 09 | **SQ3R** | Prompt Engineering | Survey · Question · Read · Recite · Review — all 5 stages filled |
| 10 | **Bullet Journal** | Building with LLMs | Dev log with symbols (• ○ — ✦ ✕) across a sprint week |

---

## Usage

```
git clone https://github.com/sBavisetti/note-taking-methods.git
cd note-taking-methods
# open index.html in your browser
```

No npm, no build, no server. All fonts are loaded from Google Fonts (requires internet for first load; falls back to system fonts offline).

---

## Design System

All pages share the same design tokens, mirrored from a personal website:

| Token | Light | Dark |
|-------|-------|------|
| Background | `#fafaf7` | `#0a0a0b` |
| Surface | `#ffffff` | `#131316` |
| Accent | `#0ea5e9` | `#38bdf8` |
| Text | `#18181b` | `#f4f4f5` |
| Muted | `#52525b` | `#a1a1aa` |

**Fonts:** [Inter](https://fonts.google.com/specimen/Inter) for prose · [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) for labels, badges, code

**Card pattern:** `border-radius: 0.75rem` · `border-top: 2px solid accent` · editorial em-dash list bullets

---

## File Structure

```
note-taking-methods/
├── index.html                  ← start here
├── llm-01-cornell.html
├── llm-02-outline.html
├── llm-03-mindmap.html
├── llm-04-charting.html
├── llm-05-sentence.html
├── llm-06-boxing.html
├── llm-07-zettelkasten.html
├── llm-08-flownotes.html
├── llm-09-sq3r.html
├── llm-10-bulletjournal.html
└── llm-cornell-notes.html      ← the original note this collection grew from
```

---

## Features

- **Zero dependencies** — pure HTML + CSS + vanilla JS
- **Light / dark theme** — per-page toggle, defaults to dark
- **Fully responsive** — readable on mobile and desktop
- **Self-quiz mode** (Cornell page) — blur notes or summary, hover to reveal
- **Clickable cross-links** (Zettelkasten page) — clicking a `Z-ref` scrolls to the linked card
- **Interactive SVG diagrams** — mind map and flow notes with hover states and theme-aware colours

---

## Why 10 Methods?

Each note-taking format has different strengths for different types of learners and material:

- **Cornell / SQ3R** — structured review and retention
- **Outline** — logical hierarchy and process flows  
- **Mind Map / Flow Notes** — visual thinkers and relationship-heavy topics
- **Charting / Sentence** — fact-dense comparison and rapid capture
- **Boxing / Zettelkasten** — chunked knowledge and long-term synthesis
- **Bullet Journal** — practical, mixed tasks-and-notes workflow

Using LLMs as the shared topic lets you see the *same information* presented in radically different ways — useful both as an LLM reference and as a demonstration of how format shapes comprehension.

---

## License

MIT — use freely, adapt for your own topics.
