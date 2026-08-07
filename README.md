# One Page Tools

Small, self-contained browser tools. Each tool is a **single HTML file** with no build step, no
server and no database — open it and it works.

## Tools

| Tool | What it does |
|---|---|
| [Nomination Document Builder](nomination-tool.html) | Prepares a direction to transfer land to a nominee, and exports it as a formatted `.docx` or `.pdf` with signing blocks. |

## Using them

**Hosted:** open the published site and pick a tool. (Link is in the repo's *About* section once
GitHub Pages is enabled.)

**Locally:** clone the repo, or download the single HTML file, and double-click it. Both work the
same — the tools are just files.

**Offline:** open a tool and press `Ctrl+S` to save the page. Note that the export libraries load
from a CDN on first use, so save the page *after* it has loaded once, and the browser will keep them.

## Your data stays on your machine

There is no backend. Nothing typed into a tool leaves the browser: documents are generated
client-side and downloaded straight to your computer, and drafts are saved as `.json` files
wherever you choose to put them.

Because of that, **client data must never be committed to this repo.** `.gitignore` already
excludes `*.json`, `*.docx`, `*.doc` and `*.pdf` for exactly this reason — if you need to commit a
sample file, rename it or add a deliberate exception, and check it holds no real matter details.

## Adding a tool

1. Drop a new self-contained `.html` file in the repo root.
2. Add a card for it in `index.html` and a row in the table above.
3. Commit and push — GitHub Pages redeploys automatically.

Keep each tool to one file so it can be shared, emailed or saved on its own.

## Nomination Document Builder — notes

- **Parties** — vendors, purchasers and nominees are each a list, and every party independently
  picks its type: individual, company, trust with a corporate trustee, or trust with individual
  trustees. Lists can mix types freely.
- **Wording** adapts to the data: `I,` versus `We,`, singular versus plural capacities
  (`as Director of` / `as Directors of`, `as Trustee of` / `as Trustees of`), and addresses shared
  by several people are collapsed into one phrase.
- **Output** is A4, Arial 11pt, in both the `.docx` and the `.pdf`. The PDF is real text, not an
  image, so it stays searchable and selectable.
- **Signing space** above each signature rule is adjustable (Compact through Wide) for e-signature
  platforms such as DocuSign.
- **Samples** — the *Load sample…* menu fills the form with fictional data covering the common
  structures, useful for checking how a structure reads before entering a real matter.

The generated wording is a starting point, not legal advice — always review a document before it
goes out.
