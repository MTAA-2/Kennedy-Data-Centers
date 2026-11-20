# Overtime Justice Help — Data Center Workers Landing Page

Static GitHub Pages rebuild of https://overtimejusticehelp.com/,
converted from the client's supplied file
(`index-55dca6e9.html`, "Data Center Workers: Overtime Check
(Version A)") into our current framework format
(index-12.html / style-14.css lineage — the Massachusetts tobacco
page). HTML + CSS only, no PHP.

## Framework carried over (unchanged)

- MTAA CIPA block script in the head
- Meta Pixel **1238664640565416** + ViewContent
- MTAA form embed **nf_3270a8a1b0e4425cb70e9f97f2fa5a3c** in the
  overflow form card (hangs past the hero, scrolls internally)
- Relative footer legal links (privacy-policy.html / disclaimer.html)

## Branding converted to the sample's firm

- **Kennedy Law Firm, LLP**, 2925 Richmond Ave., Ste. 1200,
  Houston, TX 77098 — Galvin Kennedy responsible for the page
- Phone **713-425-6445** in the header and footer (the rendered
  sample displays it twice)
- Footer disclaimer is the sample's own four paragraphs, verbatim
- Verified: zero traces of the previous firm/subject
  (Bernheim Kelley, tobacco, smoking, Massachusetts, etc.)

## Palette — sampled live from the rendered page, 2026-11-20

Matches the client's file exactly:

| Surface | Color |
|---|---|
| Page / hero background | warm cream `#fffaf2` |
| Headings / ink | charcoal `#23262b` |
| CTA buttons | safety orange `#d9480f` (hover `#b33a0b`) |
| Section-heading bands | peach `#ffe3cf` |
| Cards | peach `#fff1e3`, border `#f2c49f` |
| Numbered-step circles | yellow `#ffd166` |
| Headline highlighter | yellow `#ffd166`–`#ffe381` gradient |
| Header / footer phone | rust `#b33a0b` |
| Footer | no dark block on the sample — light, on the cream page |

Headings use **Archivo** (the sample's heading face); body is Inter.
The hero is light, as on the sample — the framework's dark hero
gradient is replaced by the cream background with a light-overlay
parallax photo.

## CSS changes vs the framework

Colors and heading font-family values only, plus three small
additions the framework has no rule for (grouped in one marked
block at the end of style.css): the hero headline's second line +
yellow highlighter, the checkmark before card titles, and the
numbered yellow-circle steps. Two slot changes: the logo rule is
widened for the firm's wordmark logo (300px desktop / 200px
mobile), and the hero overlay is lightened so dark text reads over
the photo. Diff-verified.

## Placeholders — two files to drop in

1. **`KENNEDY-logo.webp`** — the firm's logo, referenced in the
   header and footer (same filename the client's file uses).
   Drop it into this folder's root.
2. **`hero-a.jpg`** — the data-center workers photo, referenced
   as the hero parallax background (same filename the client's
   file uses). Drop it into this folder's root.

The other parallax bands point at `YOUR-IMAGE-URL-HERE` (unused on
this page's sections, kept from the framework).

## Flags

- **The sample's own form is a native 5-question quiz, not an
  embed — and its endpoint is empty.** The client's file has
  `leadEndpoint: ""` and would show "Online requests are not
  connected yet" on submit. This build uses our MTAA embed
  instead, so leads flow normally. If he wants the client's five
  questions in the intake, that is a form-config job (same pattern
  as the tobacco/Heltzer multi-step configs) — the questions are
  in the supplied file.
- **The live quiz differs from the supplied file's quiz.** The
  live site's first question asks what kind of work the visitor
  did (hourly trade, laborer, operator, supervisor, salaried,
  day rate, flat weekly, contractor/1099); the file's first
  question asks whether they worked on a data center project
  (now / last 3 years / over 3 years ago / no). The "Do You
  Qualify?" cards here are built from the live page's work types
  plus the file's overtime/extra-pay questions. The file's
  8-state list (AZ, GA, IL, IN, OH, PA, TX, VA) appears nowhere
  on the live page, so it is not on this page — say the word if
  it should be added.
- **The sample's legal links are dead.** Its Privacy Policy,
  Disclaimer, and Terms of Use links all return GitHub Pages
  404s (checked 2026-11-20), so no second firm name could be
  cross-checked there. Kennedy Law Firm, LLP is the only firm
  named anywhere on the sample.
- **Pixel:** the client's file carries its own pixel
  (249210042119489). This build keeps our framework pixel; swap
  the two `fbq('init', ...)` / noscript lines if this campaign
  runs on the client's pixel instead.
- **No fee language.** The sample says nothing about fees or
  contingency, so none is claimed on this page (the framework's
  "No fee unless we win" footer line was replaced with the
  sample's "No cost to check").
