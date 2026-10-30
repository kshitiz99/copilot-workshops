# GitHub Copilot Workshops

Self-paced, step-by-step GitHub Copilot workshops, published with GitHub Pages.

**Live site:** https://kshitiz99.github.io/copilot-workshops/

| Workshop | Link |
| --- | --- |
| Explore agentic & autonomous workflows | https://kshitiz99.github.io/copilot-workshops/explore-automations/ |

## Structure

```
index.html                         Landing page listing all workshops
theme.css                          Shared design tokens
assets/                            Shared images (mascot)
<workshop-slug>/index.html         One self-contained workshop page
<workshop-slug>/assets/            Screenshots and recordings for that workshop
```

## Add a new workshop using the same template

1. Copy `explore-automations/` to a new folder, for example `my-new-workshop/`.
2. In the new `index.html`:
   - Update `<title>`, the meta description, the topbar kicker (duration) and `<h1>`.
   - Edit the rail `<ol id="clSteps">`: one `<li>` per step, with `data-target` matching a step `id`.
   - Edit each `<article class="cl-step" id="..." data-minutes="...">`. The progress bar and
     "minutes left" are calculated from `data-minutes`.
   - Change `STORE_KEY` in the script so saved progress does not clash with other workshops.
3. Reusable building blocks inside a step:
   - `.sowhat` callout, `.crit-grid` / `.crit-card` cards, `.checkpoint` aside
   - `details.stage` for numbered, collapsible sub-steps
   - `.tpl > textarea.sc-text` or `blockquote.mcp-lab-prompt` for prompts (a **Copy** button is added automatically)
   - `figure.shot` for screenshots and `<video>` recordings
4. Add a card for the workshop to the root `index.html`.

Deep links work with `#<step-id>`, for example `.../explore-automations/#round2`.

## Maintainer

Created and maintained by [Kshitiz](https://www.linkedin.com/in/kshitiz-agarwal-5b7950155/).
DM me for any issues.
