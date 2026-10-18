# Frameworks
A repository of frameworks on mental models, business strategy, AI research, market trends and growth economics
# Frameworks

Interactive schematic decks by [Dev](https://x.com/notesbydev), built from the analysis published on [@notesbydev](https://x.com/notesbydev).

Each article or thread on @notesbydev explains what is changing and why. Each page here turns that idea into a model you can see and use: a deck of slides built around one flow diagram that first shows what the model is, and then lets you click through how to apply it to yourself.

Live site: **https://hackrlife.github.io/Frameworks/**

Every page is labelled **Concept**. Pages are ideas and models, not working products, financial advice or medical advice. Views are Dev's own.

---

## How a page gets made

Nothing here is written or built without Dev's sign-off, at two points.

1. **Idea.** Each morning, 2 or 3 ideas are proposed for that day's long piece. Dev approves one, edits one, or sets his own direction.
2. **Piece.** The approved idea is written as an X article (a Markdown file) or an X thread. Dev reads it.
3. **Approval.** Dev approves the written piece, or asks for changes and reads it again.
4. **Page.** Only then is the Frameworks page built, from the approved piece and only from what it says. It is published here and linked from the piece.

---

## Tracks

| Track | Day | Source piece | What the schematic shows |
|---|---|---|---|
| AI research | Mon, Sat | X article on a new AI paper | The solution built on the paper's key finding, each part tagged with the finding it rests on |
| Business strategy | Tue | Thread | The value chain, control points and growth loops behind a company's move or an industry shift |
| Economics and funding | Wed | X article on a macroeconomic question | The causal system: levers, who acts, loops, and where the evidence is strong or contested |
| Market trends | Thu | Thread | What is driving a market, with charts redrawn from published report figures |
| Economics and funding | Fri | Thread on startup and VC funding flows | How capital is moving by stage, sector and geography, and how a founder reads the cycle |
| Mental models | Sun | X article: *100 mental models from philosophy* | One philosopher's model, taken apart into its parts and flow, and applied to everyday life |

---

## The deck

Every page is one self-contained `index.html`. It shows one slide at a time, and one schematic runs through the whole deck.

### Navigation
- **Next** and **Back** buttons, the left and right arrow keys, swipe on touch, and progress dots with slide names.
- The URL follows the slide, so a link like `.../#apply` opens straight on that slide.

### Interaction
- The schematic is inline SVG: parts are nodes, connections are arrows, and loops are drawn as loops.
- The schematic is the control. Click or tap a node, arrow or loop (or focus it and press Enter) to open its panel.
  - **On the model slides**, the panel explains that part and shows its source.
  - **On the application slides**, the panel shows how to apply that part to yourself: what you do, the question to ask yourself, and an example.

### Slide sequence

The ids are fixed so that articles and threads can link to a slide.

| # | Slide | id | What it does |
|---|---|---|---|
| 1 | Title | `title` | Concept label, title, track, date, byline, link to the source piece |
| 2 | The model in one line | `what` | The whole schematic in outline, the model in one sentence, and its source |
| 3–5 | Build the model | `model`, `model-2`, `model-3` | The schematic assembles part by part; click each new part for its meaning and source |
| 6 | The flow | `flow` | Step through how a situation moves through the model; switch between loops where there are loops |
| 7 | Apply it to yourself | `apply` | The same schematic, now clickable for application |
| 8 | Scenarios | `scenarios` | Pick an everyday situation; the schematic re-routes and fills in for it |
| 9 | Your version | `yours` | Enter your own situation; the schematic fills with your words and gives your steps and a review question. Nothing is stored or sent. |
| 10 | Limits | `limits` | Where the model fails or is misused, and what is original versus a modern extension or this page's own design |
| 11 | Sources | `sources` | Every source, linked |

On Market trends pages, chart slides sit between `model` and `flow`. You can switch report editions or segments, and hover a point to see the exact figure and its citation.

---

## Repository layout

```
Frameworks/
├── README.md            this file
├── index.html           home page, generated from frameworks.json
├── frameworks.json      list of every page, newest first
└── YYYY-MM-DD-<slug>/
    └── index.html       one deck per piece
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
- **Readable without JavaScript.** Diagrams render as static SVG first and interaction is layered on top. Without JavaScript, the slides stack one under another with every panel's text visible.
- **Built from the approved piece.** Every part, step and example traces to the article or thread. The page adds no new analysis.
- **Every control does something.** Each click shows a part, a step, a dependency or an application; nothing is decorative.
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
- **Report data.** Market trends pages cite every figure (report title, publisher, date, chart or table). They redraw charts from the published numbers, show only a selection that supports the argument, and never reproduce report pages, images or full datasets.
- **Tested before publishing.** Each page is checked in a headless browser at phone and desktop width, in light and dark mode. Every slide and node is clicked through, and the page must show no console errors.

---

## Contributing

This is a personal project. Pages are added only after the source piece is approved. Corrections are welcome as issues: point to the page, the claim and the source.
