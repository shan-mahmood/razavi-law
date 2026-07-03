# Razavi Law Group — Employment Landing Page

Single-page, static landing page for the employment ("Who Fired You?") vertical.
No build step, no dependencies — `index.html` is fully self-contained (fonts via
Google Fonts CDN; the two photos and the RAZAVI logo are embedded inline).

## Deploy

### Option A — GitHub → Vercel (recommended)
```bash
cd razavi-lp
git init
git add .
git commit -m "Razavi employment landing page"
# using GitHub CLI:
gh repo create razavi-employment-lp --private --source=. --push
# or plain git after creating an empty repo on github.com:
# git remote add origin https://github.com/<you>/razavi-employment-lp.git
# git branch -M main && git push -u origin main
```
Then at vercel.com/new → **Import** the repo → Framework preset: **Other** →
no build command, output = repo root → **Deploy**. You get a
`*.vercel.app` preview URL to send the client for approval.

### Option B — fastest preview (drag & drop)
Go to vercel.com/new, drag this folder onto the page, Deploy. Instant URL.

## After client approval (DNS)
In Vercel: Project → Settings → Domains → add the domain. Vercel shows the exact
A / CNAME records to enter at the registrar. (This is the DNS data step.)

## Before production — still to finalize
- [ ] Replace the stand-in **"WHO FIRED YOU?"** hero mark with the official white asset
- [ ] Swap in the real brand fonts (currently Poppins / Inter / Anton / Oswald / Cinzel as stand-ins)
- [ ] Replace the 3 placeholder Google reviews with real, approved ones
- [ ] Confirm Faheem Tukhi's exact title
- [ ] Wire the form's lead payload (logged to console now) to the CRM/intake endpoint
- [ ] Confirm approved settlement figures if a results strip is added
- [ ] Bar-compliance / brand review (Kevin) before publishing
