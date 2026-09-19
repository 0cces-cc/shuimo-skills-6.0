# shuimo-6.0 — Two Ways a Photograph Becomes Ink

**Author · @0cces-cc**

[中文](README.md) · [日本語](README.ja.md) · [Ink Poster SKILL](skills/shuimo-ink-6.0/SKILL.md) · [Photo Graft SKILL](skills/shuimo-graft-6.0/SKILL.md) · [Archive](examples)

The same photograph can become a complete ink-poster painting, or extend into an ink painting while preserving the photograph's key elements. This repository holds two versions of a text-to-image Skill sharing one set of ink-generation standards.

- **shuimo-ink-6.0 (Ink Poster)** — repaint the source as one complete modern-ink poster. The photograph supplies facts, relationships and character; the finished work is painting through and through, with no photographic regions retained.
- **shuimo-graft-6.0 (Photo Graft)** — join the original photograph and newly painted ink into one work. A continuous real-photo anchor is preserved; a form from the photograph crosses the boundary, changes medium, and grows into an independently composed ink field.

| | Ink Poster | Photo Graft |
|---|---|---|
| Role of the photo | sole content source; the result is all painting | a protected photographic layer in the final work |
| Result | one complete modern-ink poster | real photograph + grafted ink as a single work |
| Invoke | `$shuimo-ink-6.0` | `$shuimo-graft-6.0` |

## Shared discipline

Decide first; send the model only what this image needs:

1. **Decisions before wording** — Ink Poster runs anchor → proposition → one authorial decision → expressive extension; Photo Graft fills an execution card in the order C → P → H → I → M: whole-picture composition C first, then the subject, zones P/H/I, the main exit and material placement M. Missing facts stay "unknown", never invented.
2. **Form first, material second, release last** (graft) — the interface is concrete: which form, through which edge, continuing in which direction. Direction, width, tonal weight and branching are preserved at the boundary; scaling, merging and tapering happen only deep inside the ink field.
3. **Five-section short prompt** — target 500–900 Chinese characters; one fact stated once; only the mechanisms chosen for this image.
4. **Single-variable correction** — locate the primary failure, replace only that section; never append patches to the prompt tail.

## Ink standards at a glance

- warm-white xuan paper `#f7f4ea`, visible fiber grain, never aged;
- five ink values (burnt `#1a1712` / dense `#2e2a22` / heavy `#57503f` / diluted `#8f8671` / clear `#c9bea4`); pure black forbidden;
- full wet–dry value hierarchy, layered wet → light → heavy → dense → burnt;
- long continuous brush gestures; 2–8 decisive strokes build the subject; dry brush and flying white;
- three grain layers (paper fiber / ink grain / mineral gold) with a single grain focus;
- **mineral gold**: localized deposits that cluster → transition → scatter, coarse and fine particles mixed, gaps showing ink beneath — never glitter;
- one mineral accent color carrying structure (cinnabar, azurite, mineral green, gamboge, ochre, rouge, indigo); warm-neutral ink stays dominant;
- modern editorial-illustration character; no antique imitation, inscriptions or seals.

Full rules live in each skill's [references/](skills/shuimo-ink-6.0/references). **Both skills share one identical `ink-standard.md`** (duplicate copies; the copy in shuimo-ink-6.0 is the source of truth — sync edits to both). Graft-specific rules (photo protection, the C → P → H → I → M execution order, cross-boundary handoff) live in the graft skill's own SKILL.md and handoff.md.

## Install

```bash
git clone https://github.com/0cces-cc/shuimo-6.0.git
cp -R shuimo-6.0/skills/* ~/.codex/skills/   # Claude-family hosts: ~/.claude/skills/
```

Restart the host if the Skills do not appear.

## Usage

```text
Use $shuimo-ink-6.0 to repaint this photo as one complete ink poster.
```

```text
Use $shuimo-graft-6.0 to graft this photo into ink. Keep the trunk-and-eaves relationship.
```

A concise Chinese creative note accompanies the image by default; prompt-only delivery is available on request.

## Repository layout

```text
shuimo-6.0/
├── README.md / README.en.md / README.ja.md
├── LICENSE                 # CC BY-NC 4.0
├── examples/               # archive: source → decision record → result
└── skills/
    ├── shuimo-ink-6.0/     # Ink Poster: full repaint
    │   ├── SKILL.md
    │   └── references/     # ink-standard / method / review
    └── shuimo-graft-6.0/   # Photo Graft
        ├── SKILL.md
        └── references/     # ink-standard / handoff / compiler / review
```

## About photos

Supplied photos are used only as references for the current generation task. They are not browsed, shared, re-uploaded or saved elsewhere unless explicitly requested.

## License

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) — attribution, non-commercial. Commercial use requires the author's prior written permission.
