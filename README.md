# GPTAgent Team Workflow Plan

**QC-Law25 — Sovereign App** · Gemini v1.0 · Compliance-as-a-Service

A ready-to-ship static site that summarises the conversation analysis and breaks down the requested work into role-based workflows for the GPTAgent Team. Zero dependencies — open `index.html` in any browser and it works.

---

## Features

| Feature | Details |
|---|---|
| **Conversation Analysis** | Goal, Constraints, and Output cards at a glance |
| **Role-Based Assignments** | Six colour-coded team cards (Program Lead, Product Strategist, UX Designer, Frontend Engineer, Backend Engineer, QA & Launch) |
| **Interactive Checkboxes** | Each task has a checkbox; progress bars update in real time |
| **Persistent State** | Checkbox state is saved to `localStorage` — survives page refreshes |
| **Phase Stepper** | Visual timeline connecting Phase 1 → 2 → 3 with colour-coded badges |
| **Immediate Next Steps** | Highlighted action items for kickoff |
| **Accessible** | Skip-link, ARIA roles/labels, focus styles, semantic heading hierarchy |
| **Print-Friendly** | `@media print` styles produce a clean black-and-white handoff document |
| **Open Graph Tags** | Rich link previews when shared via Slack, Teams, or social media |
| **Responsive** | Fluid grid layout works on mobile, tablet, and desktop |

---

## Quick Start

### Option 1 — Open locally
```bash
# Clone or download the repository, then:
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — GitHub Pages
1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set **Source** to `main` branch, root folder `/`.
4. Click **Save** — your site will be live at `https://<username>.github.io/<repo>/`.

### Option 3 — Netlify Drop
1. Visit [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag and drop the project folder.
3. Netlify provides an instant public URL — no account required.

### Option 4 — Any static host
Upload `index.html` to any web server, S3 bucket, Vercel, Cloudflare Pages, etc. No build step required.

---

## File Structure

```
/
└── index.html    — Complete single-file app (HTML + CSS + JS, no dependencies)
└── README.md     — This file
```

---

## Customisation

All content and styles live in `index.html`:

- **Role colours** — edit the CSS custom properties under `/* Role colours */` in `:root`
- **Phase colours** — edit `--phase-1`, `--phase-2`, `--phase-3`
- **Tasks** — add or remove `<li>` items inside any `.task-list`; the progress bar auto-adjusts
- **localStorage key prefix** — change `STORAGE_PREFIX` in the `<script>` block if you need to isolate state per environment

---

## Team

| Role | Responsibility |
|---|---|
| Program Lead 🧭 | Scope, timeline, stakeholder approvals |
| Product Strategist 📋 | User stories, MVP definition, acceptance criteria |
| UX Designer 🎨 | Information architecture, wireframes, accessibility |
| Frontend Engineer 💻 | Responsive UI, component integration, build artifacts |
| Backend Engineer ⚙️ | Data model, APIs, conversation ingestion |
| QA & Launch ✅ | Content validation, usability checks, release sign-off |

---

*Prepared for the GPTAgent Team · Ready for stakeholder review*
