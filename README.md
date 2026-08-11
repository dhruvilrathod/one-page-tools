# One Page Tools

Small, self-contained browser tools. Each tool is a **single HTML file** with no build step, no
server and no database — open it and it works.

## Tools

| Tool | What it does |
|---|---|
| [Nomination Document Builder](nomination-tool.html) | Prepares a direction to transfer land to a nominee, and exports it as a formatted `.docx` or `.pdf` with signing blocks. |
| [Never Sold or Occupied Declaration](never-sold-tool.html) | Prepares the vendor's confirmation that a home is brand new and has never been leased, sold or occupied. |

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

## Never Sold or Occupied Declaration — notes

- **Vendors** use the same party model as the nomination tool: a list where each party is an
  individual, a company, or a trust with a corporate or individual trustee. This document names no
  addresses, so parties carry none.
- **Confirmations** are an editable numbered list, defaulting to the brand-new-home and
  never-leased-or-occupied wording.
- **Signatures** print two across the page by default, or one per line, with the position in
  brackets under each rule.

## Shared conventions

Both tools follow the same rules, so anything you learn in one carries over:

- A4, Arial 11pt, in the `.docx` and the `.pdf` alike; the PDF is real text, not an image.
- Adjustable signing space for e-signature platforms.
- Drafts save as `.json` to a folder you pick; a draft only loads into the tool that wrote it.
- Downloads are named plainly (`Nomination`, `Declaration`) with no client details in the filename.
- Blank fields print as a rule rather than sample text, so an incomplete draft still previews.

The generated wording is a starting point, not legal advice — always review a document before it
goes out.
