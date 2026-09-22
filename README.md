# Deck of Many Colors — Personal Fan Reference

A 104-card miniature painting scheme deck for **Christopher** (52 Fantasy, 52 Sci-Fi), inspired by Ninjon's *Deck of Many Colors*.
**Not affiliated** with Ninjon, Monument Hobbies, The Army Painter, AK Interactive, Privateer Press, or Two Thin Coats.

**Primary paint brand: Pro Acryl (PRO).** Every swatch leads with a Pro Acryl match, code, and mix ratio where one applies. AK, TAP, P3, and TTC matches are listed where they exist (cards F01–F06 and S01–S06 so far).

Live site: https://kudzooman2025.github.io/deck-of-many-colors/

## What's here

| File | Purpose |
| --- | --- |
| `index.html` | Deck viewer: filter by theme, draw a random card, tap any card for hex codes, Pro Acryl matches, mix ratios, notes, and secondary brands. Print lays out the visible cards with their paint lists. |
| `gallery.html` | Art gallery: every card's art front beside its layout preview, with theme filter, title/ID search, and a fullscreen lightbox. |
| `cards.json` | The card data you edit. One entry per card with five colors (shade, base, accent, light, detail), each with a hex value and paint matches. |
| `cards.js` | Generated from `cards.json` by `build.py`. Both pages load this file, so they work when opened straight from disk as well as when served. |
| `build.py` | Regenerates `cards.js` and validates the data (unique IDs, five colors per card, a PRO match on every color, art file present). |
| `*-front.jpg` | Art front for each card, 540×720. |
| `*-layout.jpg` | Layout preview (front plus paint back) for each card. |

## Editing cards

1. Edit `cards.json`.
2. Run `python3 build.py`.
3. Commit both `cards.json` and `cards.js`.

`build.py` drops any paint entry whose `confidence` is `placeholder` and any internal workflow fields, so a full pipeline export can be dropped in as-is.

## Viewing

Open `index.html` or `gallery.html` directly in a modern browser, or visit the GitHub Pages site. No build step or network connection is needed to view the deck.

For printing from the viewer, turn on **Background graphics** in the print dialog so the swatches keep their color.

Paint matches are approximate personal references, not measured conversions. Verify against your own pots under your lighting.
