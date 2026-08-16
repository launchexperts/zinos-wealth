# Handoff: Zinos Wealth — Home page + Coming Soon page

## Overview
Marketing site front end for Zinos Wealth, a Queensland-based financial advisory practice. Two screens: a full home page (hero, value strip, about, services, CTA, footer) and a single-screen "coming soon" holding page. Both share one brand system.

## About the Design Files
The HTML files in this bundle are **design references created in HTML** — prototypes that show the intended look, copy, and behavior. They are not production code to copy verbatim. The task is to **recreate these designs in the target codebase's environment** (React/Next, Vue, Astro, WordPress theme, etc.) using its established patterns, component library, and styling approach. If no environment exists yet, pick an appropriate framework and implement there.

Note on file format: the `.dc.html` files are single-file prototypes with all styling written inline. They open directly in a browser (they load a small local `support.js` runtime, included). Treat the inline styles as the spec, not as the intended implementation style — extract them into the target codebase's CSS/utility/token system.

## Fidelity
**High fidelity.** Colors, typography, spacing, and copy are final-intent and were matched to an approved visual mockup. Recreate closely. Two caveats:
- The photographs were extracted from a low-resolution mockup screenshot. Replace with the original high-res photography before launch.
- The section icons (people, target, shield, chart, piggy bank, umbrella, leaf, phone, mail, pin) are hand-drawn 1.2–1.3px stroke SVGs standing in for the brand's real icon set. Swap for the real assets if they exist.

## Screens / Views

### 1. Home (`Zinos Wealth Home.dc.html`)
Purpose: introduce the practice, communicate the service range, drive "Book a discovery call".
Page background `#FAF7EF`. Designed for a ~1440px desktop viewport; horizontal page gutter is **112px** on all content sections (header uses 48px).

**1.1 Header** — `#FCFAF3`, padding `22px 48px`, bottom border `1px solid rgba(0,0,0,.05)`. Flex row, space-between: logo image (`assets/logo-zinos.png`, height 52px, auto width, links to home) · nav · CTA.
- Nav: flex row, gap 38px, font-size 12px, letter-spacing .14em, uppercase, `white-space:nowrap`. Items: HOME, ABOUT, SERVICES, OUR PROCESS, RESOURCES, CONTACT. Inactive `#403C36`; active (HOME) `#B99447` with `padding-bottom:6px; border-bottom:1px solid #B99447`.
- CTA: "BOOK A DISCOVERY CALL", background `#C0A053`, white text, 12px / .14em, padding `19px 34px`, square corners. Hover `#A9873D`.

**1.2 Hero** — `min-height:710px`, flex centered, background `linear-gradient(180deg,#FAF6EC 0%,#F7F2E6 100%)`, `overflow:hidden`.
- Photo: `assets/hero-coast.png`, absolutely positioned top/right, `height:100%; width:56%; object-fit:cover; object-position:right center`, faded into the background on its left edge with `mask-image: linear-gradient(90deg, transparent 0%, rgba(0,0,0,.35) 18%, #000 46%)`.
- Text column: `padding:0 48px 0 112px; max-width:640px`, sits above the photo.
  - Eyebrow "FINANCIAL ADVISORY IN QUEENSLAND" — 12px, letter-spacing .2em, `#B99447`, margin-bottom 26px.
  - H1 — Cormorant Garamond 400, **73px**, line-height 1.16, letter-spacing -.005em, `#241F19`. Two lines: "Plan with purpose." / "Live with *confidence.*" — the last word italic in `#B99447`.
  - Gold rule: 64×2px `#C0A053`, margin `34px 0 32px`.
  - Body — 17px / 1.85, `#4A453D`, max-width 400px: "Personalised financial advice to help you grow, protect and enjoy your wealth — today and into the future."
  - Actions row (gap 52px): primary button `#C0A053` / white, 12.5px / .14em, padding `20px 36px`; text link "LEARN MORE" `#2C2A26` with a 26×1px gold line + 7px rotated-45° chevron head as the arrow.

**1.3 Value strip (dark)** — background `#262421`, padding `54px 112px 58px`. 4-column CSS grid; columns 2–4 have `border-left:1px solid rgba(255,255,255,.14)`. Each cell: centered column, gap 22px, padding `0 34px` — 38px gold-stroke icon, label 13px / .16em uppercase white, body 14.5px / 1.8 `#C9C4BB` (max-width ~210–230px).
Content: CLIENT FIRST / "Your goals come first. Always." · CLEAR ADVICE / "Strategic, transparent advice you can rely on." · FINANCIAL CONFIDENCE / "Helping you make informed decisions with confidence." · LONG TERM THINKING / "Building and protecting wealth for generations."

