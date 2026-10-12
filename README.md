# Vcodex X3 — Whole-book EPUB page counter

This repository is being prepared for a CPR-vCodex modification for the Xteink X3.

## Goal

Show a bottom-of-screen counter for the current page and estimated total pages across the entire EPUB book, without resetting at chapter boundaries.

## Status

- Source modification patch: not yet committed.
- Firmware `.bin`: not built or tested.
- The page count in EPUB readers depends on font/layout settings. A reliable whole-book count requires pagination data for all spine sections; a byte-size estimate is not exact.

## Upstream

CPR-vCodex is based on CrossPoint Reader: https://github.com/crosspoint-reader/crosspoint-reader

The intended base source is the CPR-vCodex archive discussed in the ChatGPT conversation. Before installing any firmware, build and test it for the exact Xteink X3 hardware revision.
