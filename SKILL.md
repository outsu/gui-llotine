---
name: gui-llotine
description: Prevent AI UI slop and generic vibe-coded frontend patterns. Use whenever designing, building, styling, refactoring, or reviewing web UIs, mobile interfaces, landing pages, dashboards, HTML/CSS, Tailwind, React, or component libraries.
---
# gui-llotine

Eliminate generic AI-generated frontend patterns ("UI slop") and produce intentional, product-specific interfaces without over-constraining the layout.

## When to Use

- Building or styling new web pages, dashboards, landing pages, or app views
- Refactoring existing frontend components (React, Tailwind, shadcn/ui, CSS)
- Auditing or reviewing UI code for generic AI tells

## Steps

1. **Commit to a deliberate palette and typography first**

   - Ban default `indigo-500` / `violet-500` / `purple-500` gradients, neon-on-dark glowing box shadows, and timid all-cream fallback palettes unless matched to an existing brand.
   - Pick one high-contrast dominant surface, one sharp functional accent, and a deliberate font pairing instead of unstyled default `Inter` everywhere or random italic serif words inside sans-serif headings.

2. **Strip structural and component bloat**

   - **No left-border stripe cards:** Never put a 3-4px colored left or top border on regular cards (`border-l-4`). Reserve colored edges strictly for semantic alerts.
   - **No nested box-in-box grids:** Group related content with whitespace and typography first instead of wrapping every section, list item, and stat in its own bordered card.
   - **No eyebrow and badge spam:** Drop ALL-CAPS mini labels ("FEATURES", "WORKFLOW") and pill badges ("NEW", "AI", pulsing green "LIVE" dots) above every heading.
   - **Break the 3-card icon clone:** Avoid rows of identical `rounded-xl` cards with a Lucide icon (`Sparkles`, `Zap`, `Shield`, `Rocket`) inside a tinted square stacked above a title. Never use emojis as UI icons.

3. **Write concrete, human UI copy**

   - Start headings with specific verbs or outcomes instead of vague slogans ("Build the future", "All-in-one platform") or gradient-clipped text (`bg-clip-text`).
   - Use digits (`3`), not spelled-out words (`three`), in UI labels and metrics. Never invent fake "+24.5% from last month" stats, avatar stacks, or placeholder testimonials.
   - Avoid em-dashes in UI microcopy and keep monospace fonts strictly for code, IDs, and tabular numbers (`tabular-nums`).

4. **Create hierarchy through asymmetry and state**

   - Vary padding, grid spans, and visual weight so primary actions dominate rather than making every card identical in height and radius.
   - Define crisp interactive states (`hover`, `focus-visible`, `active`, `disabled`) with fast, subtle transitions instead of generic scroll fade-ins.

## Gotchas

- **Anti-purple cascade:** When banned from purple, models automatically fall back to Tailwind `emerald-500` or warm beige/amber. Choose colors based on domain context, not the next statistical default.
- **Unmodified library defaults:** Using Tailwind or shadcn/ui is fine, but shipping untouched default radii, spacing, and Lucide `Sparkles` icons immediately flags a layout as AI-generated.