**1.4 About** — background `#FAF6EC`, padding `96px 112px 104px`. Grid `minmax(0,1fr) minmax(0,1.32fr)`, gap 96px, items centered.
- Left: eyebrow "ABOUT ZINOS WEALTH" (12px / .2em gold) · H2 Cormorant Garamond 400 **52px** / 1.25 `#241F19`, "Independent advice." / "Focused on *you.*" (italic gold) · 56×2px gold rule · two paragraphs 16px / 1.9 `#4A453D`, max-width 470px · outlined button "LEARN MORE ABOUT US" — `1px solid #C0A053`, text `#8C6E2E`, 12.5px / .14em, padding `20px 30px`, arrow at gap 30px; hover fills `#C0A053` with white text.
- Right: photo `assets/about-beach.png`, `width:100%; height:556px; object-fit:cover`, with a `1px solid #C0A053` frame offset up-and-left: wrapper `padding:44px 0 0 44px` and an absolutely positioned border box at `left:0; top:0; right:44px; bottom:44px`.

**1.5 Services** — background `#FDFBF6`, padding `88px 112px 76px`. Centered head: eyebrow "OUR SERVICES" · H2 Cormorant Garamond 400 **50px**, letter-spacing .01em, "Comprehensive advice. Tailored strategies." · 56×2px gold rule, auto-centered.
5-column grid, `margin-top:70px`; columns 2–5 have `border-left:1px solid rgba(185,148,71,.28)`. Each cell: centered, gap 20px, padding `0 26px` — 52px gold icon, title 12.5px / .15em uppercase `#241F19`, body 14.5px / 1.8 `#4A453D` max-width 190px, then a gold arrow link (26×1px line + chevron, margin-top 14px).
Content: WEALTH CREATION / "Strategies to grow your wealth and achieve your financial goals." · WEALTH PROTECTION / "Protecting your income, assets and lifestyle against the unexpected." · RETIREMENT PLANNING / "Plan for the retirement you want and enjoy financial freedom." · SUPERANNUATION / "Make the most of your super and build a strong future." · ESTATE PLANNING / "Preserve your legacy and provide for future generations."

**1.6 CTA band (dark)** — `#262421`, padding `76px 112px`. Inner max-width 1120px, centered; two equal columns.
- Left: H2 Cormorant Garamond 400 **46px** / 1.3 `#F6F2E9` — "Let's create your" / "financial future *together.*" (italic `#C0A053`); `padding-right:80px`.
- Right: `border-left:1px solid rgba(192,160,83,.5)`, `padding-left:96px`; body 16px / 1.85 `#D5D0C6` max-width 390px — "Book a discovery call to discuss your goals and find out how we can help you achieve them."; gold button with white arrow, padding `21px 34px`, gap 34px.

**1.7 Footer** — background `#FAF6EC`. Top grid `1.5fr 1fr 1fr 1.2fr`, gap 48px, padding `60px 112px 56px`: logo image (height 50px) · NAVIGATION column · SERVICES column · CONTACT column. Column headings 11.5px / .18em uppercase `#241F19`, margin-bottom 20px; links 14.5px `#4A453D` in a flex column, gap 11px. Contact rows use 15px gold-stroke icons at gap 14px: `07 3188 9123`, `hello@zinoswealth.com.au`, `Level 12, 240 Queen Street / Brisbane QLD 4000`.
Legal bar: `border-top:1px solid rgba(0,0,0,.09)`, padding `20px 112px 26px`, 12px `#6A645B`, space-between — ABN/AFSL line on the left; "Privacy Policy | Terms & Conditions" on the right (gap 26px, `|` at `rgba(0,0,0,.18)`).

### 2. Coming Soon (`Zinos Wealth Coming Soon.dc.html`)
Purpose: holding page before launch; keeps phone/email/address reachable.
Full-viewport grid, `minmax(0,1fr) minmax(0,0.92fr)`, background `#FAF6EC`.
- Left column: `min-height:100vh`, flex column, `justify-content:space-between`, padding `52px 72px 44px 96px`, `box-sizing:border-box`.
  - Top: logo image, height 50px, links to the home page.
  - Middle block (`padding:64px 0`): eyebrow "FINANCIAL ADVISORY IN QUEENSLAND" (12px / .2em gold) · H1 Cormorant Garamond 400 **70px** / 1.15 `#241F19`, max-width 600px, line 1 "Something considered is", line 2 italic gold "on the way." (explicit line break) · 64×2px gold rule (`margin:34px 0 30px`) · paragraph 17px / 1.85 `#4A453D`, max-width 430px: "Our new site launches soon. In the meantime, we are already taking on clients who want personalised advice to grow, protect and enjoy their wealth."
  - Bottom contact band: `border-top:1px solid rgba(0,0,0,.09)`, `padding-top:34px`, flex wrap, gap `40px 56px` — phone, email, address rows (same icon treatment as the footer), plus the ABN/AFSL line at 12px `#8A8378` on its own full-width row.
- Right column: `position:relative; overflow:hidden`, fallback background `#EFE9DB`. Photo `assets/hero-coast.png` absolutely full-bleed, `object-fit:cover; object-position:65% center`; over it a `linear-gradient(90deg, rgba(250,246,236,.85) 0%, rgba(250,246,236,0) 34%)` wash so the photo blends into the left column; inset `1px solid rgba(255,255,255,.55)` frame at 44px from every edge, `pointer-events:none`.

