# AGENTS.md — jonathanmccallum-ar (Arabic (Modern Standard) mirror of jonathanmccallum.com)

Arabic (Modern Standard) mirror site. Same theme and design as the main site (Paper Light),
content translated into Arabic (Modern Standard), meaning-first. Repo: streamjonathan/jonathanmccallum-ar.
Live (when approved): ar.jonathanmccallum.com. Proof: jonathanmccallum-ar.pages.dev.

## Mission

Mirror jonathanmccallum.com in Arabic (Modern Standard) — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Arabic (Modern Standard) site goes live on ar.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Lewis quotations: use the published Arabic (Modern Standard) translation where one exists
  (cite it); otherwise translate fresh and mark it "translated for this site".
- Bible verses: use the Arabic Van Dyke (public domain) wording, never
  re-translate from the English article.
- Names (never vary): يسوع, الله, أسلان, نارنيا, ديغوري, بولي, جاديس, سي. إس. لويس. Book titles use the standard published Arabic (Modern Standard) titles.
- Voice: Plain Modern Standard Arabic, short sentences, warm and direct.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
