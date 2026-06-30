# Ian Xiaohei Illustrations

> Turn the judgments, processes, states, and metaphors in English articles into white-background, hand-drawn, slightly absurd but clean inline illustrations.
>
> 16:9 landscape | Xiaohei IP | pure white hand-drawn style | a few red/orange/blue English annotations | Codex Skill

---

> **Unofficial English edition.** This repository is an English translation and adaptation of Ian's original [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations). It is not affiliated with or endorsed by Ian. The skill, the recurring **"Xiaohei"** character, and the example illustrations were created by **Ian** ([@helloianneo](https://github.com/helloianneo)) and remain copyright © Ian, distributed under the MIT License. Only the documentation has been translated to English and the default behavior changed to target English-language articles. See [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md) for full terms and attribution.

---

## What is this repo

Ian Xiaohei Illustrations is a Codex Skill that guides an AI Agent to generate inline illustrations for English articles, posts, blogs, Notion documents, and methodology content.

It is not a generic illustration prompt, nor a PPT infographic template. Its core goal is to first understand the cognitive anchor points in the article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explainer image.

The default visual IP is "Xiaohei": a solid black character with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, and not decoration standing in the corner — it's an absurdist worker earnestly participating in the system at work.

In one sentence: **make the AI not just "add an illustration," but actually draw out one key cognitive move from the article.**

---

## Who is this for

Especially good for:

- People writing English articles who need inline illustrations and figures
- People producing knowledge content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want an illustration style that's lighter, weirder, and more personally distinctive than a PPT infographic
- People using Codex for content production who want a consistent, reusable visual language

Not a good fit for:

- People who want commercial illustration, brand key visuals, or polished flat illustration
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute mascots, or sticker-pack styles
- People who want to cram large blocks of body text, long explanations, or an entire course page into a single image
- People who need strictly editable vector source files

---

## What it produces

Produces by default:

- 16:9 landscape inline illustrations
- A shot list of 4-8 images per article
- For each image: theme, core meaning, structure type, what Xiaohei is doing, and suggested English annotation text
- Final PNG images, saved to the workspace under `assets/<article-slug>-illustrations/`

Does not produce by default:

- PPTX / PDF / Keynote
- Editable SVG / HTML / Canvas graphics
- Commercial posters or cover key visuals
- Text-heavy infographics

---

## Visual style

This skill uses Ian's "Xiaohei absurdist inline illustration" style by default:

- Pure white background — no paper texture, no beige, no shadows, no gradients
- Black hand-drawn line art, thin lines, slight wobble
- Generous negative space, with the subject occupying only about 40%-60% of the frame
- A few handwritten English annotations in red, orange, or blue
- Each image expresses exactly one core action, structure, state, or metaphor
- Xiaohei must be involved in the core action — never just decoration
- Absurd, creative, and clean — but never cutesy or childish

---

## Example results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sorting by Purpose

![Sorting by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish, Many Uses

![One Fish, Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style-calibration examples, not composition templates. When using the skill, reinvent the metaphor from the current article — don't copy the objects or composition of older examples.

---

## Installation

Clone the repo:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill into your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Once installed, use it in Codex like this:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei absurdist inline illustrations for this English article.
```

---

## How to use it

### Planning illustrations only

```text
Use $ian-xiaohei-illustrations — don't generate images yet.
Please analyze where this article below would benefit from illustrations, and output a shot list of about 5 images.
For each image, specify: where it goes (after which paragraph), theme, core meaning, structure type, what Xiaohei is doing, and suggested English annotation text.

<paste article>
```

### Generating inline illustrations directly

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei absurdist inline illustrations for the article below.
Requirements: 16:9 landscape, pure white background, black hand-drawn line art, a few handwritten English annotations in red/orange/blue.

<paste article>
```

### Generating a single image for one concept

```text
Use $ian-xiaohei-illustrations to generate one inline illustration for: "Trust isn't declared — it's built piece by piece, like laying down evidence one block at a time."
The image should be absurd but clean, and Xiaohei must carry the core action.
```

### Removing a title or incorrect text from an image

```text
Use $ian-xiaohei-illustrations to help me edit this image — remove the "Flowchart" title in the top-left corner, and keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

This skill's process is:

1. Read the article, Markdown, Notion content, screenshots, or a topic given by the user
2. Extract the core arguments, cognitive turning points, process structures, and passages worth visualizing
3. Output a shot list first: each image picks exactly one cognitive anchor point
4. Choose a structure type for each image: workflow, partial system view, before/after comparison, character state, conceptual metaphor, layered method, map/route, or short comic panel
5. Reinvent a low-tech, absurd but coherent physical metaphor
6. Have Xiaohei carry out the core action
7. Call the image model separately for each illustration
8. Check against the QA checklist: white background, negative space, Xiaohei's action, English annotations, no PPT feel, no reuse of old examples
9. Save the final PNGs and report their purpose and paths

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The part that actually needs to be installed into Codex is the subdirectory:

```text
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub-facing documentation.

---

## Notes

- The shorter the text in an image, the more stable the result.
- Each image should tell exactly one core structure — don't turn the article into an instruction manual.
- Xiaohei must carry the core action; if the image still makes complete sense with Xiaohei removed, Xiaohei is too decorative.
- The example images are only for calibrating line density, negative space, color restraint, and how Xiaohei participates — don't copy their composition.
- AI image models can produce typos, hallucinated labels, style drift, or extraneous titles — check the output after generation.
- If the text comes out badly garbled, reduce the amount of annotation text and regenerate.

---

## Related projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — A Skill for generating Chinese hand-drawn, technical PPT-style page illustrations
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — A curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — A guide to building a personal knowledge base with Obsidian + Claude AI

---

## About the author

**Ian** — Product designer / one-person-company practitioner / AI builder

Building a one-person company with an AI team.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## Keep exploring

This Xiaohei illustration skill is just one small tool in the personal production system I'm building with AI.

If you're also using AI for content, knowledge bases, workflows, or productization, feel free to check out my website: [www.ianneo.xyz](https://www.ianneo.xyz).

If you'd just like to observe for now, follow me on [X/Twitter](https://x.com/ianneo_ai).

If you'd like to learn about the Indie Builders Club, add me on WeChat: `ianneoxyz`, with the note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian's WeChat QR code" width="120">
</p>

If scanning the code isn't convenient, you can also search for `ianneoxyz` on WeChat.

---

## License

MIT License. See [LICENSE](LICENSE).
