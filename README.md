# CV

Static personal site hosted on GitHub Pages from the `main` branch.

Live at https://oliviavoster.github.io/CV/

## Layout

Pages serves the repo root, so whatever sits at the root **is** the live site.

| Path | Serves at | Purpose |
|---|---|---|
| `index.html` | `/CV/` | The CV — the live site |
| `styles.css` | | All styling for it |
| `assets/` | | Images |
| `.nojekyll` | — | Tells Pages to serve files as-is instead of running Jekyll |

## Building a new version without touching the live one

Put the work-in-progress in its own directory, for example `v2/`, keeping its
own HTML, CSS and images inside it:

    v2/index.html
    v2/styles.css
    v2/assets/

It is live at `/CV/v2/` as soon as it is pushed, and the root stays exactly as
it is while you work. Nothing at the root is touched, so the live CV cannot
break.

When the new version is ready, promote it by moving its files up to the root,
replacing the current ones. Because each version keeps its files together, the
move needs no edits to any HTML — the relative paths still resolve.

## Editing

Edit, commit, push to `main`. Pages rebuilds automatically; the change is
usually live within a minute.

To preview locally, open `index.html` in a browser — there is no build step.
