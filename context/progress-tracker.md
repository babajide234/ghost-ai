# Progress Tracker

Update this file whenever the current phase, active feature, or implementation state changes.

## Current Phase

- Phase 1: Foundation

## Current Goal

- Define the immediate implementation goal here.

## Completed

- Feature 01: Design system — shadcn/ui initialized, UI primitives added, dark theme tokens configured, `cn()` utility in `lib/utils.ts`.

## In Progress

- None.

## Next Up

- Feature 02 (next feature unit to be defined in context/feature-specs/).

## Open Questions

- None yet.

## Architecture Decisions

- `lib/utils.ts` used instead of `libs/utils.ts` to match the `lib/` boundary defined in architecture-context.md.

## Session Notes

- Using Next.js 16.2.4 + Tailwind v4 (no tailwind.config.ts — config via `@theme inline` in globals.css).
- shadcn init rewrites globals.css; dark theme tokens were applied after init.
- Circular font reference `--font-sans: var(--font-sans)` fixed with literal Geist font names in `@theme inline`.
- Project is dark-only — `dark` class applied on `<html>` in layout.tsx; `:root` and `.dark` blocks both carry dark palette values.
- Project design tokens (`--bg-base`, `--text-primary`, etc.) are defined in `:root`/`.dark` and mapped to Tailwind utilities (`bg-base`, `text-copy-primary`, etc.) via `@theme inline`.
