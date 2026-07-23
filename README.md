# Roy Ricaldi — Personal Research Site

A single-page site for GitHub Pages. No build step, no Jekyll, no dependencies to install — just HTML, CSS, and a few lines of JS. Open `index.html` in a browser and it works; push the folder to GitHub and it's live.

**Design:** modern and minimal — white and warm-gray tones only, no color accent anywhere. Headings are set in Newsreader (serif), everything else in Inter, both loaded from Google Fonts.

## Files

- `index.html` — all page content and structure
- `style.css` — all styling (design tokens/colors/fonts are declared at the top)
- `script.js` — mobile menu toggle, nothing else
- `images/` — you'll create this when you add your photo (see below)

## How the content is organized, and why

| Section | Purpose |
|---|---|
| **Hero** | Name, title, one-line pitch, affiliations, and links (email, LinkedIn, Scholar, ResearchGate) up front. |
| **About Me** | The placeholder you asked for — a short, human paragraph in your own words. |
| **Research** | Your thesis framing plus your stated research interests as scannable tags. |
| **Publications** | All nine outputs, newest first, linked to a real public version wherever one exists, plus a pointer to your full Google Scholar profile for the complete record. |
| **Teaching & Supervision** | Your two TA roles, the IST-seminar-to-thesis pathway, and your supervision record with a placeholder next to each student for what they worked on. |
| **Let's Work Together** | Two calls to action, kept separate: one for researchers/practitioners, one for TU/e students. |
| **Footer** | Email, LinkedIn, Scholar, ResearchGate, location. |

## About the publications list — please read

Google Scholar blocks automated access (its robots.txt disallows it), so I couldn't scrape your profile directly. Instead I cross-checked your CV against **DBLP**, the standard computer-science bibliography, which gave me verified titles, full author lists, and working links for five of the nine entries. Three things came out of that worth knowing:

- **Two titles changed.** Your CV lists *"TeleHunt: A Framework and Tool for **AI-Powered CTI Hunting** on Telegram"* and *"Topical Shifts in the Dark Web: A Longitudinal Analysis of **the** Cybercrime Ecosystem."* The versions actually posted to arXiv are titled *"...for **Efficient Cybercriminal Community Discovery** on Telegram"* and *"...Analysis of **Content from** the Cybercrime Ecosystem."* I used the arXiv titles since they're what a reader will actually find. Worth updating your CV to match, or telling me if the CV title is the one you actually want shown.
- **"Where is Dmitry going?"** lists Luca Allodi as first author, with you second — I kept that order since it's how it's actually published.
- **Four entries have no confirmed public link**: *DMITRY* (still in prep), *Sustainable Cybersecurity*, *Analyzing Publications for Information Leakage in arXiv*, and *Generative Adversarial Networks for Digital Forensics*. These predate or fall outside what DBLP indexes. I left them as plain text rather than guess a URL — if you have direct links for any of them, send them over and I'll wire them in.
- As a bonus from the same search: **Jai Wientjes, Yasen Yalamov, and Victor Asanache are co-authors with you on specific papers** (the "Where is Dmitry going?", "An Experimental Design...", and "TeleHunt" papers respectively) — that might be exactly the project to reference for their entries below.

## Before you publish — a short checklist

1. **About Me** — search `index.html` for `[EDIT: ABOUT ME]` and replace the placeholder paragraph with a few sentences in your own words.
2. **Student projects** — search for `[EDIT: PROJECT]`, eight in total, one per supervised student. Replace each with a line on what they worked on.
3. **Photo** — add a photo (roughly square or slightly portrait, at least 360×430px) as `images/profile.jpg`, then find `[EDIT: PHOTO]` in `index.html` and replace the placeholder monogram block with:
   ```html
   <img src="images/profile.jpg" alt="Roy Ricaldi">
   ```
4. **"Security Group" vs. "Threat Analysis Group"** — your LinkedIn summary says Threat Analysis Group, your LinkedIn experience section says Security Group. I used "Security Group" in the hero (marked `[EDIT: GROUP NAME]`); confirm which is currently accurate.
5. **Phone number** — left off the public site on purpose (most academic pages skip a personal mobile to avoid spam); only email is listed. Add it back into the footer if you'd rather it be public.
6. **Email address** — every contact link points to your TU/e address (`r.j.ricaldi.saavedra@tue.nl`). Swap in your Gmail throughout if you'd prefer that instead.
7. **Full CV (optional)** — if you want a downloadable PDF, drop it in as `files/Roy_Ricaldi_CV.pdf` and add a "Download CV" link, e.g. in the footer next to LinkedIn.

## Publishing to GitHub Pages

1. Create a new **public** GitHub repository. Name it exactly `<your-username>.github.io` if you want the site at `https://<your-username>.github.io`; any other name works too, it'll just live at `https://<your-username>.github.io/<repo-name>/`.
2. Add these files to the repo. Easiest path if you're not using git day-to-day: on the repo's GitHub page, click **Add file → Upload files**, and drag in `index.html`, `style.css`, `script.js`, and your `images/` folder. Or, from the command line:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages** → under "Build and deployment," set **Source** to "Deploy from a branch," pick the `main` branch and `/ (root)` folder → **Save**.
4. GitHub Pages gives you a live URL within a minute or two, shown on that same Pages settings screen.

## Making changes later

No build step. Edit `index.html` or `style.css` directly, commit, push — GitHub Pages redeploys automatically, usually within a minute.
