# S&C UK&I — Strategy & Consulting Onboarding

An internal onboarding microsite for new joiners to Slalom UK&I Strategy & Consulting.
Static HTML — no build step, no dependencies, no server-side code.

> **Internal use only.** Contains named team members, client case studies, and internal
> tool links. Host behind Slalom SSO (GitHub Enterprise Pages / internal domain only).
> Do **not** publish to a public GitHub Pages site.

---

## What's here

| Path | Purpose |
|------|---------|
| `index.html` | Landing / welcome page — **entry point** |
| `who-we-are.html` | Team, structure & the GtM / Industry support org chart |
| `what-we-do.html` | Capabilities overview |
| `how-we-work.html` | Ways of working, principles, internal partnerships |
| `where-we-create-impact.html` | Client work, example projects & the CX sizzle reel |
| `case-studies.html` | Referenced client success stories |
| `who-to-know.html` | Key people & contacts |
| `what-next.html` | Next steps for new joiners |
| `assets/` | All styles, fonts, icons, images (see below) |

### `assets/`
- `site.css` — shared site styles
- `colors_and_type.css` — Slalom design tokens (colours, type scale)
- `site.js` — small progressive-enhancement script (scroll reveals, accordions)
- `fonts/` — self-hosted brand fonts (Slalom Sans, Lora, JetBrains Mono)
- `icons/` — Slalom line icons (SVG)
- `img/`, `brand/` — imagery and brand marks
- `cs/` — case-study photography + the CX video poster
- `slides/` — source slide exports used as imagery

Everything is **self-contained and works offline** — open `index.html` in any browser.
The only outbound links are normal hyperlinks (e.g. the CX video plays on slalom.com,
internal tools open in SharePoint); nothing is hot-linked or fetched at runtime.

---

## Deploying (GitHub Enterprise Pages)

1. Commit and push to the repo's default branch (`main`).
2. **Settings → Pages → Source:** Deploy from a branch → `main` / `/ (root)` → **Save**.
3. Because this is an Enterprise repo, set Pages visibility so only logged-in
   members of the organisation can view it (Settings → Pages → *Visibility*).
4. The live URL appears in the Pages settings once the deploy finishes (~1–2 min).

Any push to `main` redeploys automatically.

---

## Maintaining the content

All content is plain HTML — edit the text directly and commit. No tooling required.

**Updating people in the org chart** (`who-we-are.html`, accordion item 14 "GtM / Industry support"):
- Each industry sits in a `.org-card` block.
- The lead's name is in `.org-card__leadname`; team members are `<li>` items in the
  `.org-card__members` list below it.
- A comment at the top of that block (`<!-- EDITABLE ORG CHART ... -->`) explains the structure.
- To move someone between groups, cut their `<li>` from one card and paste it into another.

**Editing other copy:** open the relevant page, find the text, change it, commit, push.

---

## Conventions

- Sentence case throughout (Slalom brand standard).
- Slalom Blue `#0C62FB` is the primary accent; secondary accents are cyan, coral, chartreuse.
- No emoji. Icons come from `assets/icons/`.
- Keep the folder structure intact — pages reference assets by relative path.
