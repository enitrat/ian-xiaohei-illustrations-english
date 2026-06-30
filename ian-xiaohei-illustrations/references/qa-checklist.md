# QA Checklist

## Must-pass items

- It's 16:9 landscape.
- The background is a clean white base.
- Xiaohei is present.
- Xiaohei carries the core action, not just decoration.
- It doesn't replicate the composition of an old example, but generates a new metaphor for the current article.
- The scene is bizarre, creative, and interesting.
- Clean and uncluttered, with the subject taking up no more than about 60% of the frame.
- One image conveys only one core structure.
- English annotations are few, short, and legible.
- Orange is used only for the main path or arrows.
- Red is used only for key points, problems, warnings, or results.
- Blue is used only for supplementary notes, feedback, or system status.

## Failure signals

If any of the following occur, regenerate or do a partial edit:

- A title like "Common pitfalls / Workflow / System architecture diagram / Roadmap" appears in the top-left corner.
- Xiaohei looks like a mascot, an emoji/sticker, or a cute cartoon character.
- The scene looks like a slide deck, course courseware, or a formal flowchart.
- Too many elements, too many arrows, too many nodes.
- The text turns into long explanatory passages.
- The background has paper texture, shadows, gradients, beige tones, or noise.
- A real UI screenshot or tech-style interface appears.
- The text contains serious typos or the annotations are illegible.
- The scene feels too rigid, lacking an absurd metaphor.
- It's too similar in composition to an old example in `assets/examples/`.

## Iteration methods

- Too plain: make Xiaohei the subject of the action, and add a metaphor that's strange but coherent.
- Too complex: cut nodes, keeping only one action and 3-5 short annotations.
- Too cute: emphasize deadpan, blank serious expression, not cute, not mascot.
- Too PPT-like: remove titles, borders, neat grids, and excess arrows, and turn it into a hand-drawn scene instead.
- Too similar to an old example: keep the core meaning, but swap out the main object and Xiaohei's action.
- Text errors: prefer a partial edit first; if there are too many errors, regenerate and reduce the number of annotations.

## Delivery judgment

A high-quality image should make the reader think "that's a bit odd" at first, then understand the structure within one second.

If it looks like a tutorial page at first glance, rather than a bizarre product sketch on a blank sheet of paper, it doesn't pass.
