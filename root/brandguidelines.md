# Rithim Corporate Brand Guidelines

**Version:** 2.0 | **Issued:** 28 May 2026

> These guidelines apply to ALL publications — HTML, slides, documents, PDFs, reports, and any other output. No exceptions unless explicitly overridden.

---

## Company Identity
**Brand Name:** Rithim  
**Brand Anchor Color:** Forest Green (`#031c11`) — represents sophistication, trust, and environmental consciousness.

---

## Color Palettes

### Dark Theme *(On-screen / Digital Only)*
| Role                | Hex       | Name         |
|---------------------|-----------|--------------|
| Primary Background  | `#031c11` | Evergreen     |
| Secondary Background| `#0a2818` |              |
| Elevated Card       | `#0f3020` |              |
| Primary Text        | `#FFFFFF` | White         |
| Secondary Text      | `#BECAD1` |              |
| Muted Text          | `#7A9099` |              |
| Borders             | `#4B5B65` |              |

### Light Theme *(Reports & Printed Documents — **Mandatory**)*
| Role                | Hex       | Name            |
|---------------------|-----------|-----------------|
| Page Background     | `#EEF3F0` | Evergreen Wash   |
| Surface             | `#DDE8E2` |                 |
| Card                | `#FFFFFF` | White            |
| Primary Foreground  | `#031c11` | Evergreen        |
| Secondary Foreground| `#2D4A38` |                 |
| Muted Foreground    | `#5A7868` |                 |
| Borders             | `#A8C4B4` |                 |

### Data Visualization *(Charts & Graphs Only — max 3–4 colors per chart)*
| Color        | Hex       |
|--------------|-----------|
| Royal Blue   | `#4169E1` |
| Hot Magenta  | `#FF006E` |
| Lemon Yellow | `#FFED4E` |
| Neon Lime    | `#00FF41` |
| Bright Red   | `#FF4365` |
| Soft Purple  | `#A78BFA` |

### RAG Status Indicators *(Traffic Light Standard — status use only)*
| Status             | Hex       |
|--------------------|-----------|
| Red (Critical)     | `#CC2200` |
| Amber (At Risk)    | `#FF8C00` |
| Green (On Track)   | `#228B22` |

### Interactive & Highlights
| Role         | Hex       |
|--------------|-----------|
| CTA Dark     | `#FFED4E` |
| CTA Light    | `#031c11` |
| Hover States | `#FFE066` |
| Focus Rings  | `#5B7FFF` |

---

## Logo Rules
- Use the Rithim corporate logo **unmodified**.
- **No** recolouring, cropping beyond the original file, stretching, or overlays.
- **No** text wordmark substitutions.

### Sizing
| Context     | Size            |
|-------------|-----------------|
| Header      | 1.1–1.3 inches  |
| Cover Page  | 2.0–2.5 inches  |

---

## Documentation Standards
- **Theme:** Light theme exclusively for all reports and PDFs.
- **Date Format:** DD Month YYYY (e.g., `28 May 2026`) on cover page and header.
- **Undated reports are not approved for distribution.**

---

## Implementation Rules
- Data viz colors are reserved for **charts and graphs only** — never for UI backgrounds or large text.
- RAG colors are exclusively for **status indicators**.
- Maximum **3–4 colors** per bar chart.
- **Colorblind accessibility required** — always pair colors with icons or labels.
- Do **not** use bright colors for large text blocks.

---

## Visual Output Skill
When generating any visual output — posters, banners, graphics, artwork, or static design assets — use the **`canvas-design` skill**. This applies to `.png` and `.pdf` visual outputs.

- Outputs: `.png` for digital, `.pdf` for print-ready.

### Standard Canvas-Design Prompt Prefix
Always prepend the following brand context when invoking `/canvas-design`:

```
Brand: Rithim. Anchor color: deep forest green (#031c11 — Evergreen).
Palette: backgrounds in #EEF3F0, surfaces #DDE8E2, headlines #031c11, accents #2D4A38.
Feel: sophisticated, trustworthy, environmentally conscious. Minimal, refined, corporate.
Typography: thin, design-forward fonts. Sparse text, visual-first.
<your specific design request here>
```

### Example
```
/canvas-design Brand: Rithim. Anchor color #031c11 Evergreen. Palette: #EEF3F0 backgrounds, #031c11 headlines, #2D4A38 accents. Feel: sophisticated, minimal, corporate. Create a poster for our annual investor report launch.
```
