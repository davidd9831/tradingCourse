# Day Trading From Zero

A static, no-build course website. 15 modules, 71 lessons, quizzes, assignments, calculators, glossary and final exam.
Progress is saved in each visitor's own browser (localStorage). There is no server, database or tracking.

## Files
- `index.html` : page shell and metadata
- `style.css`  : all styling (light and dark themes follow the visitor's system setting)
- `app.js`     : the course engine, all lesson content, glossary and sources
- `.nojekyll`  : tells GitHub Pages to serve the files as-is

## Deploy on GitHub Pages
1. Create a new repository on GitHub (for example `day-trading-course`). Public repos work on the free plan.
2. Upload all files in this folder to the repository root (drag and drop them on the repo page, including `.nojekyll`).
3. Go to Settings > Pages. Under "Build and deployment", choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/day-trading-course/`.

For a custom domain, add it under Settings > Pages and create the DNS records GitHub lists.

## Test locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.

## Editing content
Lesson text lives in `app.js` as JavaScript objects (`MODULES.push({...})`), one block per module. Each lesson is `{t: title, m: minutes, h: html}`. Quizzes are `{q, o:[options], a:index of correct answer, e:explanation}`. The glossary and sources are the `GLOSSARY` and `SOURCES` arrays. Use backticks for lesson HTML and avoid writing `${` inside them.

## Before you sell or promote this
- This is educational material, not financial, tax or legal advice. Keep the disclaimers.
- Rules change (margin rules, tax rules). Re-verify the regulatory lessons against the linked sources on the Sources page before publishing, and periodically after.
- Have a securities or advertising lawyer review your marketing, earnings claims and any results you show. See Module 13.
- Your own name, contact details and privacy or terms pages are not included. Add them if you collect emails or take payments.
