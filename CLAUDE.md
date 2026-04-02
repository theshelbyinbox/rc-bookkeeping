# Rachel Cooper Bookkeeping — Project Handoff

## Project Overview

Multi-phase web project for Rachel Cooper, bookkeeper in rural Lake County, Oregon. Started as a standalone pricing calculator rebuild; expanded to a full landing page rebuild and three complete website concept designs. All deliverables are single self-contained HTML files (inline CSS/JS, no build step, Google Fonts only).

Rachel's phone: 541-219-1828

---

## Files — Current Status

**Pricing Calculator (active — teal version only):**
- `rachel-pricing-calculator.html` — Teal version, fully polished, primary deliverable

**Landing Page (built, not yet reviewed by Shelby):**
- `rc-bookkeeping-landing.html` — Continuous-scroll replica of rc-bookkeeping.com. Sections: sticky nav, hero, services, about, contact, footer. Fonts: Crimson Text (headers) + Oxygen (body).

**Three Concept Pages (built, not yet reviewed by Shelby):**
- `rc-concept-1-quiet-authority.html` — The Quiet Authority
- `rc-concept-2-the-neighbor.html` — The Neighbor You Trust
- `rc-concept-3-strategic-guide.html` — The Strategic Guide

**Reference / Supporting Materials:**
- `Rachel Cooper Monthly Pricing Calculator - FOR CLAUDE.md` — Original pricing spec from ChatGPT build (~96KB)
- `Rachel Cooper - Services Page Copy.md` — Three website copy options (Warm/Confident/Casual) with sales psychology breakdown
- `RC Bookkeeping Brand Board.png` — Brand colors, fonts, and overall vibe reference
- `RC Bookkeeping Logo - Transparent Dark Teal.png` — Logo, dark teal version
- `RC Bookkeeping Logo - Transparent White.png` — Logo, white version (used in nav/footer of concept pages)
- `Rachels Photos/` — 9 photos used in concept pages (mix of headshots, outdoor/ranch scenes)

**Stale / Not Being Maintained:**
- `rachel-pricing-v1-sage.html` — Sage version of calculator; abandoned after Shelby chose teal only
- `Rachel Cooper Monthly Pricing Calculator.html` — Older title-case copy, pre-polish
- `Rachel Cooper Monthly Pricing Calculator - Sage.html` — Older title-case sage copy, pre-polish

---

## Phase 1 — Pricing Calculator (Complete)

**Core logic:**
- Checkbox/dropdown inputs for 6 service categories
- Real-time calculation across 3 tiers: Normal Months (8/year), Quarterly Months (Apr/Jul/Oct), January Year-End
- Payroll formula: $72 x frequency_multiplier x employee_multiplier
- Frequency multipliers: 1x/month=1.0, 2x/month=1.75, Weekly=2.5
- Employee multipliers: 1-2=1.0, 3-5=1.2, 6-10=1.4, 11-15=1.6, 16+=2.0
- Monthly Bookkeeping ($228) = Data Entry ($120) + Bank Reconciliation ($108)
- Tax Deposits: "Prepare Only" ($72) vs. "Prepare & Submit" ($96)

**Design polish applied:**
- Unified card with single shadow/border-radius (no disconnected floating blocks)
- Header flows flush into body (no gap)
- Solid left-accent estimate badge (replaced dashed "draft-looking" border)
- Clean whole-dollar currency display ($444 not $444.00)
- Estimate text repositioned as italic subheading under "Estimated Pricing"
- Empty state removed entirely
- Vary section moved full-width below the grid, centered, with increased contrast/font size
- Bullets on vary section enlarged (1.4rem, inline)
- Checkbox border darkened for accessibility
- Smooth CSS transitions on price changes

**CSS Variable Reference:**
```css
--cream: #D9CCC4; --rose: #C3937D; --gold: #E9A753;
--teal: #375257; --chocolate: #3C2517; --white: #FAF8F5;
--light-bg: #F0EBE5; --text-dark: #3C2517; --text-muted: #7A6E63; --border: #D9CCC4;
```

**Sales psychology layer:**
- Estimate framing language throughout (prices are starting points, not fixed quotes)
- Low-pressure CTA with phone button
- "Why Your Actual Price May Differ" section with 4 reasons
- Services page copy (3 options) saved separately for Rachel's website

---

## Phase 2 — Landing Page Rebuild (Built, Awaiting Shelby Review)

Built as a single-page scroll version of rc-bookkeeping.com with 4 sections flowing top-to-bottom.

**Sections:**
| Section | Layout | Notes |
|---|---|---|
| Sticky Nav | Fixed top, dark teal, hamburger on mobile | Brand name + smooth-scroll links |
| Hero | Two-column (text left, photo right) | image01.jpg from live site |
| Services | Two-column (image left, checklist right) | 7 services, teal checkmarks, calculator link |
| About | Full-width banner + centered text | image02.jpg, three bio paragraphs |
| Contact | Centered card with form | Placeholder — Cloudflare backend setup pending |
| Footer | Dark teal bar | SVG social icons, copyright |

