# Frameworks
A repository of frameworks on mental models, business strategy, AI research, market trends and growth economics


Digital storytelling by [Dev](https://x.com/notesbydev), built from the analysis published on [@notesbydev](https://x.com/notesbydev).

Each article or thread on @notesbydev explains what is changing and why. Each page here tells that idea as a story through one framework:

1. **The framework explains the idea.** The idea is drawn in HTML and SVG as a framework: its parts, how they connect, and the flows and loops between them.
2. **The framework is interactive.** Click its different parts to see what happens:
   - what each part does, and what changes when it changes;
   - how it scales or grows;
   - how it applies to a real case, or to yours.
3. **Short captions.** Text only moves the story along. The framework does the explaining.

Live site: **https://hackrlife.github.io/Frameworks/**

Every page is labelled **Concept**. Pages are ideas and models, not working products, financial advice or medical advice. Views are Dev's own.

---

## Storytelling elements

Each page uses the elements that best tell its idea. Some combine several, but one central framework runs through the whole story.

| Element | What you can do with it |
|---|---|
| **Flow schematic** | The idea as nodes, arrows and loops. Click a node to see its role and what it drives, step through the flows, and switch between loops. |
| **Interactive data** | Charts drawn in code from real, sourced figures. Switch periods, editions, segments or regions, and hover for the exact figure and its source. |
| **Plan** | A staged plan or roadmap. Click a stage to see who acts, what they do, what to measure, and what it unlocks next. |
| **Wireframe** | A clickable sketch of the product, tool or system the idea points to. Click a screen or component to see what it does and which part of the idea it carries out. |

---

## Story beats

Every page follows the same seven beats. The section ids are fixed so that articles and threads can link straight to a beat.

| # | Beat | id | What happens |
|---|---|---|---|
| 1 | The problem | `problem` | What is changing or broken, in one screen |
| 2 | The framework | `framework` | The framework appears and builds up, part by part |
| 3 | Explore it | `explore` | Click the parts: roles, dependencies, flows and loops |
| 4 | Scale it | `scale` | Change the scale, stage or inputs and watch it grow, strain or break |
| 5 | Apply it | `apply` | Cases from the piece, then your own, ending in the finished application, system, plan or approach |
| 6 | Evidence and limits | `evidence` | What rests on which source, what is contested, and where the design goes beyond the evidence |
| 7 | Sources | `sources` | Every source, linked |

---

## Tracks

| Track | Day | Source piece | Usually built with |
|---|---|---|---|
| AI research | Mon, Sat | X article on a new AI paper | A flow schematic or wireframe of the solution built on the paper's key finding, plus an evidence map |
| Business strategy | Tue | Thread | A flow schematic of the value chain and growth loops, plus a plan for the growth framework |
| Economics | Wed | X article on a macroeconomic question | A flow schematic of the causal system, plus interactive data from official sources |
| Market trends | Thu | Thread | Interactive data: a code-built simulation of the trend from published report figures |
| Funding flows | Fri | Thread on startup and VC funding | Interactive data on capital by stage, sector and geography, plus a flow schematic of the cycle |
| Mental models | Sun | X article: *100 mental models from philosophy* | A flow schematic of the model, applied to everyday life and to your own situation |

---

## Repository layout

```
Frameworks/
├── README.md            this file
├── index.html           home page, generated from frameworks.json
├── frameworks.json      list of every page, newest first
└── YYYY-MM-DD-<slug>/
    └── index.html       one page per piece
```

- **Folder name:** the date of the source piece and a short lowercase slug with hyphens, e.g. `2026-10-25-dichotomy-of-control/`.
- **Page URL:** `https://hackrlife.github.io/Frameworks/YYYY-MM-DD-<slug>/`

### frameworks.json

```json
[
  {
    "date": "2026-10-25",
    "slug": "2026-10-25-dichotomy-of-control",
    "title": "The dichotomy of control",
    "track": "Mental models",
    "what": "Separate what is your own judgement and action from what is not, and put your effort only into the first.",
    "source_piece": "Mental model 1 of 100: Epictetus and the dichotomy of control (X article)"
  }
]
```

The root `index.html` is regenerated from this file each time a page is added. It lists every page with its date, title, track and one-line summary, and can be filtered by track.

---

## Build rules

- **One file per page.** Inline CSS, inline SVG and inline vanilla JavaScript, with no external scripts, libraries or fonts.
- **Readable without JavaScript.** The framework renders as static SVG first, and interaction is layered on top.
- **Built from the approved piece.** Every part, step, figure and example traces to the article or thread. The page adds no new analysis.
- **Every control does something.** Each click shows a part's role, a dependency, a trade-off, how the idea scales, or how it applies. Nothing is decorative.
- **Accessible.**
  - Works by keyboard and touch.
  - Every diagram has a text description.
  - Respects `prefers-reduced-motion`.
- **Responsive.** Works at phone width with no horizontal scroll, in light and dark mode.
- **Honest numbers.**
  - Real numbers come only from sources that were opened.
  - Derived numbers are computed in code and labelled as derived.
  - Invented examples and anything a slider produces are labelled *illustrative*.
  - Where a design goes beyond its evidence, the page says so.
- **Report data.** Pages cite every figure (report title, publisher, date, chart or table). They redraw charts from the published numbers, show only a selection that supports the argument, and never reproduce report pages, images or full datasets.
- **Private by design.** Nothing a reader types into a page is stored or sent.
- **Tested before publishing.** Each page is checked in a headless browser at phone and desktop width, in light and dark mode. Every control is clicked through, and the page must show no console errors.

---
