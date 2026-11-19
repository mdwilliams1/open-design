# Astra — Design System

> **Improve Life on Earth from Space®**

This project is the Astra brand design system: tokens, foundations, reusable
components, a marketing UI kit, and slide templates. An automated compiler reads
the sources and ships them to consuming projects — link `styles.css` and pull
components from the generated bundle.

---

## Company context

**Astra** is an aerospace company headquartered in Alameda, California, with a
mission to *Improve Life on Earth from Space®* by building a healthier, more
connected planet through **Launch Services** and **Space Products**. Everything
is designed, built, tested, and manufactured in the USA.

Two product lines anchor the brand:

- **Launch Services** — rapidly deployable orbital launch (Launch System 2),
  engineered for high cadence (up to one launch per week at scale), dedicated
  direct-to-orbit insertion, and best-in-class price per launch. Astra is the
  fastest company in history to reach orbit (five years from founding).
- **Astra Spacecraft Engine** — a flight-proven Xenon/Krypton electric
  propulsion system with a magnetically shielded thruster, manufactured at scale
  for spacecraft under 1 kW of power.

### Sources provided
- Brand logo set (square + horizontal, black/white, transparent + background)
  — supplied as PNG uploads, copied into `assets/logos/`.
- Product copy (mission, Launch Services, Spacecraft Engine specs) — supplied as
  text in the project brief.
- Fonts specified by the team: **Red Hat Display** (headings) and **Barlow**
  (body) — both Google Fonts.
- No codebase or Figma file was provided. Visual foundations below are derived
  from the logo marks and the team's stated direction (monochrome, pulled from
  the logos).

---

## Content fundamentals

How Astra writes.

- **Voice: confident, technical, mission-driven.** Copy leads with capability
  and outcomes, not hype. "Rapidly deployable launch systems engineered to
  deliver resilient access to orbit worldwide."
- **Person: "we" (Astra) speaking to "you" (the customer).** "We understand the
  importance of getting exactly where you need to be." "You get a launch partner
  that can keep pace." Direct, second-person, partnership-oriented.
- **Casing.** Sentence case for body and most headings. **ALL-CAPS** reserved for
  brand-level statements, eyebrows, labels, and section taglines —
  e.g. *SPACE ACCESS, REDEFINED*. The wordmark is always all-caps ASTRA.
- **Headline pattern: short, declarative, often two or three words.**
  "Built for Cadence." "Direct to Your Orbit." "Best-in-Class Pricing." These
  read like engineering callouts.
- **Numbers and specs are first-class.** Performance is communicated through
  precise, unit-bearing figures: `THRUST (XE): ~25 mN`, `SPECIFIC IMPULSE: ~1,400 s`,
  "up to one launch per week", "less than 1 kW". Tilde (~) used honestly for
  approximate values. Set specs in mono for a technical readout feel.
- **Tone is grounded, never whimsical.** No emoji. No exclamation-heavy
  marketing. The drama comes from scale and precision, not punctuation.
- **The registered mission line** — *Improve Life on Earth from Space®* — carries
  the ® and is used as a signature, not body copy.
- **Vocabulary:** orbit, cadence, dedicated, resilient, constellation,
  replenishment, flight-proven, on-orbit heritage, responsive access,
  national security. Aerospace-precise.

---

## Visual foundations

The brand is **strictly monochrome** — black, silver, white. There are no hues.
Hierarchy comes from weight, scale, spacing, and contrast, not color.

- **Color.** Brand black `#15181B` (the square-logo background), a deepest
  `#0B0D0F` for full-bleed dark sections, pure white `#FFFFFF`, and a single
  **silver** `#C2C5C8` (the secondary star in the mark) as the lone accent. A
  neutral ramp fills in text, borders, and fills. Status is signaled by
  weight/fill, not red/green. See `tokens/colors.css`.
- **Two surface modes.** Light (paper/fog backgrounds, ink text) is the default
  for content and UI. Dark (`.astra-dark` / `[data-theme="dark"]`) inverts for
  heroes, footers, and brand moments — this is where the white mark lives.
- **Typography.** **Red Hat Display** (700–900) for display and headlines —
  geometric, engineered, confident; often uppercase with negative
  tracking at large sizes. **Barlow** for body and UI. Uppercase **eyebrows /
  labels** with wide tracking (`0.18em`) are a signature motif. Mono is used for
  spec readouts. See `tokens/typography.css`.