**Technical:**
- Fonts: Crimson Text (headers) + Oxygen (body)
- Images load from rc-bookkeeping.com CDN
- Contact form action="/api/contact" — placeholder, Cloudflare backend not yet set up
- Responsive at 980px, 768px, 480px

---

## Phase 3 — Three Concept Rebuilds (Built, Awaiting Shelby Review)

Research-driven redesigns based on Maria Wendt, Why We Buy, Rebecca Ives, and Shelby's Storytelling/Funnels resource library. Core insight: invisible sales psychology baked into structure and copy, not surface-level sales language.

**All three share:**
- Brand fonts: Crimson Pro (headers) + Nunito Sans (body) per brand board
- Brand colors: teal (#375257), brown (#8C6C5A), gold (#C9A96E), rose (#C3937D), sage (#818275), cream (#F5F0EB)
- White logo in nav and footer
- Rachel's actual photos from Rachels Photos/
- Pain-first headlines, outcome-framed services, no individual line-item prices
- Testimonial placeholder sections (real testimonials still needed from Rachel)
- Responsive at 980px, 768px, 480px with hamburger menus on mobile

**The Three Concepts:**

| File | Concept | Hero Approach | Core Psychology |
|---|---|---|---|
| rc-concept-1-quiet-authority.html | The Quiet Authority | Two-column, pain-point headline, Rachel's photo | Specificity converts. Painkiller > vitamin. Pre-sell before the call. |
| rc-concept-2-the-neighbor.html | The Neighbor You Trust | Full-bleed Rachel photo on dirt road, text overlay | Shared rural identity = instant trust. People hire people. |
| rc-concept-3-strategic-guide.html | The Strategic Guide | Bold white-on-teal typographic hero, no image | Loss aversion. Omission bias reversal. Cost of NOT hiring a bookkeeper. |

**Section breakdown:**
- Concept 1: 5 sections + nav + footer — two-column hero, centered about with pull-quote, service checklist cards, 3 testimonial cards, white contact card on teal
- Concept 2: 5 sections + nav + footer — full-bleed hero, alternating image/text blocks, photo banner with stat overlay, two-column contact
- Concept 3: 8 sections + nav + footer — typographic hero, numbered transformation items, circular portrait, 3-column service card grid, lead magnet section with email capture, editorial layout

**Known rendering note:** Preview tool had scrolling issues capturing content below the fold, but DOM verification confirmed all sections are present and correct on all three files. Open in actual browser for full review.

**Claude's recommendation:** Concept 1 as the foundation, with Concept 3's assessment-style calculator as a Phase 2 tool.

---

## Pricing Calculator Strategy — Unresolved Decision

The strategy research surfaced an important concern: **the existing pricing calculator may be hurting conversions.** It gives visitors exact numbers (price anchoring), removes their incentive to call Rachel, and allows them to self-serve and leave without starting a relationship.

Three options identified:
1. **Remove it from the main page** — replace with a soft price range ($200–$500/month) and a CTA to call
2. **Keep it as a standalone tool** — link to it from the page but don't embed it inline
3. **Rebuild it as a lead-capture assessment** — interactive form that collects info and delivers a personalized estimate in exchange for an email (the Concept 3 approach)

This decision is still open. No change made to the calculator yet.

---

## What's Open / Next Steps

1. **Shelby reviews all three concept pages** — open in browser for full scroll-through (not just preview tool)
2. **Choose a concept (or hybrid)** to develop further and present to Rachel
3. **Collect testimonials from Rachel** — identified as the single highest-impact missing element; need 3-5 real client quotes before final build
4. **Decide on calculator strategy** — keep, remove, or rebuild as lead-capture tool
5. **Cloudflare contact form backend** — not set up yet; form is HTML placeholder
6. **SEO** — flagged as Phase 4 task; keyword strategy not yet started
7. **Present to Rachel** — once Shelby approves a direction, package and send to Rachel Cooper
8. **Clean up stale files** — sage version + old title-case copies can be deleted once confirmed no longer needed

---

## Decisions Made and Why

- **Single HTML files over React** — simplicity and portability; Rachel can open in any browser without a build step
- **Teal version only** — Shelby chose teal calculator over sage; sage version no longer maintained
- **Fresh brand-board redesign for concepts** — used RC Bookkeeping brand board colors/fonts rather than replicating the Canva original
- **No individual line-item pricing on concept pages** — strategy research recommended replacing specific prices with a soft range to prevent anchoring and push people toward calling
- **Testimonials as structural requirement** — all three concepts include placeholder testimonial sections; real quotes from Rachel's clients are needed before any concept is final
- **Three concepts built simultaneously** — Shelby wanted all three options to evaluate before committing to a direction
