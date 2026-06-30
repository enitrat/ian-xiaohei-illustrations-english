---
name: ian-xiaohei-illustrations
description: Generate Ian-style in-article illustrations for English text. Use when the user asks to generate "absurdist," "Xiaohei," "hand-drawn," "in-article illustration," "article illustration," "illustration suggestions," "shot list," "remove title / revise image" tasks for an English article, post, blog, Notion doc, workflow document, methodology, process, structure, state, metaphor, or viewpoint; defaults to using the Xiaohei IP, pure white hand-drawn style, a few red/orange/blue annotations, and a clean yet wildly imaginative visual style.
---

# Ian's Xiaohei Absurdist In-Article Illustrations

## Core Positioning

Design and generate 16:9 landscape in-article illustrations for English articles. The goal is not commercial illustration, slide-deck infographics, or cute cartoons, but turning the article's key judgments, processes, structures, states, or metaphors into a clean, absurdist, creative, legible illustration that explains rather than instructs.

The default visual IP is "Xiaohei": a solid black body, white dot eyes, thin legs, a blank expression, earnestly doing something absurd yet logically sound. Xiaohei must take part in the core action of the scene — it cannot just stand to the side as decoration.

## Read These References First

Read them as needed for the task at hand — don't stuff them all into context at once:

- `references/style-dna.md`: style DNA, colors, text, and taboos.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action library, and taboos.
- `references/composition-patterns.md`: structure types, original metaphor methods, and anti-repetition rules.
- `references/prompt-template.md`: prompt template for generating a single image.
- `references/qa-checklist.md`: post-generation checks and iteration rules.
- `assets/examples/`: for occasional visual calibration only — not part of the default generation path. Do not copy the composition, objects, or annotations from these examples.

## Workflow

### 1. Digest the Article Text

First read the article, link, Notion page, Markdown file, or screenshot content the user provides. Extract:

- What the core argument is
- Which paragraphs carry a cognitive turning point
- Which content is suited to being explained with an image
- Which parts are better left as text, not illustrated

Don't distribute illustrations evenly. Prioritize "cognitive anchor points," such as: a core judgment, two breakpoints, an input-output loop, a fork in the flow, a before/after comparison, getting multiple uses out of one resource, a hand-off path, a common pitfall, or a change in a character's state.

### 2. Propose an Illustration Strategy First

If the user is just asking to "analyze how to illustrate this" or "think about where illustrations are needed," give a shot list first. For each image, clearly note:

- Which paragraph it follows
- The image's subject
- The core meaning
- The structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested English annotation text

Default to 4-8 images. For short articles, 1-3; even for long articles, don't readily exceed 9. Use only as many as needed — avoid turning the article into a picture book.

### 3. Single-Image Generation

If the user explicitly asks to "generate / produce / make images / please generate," don't stop to wait for confirmation — use the built-in `image_gen` to generate each image individually. Do not combine multiple images into one.

Each image should convey only one core structure. The prompt must include:

- 16:9 landscape in-article illustration for an English article
- Pure white background
- Black hand-drawn line art
- A few short English handwritten annotations in red/orange/blue
- Generous white space
- Xiaohei as the core subject of the action
- No slide-deck style, commercial illustration, childish cuteness, complex architecture diagrams, or upper-left-corner-style titles

Don't replicate past examples. The examples only provide a reference for style density and how Xiaohei participates — they must not be directly reused as ready-made compositions such as "conveyor belt breakpoint / Xiaohei pulling a line / material fish / stamping toolbox / common pitfall path," unless the user explicitly asks to replicate a specific image. Each time, reinvent a strange but logically sound metaphor from the current article.

### 4. Check and Iterate

After generating, check against `references/qa-checklist.md`. If any of the following issues appear, prioritize regenerating or doing a partial edit:

- Xiaohei is merely decorative
- The composition is too crowded
- It looks too much like a flowchart/slide deck
- Too much text or serious typos
- An upper-left-corner title like "Common Pitfalls / Flowchart / System Architecture Diagram" appears
- The art style is too cute, childish, or stiff
- The background isn't a clean white

### 5. Save and Deliver

If the user is working within a workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files — don't overwrite existing assets unless the user explicitly asks for a replacement.

## Output Conventions

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- The purpose of each image
- The save path
- Which images are the strongest, and which are optional

Don't write lengthy explanations of style theory — let the images speak for themselves.
