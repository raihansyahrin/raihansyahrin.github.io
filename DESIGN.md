# DESIGN.md — raihansyahrin.github.io

Rules for any edit to `index.html`, by hand or by an AI assistant. If a change breaks a rule here, change the rule on purpose or don't make the change.

## Banned

- Purple/indigo accents, two-stop glow gradients, glassmorphism, floating blobs.
- Inter or a bare system font stack as the body face.
- Emoji as icons. Stock or AI-generated imagery. Every image is a real screenshot or app icon.
- Everything-in-cards layouts, rounded cards with thin colored borders.
- Pure `#000` / `#FFF`. Use the tokens below.
- Hero → features → pricing template sections.

## Type

| Role | Face | Size |
|---|---|---|
| Display (h1, h2, numbers, kickers) | Bricolage Grotesque 700/800, tight tracking (-.03em) | h1 `clamp(56px,9vw,112px)`, band h2 `clamp(40px,6vw,72px)` |
| Hero name | Bricolage Grotesque 500 | `clamp(28px,3.4vw,44px)` |
| Hero role | Instrument Serif italic 400, terracotta | `clamp(52px,7.4vw,104px)`. Only place the serif is used |
| Body | IBM Plex Sans 400/600 | 17px desktop, 16px mobile, line-height 1.6 |
| Kicker | Bricolage 700, 13px, uppercase, .08em | — |

## Color tokens

| Token | Value | Use |
|---|---|---|
| `--paper` | `#F6F4EF` | page background |
| `--ink` | `#161513` | text |
| `--ink-2` | `#3A3833` | secondary text |
| `--muted` | `#6B675F` | dates, captions |
| `--rule` | `#DDD8CD` | hairlines |
| `--link` | `#B4361A` | the one accent (terracotta) |

Each project band has its own soft background + one darker kicker color taken from the app's own palette (Kosmogram navy/gold, Nova blue, Obrol Sandi sand, DOKAR lavender, Teman Muslim mint, KGTK sky, contact peach). Every text pair must pass WCAG AA (4.5:1); check new pairs before shipping.

## Spacing and layout

- Container 1160px, side gutter 28px (18px under 560px).
- Section padding 88–96px (64px on mobile). Grid gaps 56px desktop, 32px stacked.
- Breakpoints: 960px (stack columns), 560px (phone).
- Icon shelf: 9 columns, 5 at tablet, 3 on phone, `minmax(0,1fr)` so long names never resize icons.

## Interaction

- Nav: floating ink bar (sticky, 12px from top, radius 14px) with the phone-R mark; the link for the section in view gets a terracotta underline.
- Favicon: ink phone with a paper R and a terracotta speaker slot.

- Links: underline 1px, 2px on hover. Focus ring 3px `currentColor`.
- Screenshots open in the `<dialog>` lightbox; prev/next stay within the project; Esc, arrows, and swipe work.
- Store links go to Google Play; `data-ios` swaps to the App Store on iPhone/iPad.
- Respect `prefers-reduced-motion`. No entrance animations.

## Before shipping

Check at 390px width, tab through the page with the keyboard only, and confirm the CV link downloads the current PDF.
