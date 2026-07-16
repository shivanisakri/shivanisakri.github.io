# shivanisakri.github.io

Personal site — air cushion vehicle dynamics, simulation, and flight test.
Live at **https://shivanisakri.github.io**

## Files

```
index.html      The whole site. Hero + About are always visible; everything
                else is an expanding panel: Dissertation, Experience,
                Projects, Publications, Skills, Engineering education.
css/style.css   All styling
img/            Photos. The four .jpg files are PLACEHOLDERS — overwrite
                them with your real photos, same filenames.
```

No build step, no framework, no dependencies. Edit the HTML, commit, done.

## Swapping in your real photos

The placeholders are named after what belongs there. Upload a file with the
**same name** and it drops in — no code to change:

| File | What goes here |
|---|---|
| `img/hovercraft-hero.jpg` | Best hovercraft photo, landscape/wide |
| `img/dissertation-01.jpg` | The prototype / the build |
| `img/dissertation-02.jpg` | A field test on the slope |
| `img/dissertation-03.jpg` | A plot: model prediction vs. measured test data |

Then rewrite the `<figcaption class="cap">` text under each one — they
currently say "caption me."

Resize photos to ~1600 px wide before uploading. A 6 MB phone photo makes the
page slow.

## The panels

Each section is a plain HTML `<details>` element. To make one open by default,
add the word `open`:

```html
<details class="panel" id="projects" open>
```

To add a section, copy a whole `<details class="panel">…</details>` block and
give it a new `id`.

## Using a video in the hero instead

In `index.html`, find the `HERO MEDIA` comment. Delete the `<img>` line,
uncomment the `<video>` block, upload `img/hovercraft.mp4`. Keep it under
~10 MB — GitHub Pages is not a video host. Bigger than that, use YouTube.

## Design notes

- Palette lives in `:root` at the top of `css/style.css`. Everything derives
  from those six values.
- The orange (`--signal`) is deliberately rare: figure labels, "active" status,
  and the open-panel marker only. If it shows up everywhere it stops meaning
  anything.
- Motion respects `prefers-reduced-motion`.
