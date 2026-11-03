# ReUp substance dataset

Onset, come-up, peak, offset and total-duration ranges, redose waits and combination risks
for 12 substances commonly taken at music festivals, plus 9
prescription medicine classes. Every figure cites its source. It is the dataset behind the
ReUp harm-reduction app for Apple Watch and iPhone, published here so anyone can check it,
correct it and reuse it.

**Version 0.3.0**, published 2026-11-03.

> Timings are typical ranges, not guarantees, and are not medical advice. People vary, and
> doses, purity and mixing change everything. If someone is in trouble, get medical help.

## Files

| File | What it is |
|---|---|
| `substances.json` | The built dataset, exactly as the app ships it. All times are in minutes. |
| `schema/substance-dataset.schema.json` | JSON Schema for `substances.json`. |
| `build/research.json` | Hand-curated figures in each source's own units, with the page URL next to each. |
| `build/tripsit-provisional.json` | Onset, duration and combination ratings taken from TripSit's open data. |
| `CREDITS.md` | Every source, its credit line and its terms. |
| `LICENSE.md` | How the dataset is licensed. |

`substances.json` is built from the two files in `build/`: TripSit figures first, then
PsychonautWiki, DanceSafe and study figures merged over them. Phase durations (onset,
come-up, peak, offset) run one after another; `totalMinutes` and `minRedoseMinutes` are
measured from the time taken. A missing field means no source gave a figure.

## Licence

The dataset is shared under
[Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
(full text in `LICENSE-CC-BY-SA-4.0.txt`), because it includes figures from PsychonautWiki,
which is CC BY-SA 4.0.

**Except TripSit figures.** Figures from TripSit remain under TripSit's own terms: free for
non-commercial use with credit and a link to https://tripsit.me. They are marked with the
`tripsit` source id. See `LICENSE.md`.

## Credit

When you reuse the dataset, credit "ReUp dataset" with a link to this repository, link the
licence, and keep the source credits in `CREDITS.md`.

## Corrections

Spotted a figure that doesn't match its source, or a source we should be using? Open an
issue with the substance, the figure and a link to the source. This repository is exported
from the app's own repository, so fixes are made there and published here in the next version.
