# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

A single-file static hair salon website ("Friseursalon") written in German. No build system, no package manager, no test framework. All HTML, CSS, and JavaScript live in one file.

- `index.html` — the entire application
- Open directly in a browser; no server or build step needed.

## Architecture

All code is inline in `index.html`, organized in clearly labelled comment blocks.

**CSS (inside `<style>`):**
- Define design tokens as CSS custom properties in `:root` — always use these vars, never hardcode colors, fonts, or spacing.
- Responsive breakpoints: `≤768px` (tablet), `≤600px` (mobile), `≤400px` (small mobile).
- Include `@media (prefers-reduced-motion: reduce)` to disable animations for accessibility.

**JavaScript (inside `<script>`):**
- Keep JS minimal and vanilla — no frameworks, no bundlers.
- Use `DOMContentLoaded` to initialize interactive elements (e.g., mobile nav toggle, booking form validation, lightbox).

## Conventions

- Language: German throughout (UI text, comments, variable names where contextual).
- Formatting: German locale (`de-DE`) for any dates, times, or prices.
- Images: use `alt` text in German; prefer optimized formats (WebP with JPEG fallback).
- Accessibility: semantic HTML elements (`<nav>`, `<section>`, `<article>`, `<footer>`), ARIA labels where needed.

## DSGVO-Regeln (Pflicht)
- Keine Google Fonts via CDN — immer lokal hosten
- Keine Google Analytics oder externe Tracking-Scripts
- Keine externen Ressourcen die IP-Adressen übertragen ohne Einwilligung
- Google Maps nur als iframe mit 2-Klick-Lösung einbinden
