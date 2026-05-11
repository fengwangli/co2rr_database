# CO2RR Database Demo

This repository contains a Quarto data page demo for CO2 reduction reaction
(CO2RR) experiment data. The site reads the local CSV file at
`resources/data/co2rr.csv` during rendering and generates interactive overview,
potential, and source visualizations.

## Pages

- `index.qmd`: overview charts for product counts and Faradaic efficiency vs
  current density.
- `potential.qmd`: potential-dependent scatter plots with filters for product,
  year, stability, potential type, marker size, and y-axis variable.
- `source.qmd`: source/reference-oriented scatter plot by year, with color
  mapping and click-to-copy reference support.

## Local Rendering

Install Quarto and the R packages listed in `DESCRIPTION`, then render the site:

```powershell
quarto render
```

To view pages that use Observable JavaScript, serve the rendered `_site`
directory through a local web server instead of opening HTML files with
`file://` URLs:

```powershell
quarto preview
```

or:

```powershell
python -m http.server 8000 -d _site
```

## Dependencies

R dependencies are tracked in `DESCRIPTION`. The project does not require an
external data API token or `renv.lock`.