## Interactions & Behavior
- All nav, footer, and card arrow links are anchors. In-page anchors on home: `#about`, `#services`. Everything else is a placeholder `#` pending real routes.
- Hover states (no transition duration was specified — 150–200ms ease is a reasonable implementation choice):
  - Gold buttons: `#C0A053` → `#A9873D`, text stays white.
  - Outlined button: transparent → `#C0A053` fill, text `#8C6E2E` → white (arrow uses `currentColor`, so it follows).
  - Text links: `#B99447` → `#8C6E2E`; the "LEARN MORE" hero link goes `#2C2A26` → `#B99447`.
- No animation, loading, or error states in these designs. No forms (an email-capture field was designed and then removed from the coming-soon page at the client's request).
- Responsive behavior was not designed. Both pages are desktop-first fixed layouts; the nav and header CTA use `white-space:nowrap` and will overflow below roughly 1100px. Mobile/tablet breakpoints need design work — the obvious moves are stacking the hero photo below the copy, collapsing the 4- and 5-column strips to 2 columns and then 1, stacking the CTA band, and stacking the coming-soon grid with the photo as a top band.

## State Management
None. Both pages are static; no state variables, no data fetching. If the notify-me capture is reinstated later it needs one email field, a validity flag, and a message string.

## Design Tokens

Colors
| Role | Value |
| --- | --- |
| Page cream (base) | `#FAF7EF` |
| Cream, header | `#FCFAF3` |
| Cream, section (about/footer/coming-soon) | `#FAF6EC` |
| Cream, services section | `#FDFBF6` |
| Hero gradient | `#FAF6EC` → `#F7F2E6` |
| Photo fallback | `#EFE9DB` |
| Dark sections | `#262421` |
| Heading ink | `#241F19` |
| Body ink | `#4A453D` |
| Nav ink | `#403C36` |
| Muted ink | `#6A645B` / `#8A8378` |
| Gold, solid (buttons, rules, icons) | `#C0A053` |
| Gold, text/eyebrow | `#B99447` |
| Gold, hover fill | `#A9873D` |
| Gold, deep text | `#8C6E2E` |
| On-dark heading | `#F6F2E9` |
| On-dark body | `#D5D0C6` / `#C9C4BB` |
| Hairline on cream | `rgba(0,0,0,.09)` (borders `rgba(0,0,0,.05)`, dividers `rgba(0,0,0,.18)`) |
| Hairline on dark | `rgba(255,255,255,.14)`; gold divider `rgba(192,160,83,.5)` |
| Gold hairline on cream | `rgba(185,148,71,.28)` / `rgba(185,148,71,.45)` |

Typography — headings: **Cormorant Garamond** (weight 400; italic 400 for the accent words). UI/body: **Jost** (300/400/500). Both Google Fonts.
Scale: H1 home 73px · H1 coming-soon 70px · H2 about 52px · H2 services 50px · H2 CTA 46px · body large 17px/1.85 · body 16px/1.9 · card body 14.5px/1.8 · footer link 14.5px · button 12–12.5px/.14em uppercase · eyebrow 12px/.2em uppercase · card title 12.5px/.15em uppercase · column heading 11.5px/.18em uppercase · legal 12px · logo tagline (retired) 10–10.5px/.28em.

Spacing — section vertical padding 54–104px; page gutter 112px (header 48px); grid gaps 48–96px; card inner gap 20–22px; button padding `19–21px × 30–36px`.

Radius — **0 everywhere**. No rounded corners, no shadows. Rules are 2px tall × 56–64px wide; all borders are 1px.

Iconography — 38px (dark strip), 52px (services), 15px (contact), stroke-only, `#C0A053`, stroke-width 1.2–1.3, `fill:none`. Arrows are built from a 26×1px line plus a 7×7px element with top+right 1px borders rotated 45°.

## Assets
In `assets/`:
- `logo-zinos.png` — supplied by the client (`04-website-header-transparent-dark-mark.png`), transparent PNG, cropped to tight bounds (1376×375, aspect 3.67:1). Dark mark + "ZINOS WEALTH" wordmark; used at 50–52px height on cream. A light/reversed version does not exist yet and is needed if the logo ever sits on `#262421`. The original mockup paired the logo with a "FINANCIAL ADVISORY" tagline lockup; that tagline is not part of this file.
- `hero-coast.png` (695×739) and `about-beach.png` (612×514) — **both cropped out of the client's mockup screenshot**, so they are low resolution. Replace with the original photography (Gold Coast skyline from the north, and a Burleigh-style beach at sunrise).

Fonts load from Google Fonts via `<link>`; self-host in production.

## Files
- `Zinos Wealth Home.dc.html` — home page design
- `Zinos Wealth Coming Soon.dc.html` — coming-soon page design
- `support.js` — the prototype runtime these two files load so they open in a browser. Not part of the design; do not port it.
- `assets/` — logo and photography above
