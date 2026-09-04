# Art — sources

`Preview-source.png` — the generated banner, **1672 x 941, 1897 KB**. `Mod/About/Preview.png` is
derived from it: scaled to **896 x 504** with the mod name and a summary line engraved over the
dark upper-left corner, 587 KB. The source is only 0.06% off 16:9, so nothing is cropped away.

`ModIcon-source.png` — **1254 x 1254, 1088 KB**, scaled to **128 x 128** for `Mod/About/`.

Both files are rebuilt by `_tools/build-about.sh`, which renders `_tools/preview.html` in headless
Chrome at exactly 896 x 504 — the text is therefore composed at its final size and its glyphs are
never resampled — and re-encodes through ffmpeg, because Chrome's own PNG came out at 1.2 MB.
Always rebuild from these sources, never from an already-reduced copy.

## The icon departs from the style guide, on purpose

`STYLE_RIMWORLD.md` asks for a matte, muted pictogram at the game's camera angle, with no face and
nothing in motion. This icon is none of that: a winking face, a gear and a wrench, speed lines, a
heavy outline and saturated orange throughout. **It is kept deliberately** — this is a note so that
a later pass over the repository's showcases does not read it as an oversight and regenerate it.

The banner, by contrast, follows the guide as written.

RimWorld never reads this folder.
