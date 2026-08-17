# Alpha Scouts — The Independence Expedition

Slideshow site for the Alpha East Bay workshop. Static, no build step, one HTML file.

## Deploy

**Vercel**
1. Push this folder to a GitHub repo.
2. In Vercel: *Add New → Project* → import the repo.
3. Framework preset **Other**, build command **empty**, output directory **`.`**
4. Deploy.

**Or from the CLI**
```bash
npm i -g vercel
vercel --prod
```

**Locally**
```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
Open it over HTTP, not as a `file://` path — speech synthesis needs a real origin.

## Files
| File | What it is |
|---|---|
| `index.html` | The whole site: content, styles, script |
| `favicon.svg` | Trail blaze mark |
| `vercel.json` | Clean URLs + security headers |
| `.gitignore` | Standard ignores |

## Using it in the room
- **Present mode** (top right) goes full screen for projecting. `Esc` exits.
- **Arrow keys** move between pages; swipe left/right on a tablet.
- Every page has its own link — `#s6-do` opens Session 6 directly.
- **Printables** live under *All printables*. Each sheet prints from its own page, in a new window.
- If a print window doesn't open, allow pop-ups for the site and tap the button again.

## Read-aloud voices — set this up before Session 1

Two of the four scouts need reading support. The default voice on most devices is the
worst one installed, so install a natural voice and pick it in the sidebar.

**Windows** — Settings → Time & Language → Speech → Manage voices → Add voices.
Install a *Natural* voice (named like "Microsoft Aria Natural"). Restart the browser.

**Mac / iPad** — System Settings → Accessibility → Spoken Content → System Voice →
Manage Voices. Download an *Enhanced* or *Premium* English voice — Ava, Zoe or Evan.
Restart the browser.

**Chromebook** — Settings → Accessibility → Text-to-Speech → Speech settings →
*Enhanced network voices*. Turn on and pick one. Needs the Chromebook to be online.

Then: sidebar → **Read-aloud voice** → choose → **Test this voice**. The picker ranks
the device's voices and pre-selects the best one it finds.

> **Guides: do not read aloud what a scout could tap.** Every block *and* every single
> step has its own Hear it button. Point at the button, not at the words. Reading it for
> them is the same shape of mistake as telling them the way.

## Notes
- No `localStorage` or `sessionStorage`. Voice choice lasts for the session only.
- Fonts load from Google Fonts; the site falls back to system faces offline.