- **Spacing.** 8px base grid; generous vertical rhythm in marketing layouts
  (96–160px section padding). See `tokens/spacing.css`.
- **Corners.** Sharp to nearly-sharp. Radii top out around 10px; most surfaces
  use 0–6px. The star mark is angular — the UI echoes it. Pills are reserved for
  tags/eyebrow chips only.
- **Borders.** Hairline (1px) borders do most of the separation work. On dark,
  borders are a faint `#2A2F34`; on light, `#D7DADC`/`#C2C5C8`. A 2px border is
  the "strong"/focus treatment.
- **Shadows.** Restrained, cool, low-opacity (`rgba(11,13,15,…)`), never
  colored. Cards on light lean on borders first, shadow second. Big elevation
  (modals) uses `--shadow-xl`. See `tokens/spacing.css`.
- **Cards.** White surface, 1px subtle border, small radius (6px), `--shadow-sm`.
  On dark: raised ink surface with a faint border, no shadow.
- **Backgrounds.** Predominantly flat fields — ink black or paper. Full-bleed
  imagery (rockets, orbit, hardware) is rendered cool / desaturated toward
  monochrome to stay on-brand; pair with a dark protection gradient (bottom-up
  ink fade) when text overlays. No purple/blue gradients, no patterns, no
  textures, no hand-drawn illustration.
- **Imagery treatment.** Cool, high-contrast, desaturated to near black-and-white.
  Hardware and sky photography; star-field where appropriate. Keep it grounded
  and real — never glossy 3D render clichés.
- **Motion.** Quick and mechanical. Standard `200ms`/`cubic-bezier(0.4,0,0.2,1)`;
  entrances use a gentle ease-out. **No bounce, no spring.** Fades and short
  transl(8–16px) reveals. Decorative loops are avoided.
- **Hover states.** Solid (primary) buttons darken (ink-900); outline/ghost fill
  with a faint neutral wash; links shift to full ink / underline. On dark,
  primary (white) buttons lighten slightly toward `#D7DADC`.
- **Press states.** Subtle — a 1px downward nudge or a slightly deeper fill. No
  large scale changes.
- **Focus.** 2px ink ring (silver on dark) with a small offset. Always visible.
- **Transparency / blur.** Used sparingly: a translucent ink scrim behind the
  sticky header (with `backdrop-filter: blur`) and protection gradients over
  imagery. Not a decorative glassmorphism system.
- **Fixed elements.** Sticky top nav with a blur scrim; everything else scrolls.

---

## Iconography

- **System: Lucide** (CDN). Astra's aesthetic is thin/precise line icons with a
  consistent ~1.75–2px stroke and square-ish geometry, which Lucide matches
  closely. No brand icon font or SVG sprite was provided in the source
  materials, so Lucide is used as the substitute set — **flag for the team:
  confirm or replace with Astra's own icon library if one exists.**
- Load from CDN: `https://unpkg.com/lucide@latest` (or the React build
  `lucide-react`). Render at 18–24px in UI, stroke `currentColor` so icons
  inherit the monochrome text color.
- **No emoji**, ever. **No unicode glyphs** used as icons.
- The **star/arrow mark** is the one piece of proprietary iconography — use the
  supplied logo PNGs in `assets/logos/`, never redraw it.

---

## Index — what's in this system

| Path | What |
|---|---|
| `styles.css` | Global entry point (import this). `@import`s all tokens. |
| `tokens/colors.css` | Monochrome color ramp + semantic aliases + dark scope. |
| `tokens/typography.css` | Font families, scale, weights, tracking. |
| `tokens/spacing.css` | Spacing, radius, border, shadow, motion, layout. |
| `tokens/base.css` | Element resets + brand utility classes. |
| `assets/logos/` | Astra marks: square + horizontal, black/white, transparent. |
| `components/core/` | Button, Badge, Tag, Card, StatBlock, Eyebrow, Input, Logo. |
| `guidelines/` | Foundation specimen cards (Type, Colors, Spacing, Brand). |
| `ui_kits/marketing/` | Astra marketing website recreation (hero, products, specs). |
| `SKILL.md` | Agent Skill manifest for downloadable/Claude Code use. |

**Components** (mount via `window.<Namespace>` from `_ds_bundle.js`):
`Button`, `Badge`, `Tag`, `Eyebrow`, `Card`, `StatBlock`, `Input`, `Logo`.

**UI kits:** `marketing` (Astra.com-style site).

*(No slide template was provided, so no slide samples are included — ask if you want a deck template built.)*
