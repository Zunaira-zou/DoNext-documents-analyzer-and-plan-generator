# DoNext
**Live Demo:** https://zunaira-zou.github.io/DoNext-documents-analyzer-and-plan-generator/

**AI Administrative Assistant**

> Don’t just understand the document. Know what to do next.

DoNext turns complicated administrative documents — scholarship announcements, university notices, internship applications, admission guidelines, government notifications, and official forms — into clear, personalized action plans with deadlines, checklists, and reminders.


## Problem

Students and professionals regularly receive dense, poorly structured administrative documents. Extracting eligibility criteria, deadlines, required documents, and next steps is time-consuming and error-prone. Missing a single requirement or deadline can cost an opportunity.

## Solution

Upload or paste any administrative document. DoNext analyzes it and produces:

- A concise, action-oriented summary
- A prioritized to-do list with status tracking
- A required-documents checklist
- Detected application portals and deadlines
- An “What am I missing?” view
- A document-grounded AI chat for follow-up questions

The system clearly separates **information taken from the document** from **AI suggestions**, so users can verify critical details.

---

## Features

| Feature | Description |
|---------|-------------|
| **Document Intake** | Upload text files or paste content. PDF and image uploads are accepted with guidance for best results. |
| **Structured Extraction** | Identifies purpose, eligibility, deadlines, required documents, actions, fees, warnings, and application URLs. |
| **Action Plan** | Converts requirements into a trackable to-do list (Not started → In progress → Completed). |
| **Document Checklist** | Mark required documents as Ready or Missing. |
| **Deadline Tracking** | Color-coded urgency indicators and sorted upcoming deadlines. |
| **Online Application Detection** | Extracts portal links and provides an “Open Application” button (never auto-submits forms). |
| **What Am I Missing?** | Prioritized view of incomplete tasks and documents. |
| **Ask AI** | Chat interface grounded in the uploaded document. Distinguishes source facts from AI interpretation. |
| **Dashboard** | Overview of active applications, progress, deadlines, tasks, and notifications. |
| **Persistence** | Data stored in `localStorage` so work survives page refreshes. |
| **Trust Layer** | Explicit labeling of document-sourced information vs. AI-generated suggestions. |

---

## Quick Start

### Option A — Single-file (easiest)

1. Open `index-standalone.html`
2. Double-click the file (or open it in any modern browser)
3. Internet connection is required the first time (loads React, Tailwind, and icons via CDN)

### Option B — Local server

```bash
# Using Python
python -m http.server 8080

# Or using Node.js
npx serve -p 8080
```

Then open [http://localhost:8080](http://localhost:8080).

---

## Demo Walkthrough

1. Click **New**
2. Click **Load sample scholarship announcement** (or paste your own document)
3. Click **Analyze & Create Action Plan**
4. Review the generated summary, to-do list, and document checklist
5. Mark tasks complete and documents as ready
6. Explore **Missing** and **Ask AI**
7. Return to the **Dashboard** for a multi-application overview

---

## Tech Stack

- **React 18** (CDN)
- **Babel Standalone** (in-browser JSX)
- **Tailwind CSS** (CDN)
- **Font Awesome**
- **localStorage** for client-side persistence

No build step or package manager is required for the current demo.

---

## Project Structure

```
donext/
├── index-standalone.html   # Recommended single-file version
├── index.html              # Entry that loads app.jsx
├── app.jsx                 # Application logic and UI
└── README.md
```

---

## Roadmap

**Near-term**
- [ ] Real LLM integration with structured output
- [ ] PDF text extraction (PDF.js)
- [ ] Basic OCR for scanned documents
- [ ] Improved date and eligibility parsing

**Later**
- [ ] User accounts and cloud sync
- [ ] Email / push / calendar reminders
- [ ] Attachment of supporting files to document requirements
- [ ] Multi-language support
- [ ] Export to calendar / Notion / task managers

---

## Design Principles

1. **Action over summary** — The primary output is a clear list of next steps, not a long paraphrase.
2. **Source transparency** — Users should always know what came from the document versus what was inferred.
3. **No silent automation** — The app never submits forms or takes irreversible actions on the user’s behalf.
4. **Progressive disclosure** — Complex information is organized into focused views (summary, tasks, documents, deadlines, chat).

---

## License

MIT

---

Built as a demonstration of turning administrative complexity into manageable next steps.
