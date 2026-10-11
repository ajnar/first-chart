# first-chart

An IBCS-style revenue chart for a Kenyan SACCO, built with [Observable Plot](https://observablehq.com/plot/) in a single HTML file. No framework, no build step.

- **Top chart:** monthly actual revenue (dark grey) against prior year (light grey) and budget (outlined), in KES millions.
- **Bottom chart:** actual minus budget per month. Green bars are above budget, red bars below.
- **Title:** calculated from the data, so it states the finding rather than naming the metric.

The figures in `data/revenue.csv` are illustrative, not real SACCO results.

## Run it

Browsers block loading the CSV from a page opened directly from disk, so serve the folder with any static server:

```sh
npx serve .            # or: python -m http.server 8000
```

Then open the URL it prints.

## Files

| File | Purpose |
|---|---|
| `index.html` | Page, styles and chart code. D3 and Plot load from jsDelivr. |
| `data/revenue.csv` | `month, actual, budget, prior_year` for 2026, KES millions |
