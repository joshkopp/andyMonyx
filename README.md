# Monyx marketing site

A static, multi-page site for **Monyx**, a beginner-friendly anti-scam wallet demoed on Solana devnet. There is no build step. It is plain HTML, CSS, and JavaScript, so it works if you open the files locally or host them on [GitHub Pages](https://docs.github.com/en/pages).

The live wallet itself is at [monyx.pro](https://monyx.pro/). This repo is only the marketing site.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | Home |
| `features.html` | What the wallet does today, plus a marked "more features coming" block |
| `how-it-works.html` | Four short steps |
| `safety.html` | How the risk check works, what High / Medium / Normal mean, and the disclaimer |
| `about.html` | Origin story and founders (Josh Koppanalil and Andrew Hu). Some bios are still placeholders. |
| `faq.html` | Beginner questions, as an accordion |
| `login.html`, `signup.html` | Visual mockups only. They do not submit or collect data. The real app is at monyx.pro/#login. |
| `404.html` | Friendly "page not found." GitHub Pages uses this automatically. |
| `assets/styles.css` | Shared design: pastel green `#CEE4C3`, deep green `#1f3d2b`, rounded pills and cards |
| `assets/main.js` | Shared nav, mobile menu, scroll reveals, liquid motion, FAQ, and form guard |
| `assets/wallet.png` | Screenshot used in the home hero |
| `screens/` | Desktop screenshots of home, features, and about |

Links between pages are **relative** (`features.html`, `assets/styles.css`), so the same files work from a folder on your computer and from a GitHub Pages project site (for example `https://username.github.io/monyx-site/`).

## Preview on your computer

Option A — just open `index.html` in a browser.

Option B — a tiny local server, useful if you want to confirm links:

```bash
cd monyx-site
python3 -m http.server 8080
```

Then visit `http://localhost:8080/`.

## Upload to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Add these files to the repo. Keep the folder shape: HTML in the root, CSS and JS in `assets/`.
3. Push to GitHub.
4. In the repo, open **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
6. Choose your default branch (often `main`) and the folder **/ (root)**. Save.
7. After a minute or two, GitHub will show the public URL.

If the site will live at a subpath such as `https://username.github.io/repo-name/`, relative links already cover that. Do not change them to start with `/`, or the browser will look at the domain root and miss the repo folder.

`404.html` in the root is enough for unknown paths on GitHub Pages. You do not need extra config for that.

## A few notes

- Risk labels are High, Medium, or Normal. They are informational, not legal or financial advice. The demo is devnet only.
- Do not put API keys, RPC URLs, or other secrets in this site. It is static and public.
- Founder bios and the origin story include `<!-- PLACEHOLDER -->` comments where the real copy should go later. Features that are still being discussed live under `<!-- FEATURE PLACEHOLDER -->` on the features page.
