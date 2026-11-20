# Overtime Justice Help — Checklist Variant (Version B)

Static GitHub Pages rebuild of
https://overtimejusticehelp.com/checklist.html, converted from
the client's supplied file (`checklist.html`, "Data Center
Workers: Overtime Check (Version B)") into our current
framework format. Built from the Version A overtime build
(`github-overtime-justice-help-landing-page/`), same firm,
same embed, recolored and re-laid-out for this version.
HTML + CSS only, no PHP.

## Framework carried over (unchanged)

- MTAA CIPA block script in the head
- Meta Pixel **1238664640565416** + ViewContent
- MTAA form embed **nf_3270a8a1b0e4425cb70e9f97f2fa5a3c** in the
  overflow form card (hangs past the hero, scrolls internally)
- Relative footer legal links (privacy-policy.html / disclaimer.html)

## Branding

- **Kennedy Law Firm, LLP**, 2925 Richmond Ave., Ste. 1200,
  Houston, TX 77098 — Galvin Kennedy responsible for the page
- Phone **713-425-6445** in the header and footer (the rendered
  sample displays it twice)
- Footer disclaimer is the sample's own four paragraphs, verbatim
- This version uses the firm name as **text** in the header —
  there is no logo image on the sample page, so none is referenced
- Verified: zero traces of the previous build's Version A colors
  or the tobacco framework

## Palette — sampled live from the rendered page, 2026-11-20

Matches the client's file exactly:

| Surface | Color |
|---|---|
| Page / header background | white `#ffffff` |
| Hero background | sky blue `#e3eeff`, amber `#ffb703` divider |
| Headings / ink | navy `#10224a` |
| CTA buttons | royal blue `#1f5fe0` (hover `#1648b0`) |
| Section-heading bands | sky `#e3eeff` |
| Form-heading bar | pale amber `#ffe7a8` |
| Checklist card | white, `#c9dcff` border, `#ffe7a8` header |
| Cards / fields | pale blue `#eef4ff`, border `#b8cdf2` |
| Headline highlighter | amber `#ffb703`–`#ffe7a8` gradient |
| Header / footer phone | royal blue `#1f5fe0` |
| Footer | white, on the page background |

Headings use **Source Serif 4** (the sample's heading face); body
is **IBM Plex Sans**.

## Content — kept to what this version actually has

Unlike Version A, this page has no FAQ, no qualify cards, no
extra-pay cards, and no closing CTA section — so this build has
none of those either. What it has, in the sample's order:

1. Hero: "Data Center Workers: Is Your Overtime Pay Short?"
   with the amber highlight, the two-item "Does this sound like
   you?" checklist card, and the form card beside it
2. "Why the overtime rate might be wrong" — the federal-law
   paragraph plus the trades list (including commissioning techs)
3. "What happens next" — the same three steps, as a plain
   numbered list (as on this version, not the numbered circles)

The five-question form (worked on a data center project; how
paid; 40+ hours; extra pay; state — AZ, GA, IL, IN, OH, PA, TX,
VA, or another state) is the sample's native form, replaced here
by our MTAA embed, as on Version A.

## CSS changes vs the Version A build

Colors and heading/body font-family values only, plus two small
additions the framework has no rule for (grouped in the marked
block at the end of style.css): the hero checklist card and the
plain numbered "What happens next" list. The Version A numbered
steps and card-check rules are still in the stylesheet, unused.
Diff-verified.

## Placeholders — one file to drop in

- **`hero-b2.jpg`** — the electrician photo, referenced as the
  hero parallax background (same filename the client's file
  uses). Drop it into this folder's root.

The other parallax bands point at `YOUR-IMAGE-URL-HERE` (unused
on this page's sections, kept from the framework).

## Flags

- **The sample's own form has an empty lead endpoint**, same as
  Version A (`leadEndpoint: ""`). This build uses our MTAA embed
  instead, so leads flow normally.
- **This version's quiz matches its file.** Unlike Version A
  (live Q1 differed from the file), the live checklist quiz asks
  the same five questions as the supplied file, including the
  8-state list — so no quiz divergence to flag here.
- **The sample has no legal links at all** — no Privacy Policy,
  Disclaimer, or Terms links on the checklist page. The
  framework's relative privacy-policy.html / disclaimer.html
  links are kept (his own pages). For reference, the main page's
  legal links still don't load (Privacy Policy returns a GitHub
  500, Disclaimer a 404, checked 2026-11-20).
- **Pixel:** the client's file carries its own pixel
  (249210042119489). This build keeps our framework pixel; swap
  the two `fbq('init', ...)` / noscript lines if this campaign
  runs on the client's pixel instead.
- **No fee language.** The sample says nothing about fees or
  contingency, so none is claimed on this page.
