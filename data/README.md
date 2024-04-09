# `/data`

## `irena-proportions.csv`, `irena-proportions-2022.csv`

Processed [IRENASTAT](https://pxweb.irena.org/pxweb/en/IRENASTAT) data indicating the amount and proportion of energy produced, and energy capacity developed, by nuclear, renewable and non-renewable sources. The `-[year]` variant contains only the latest year's data.

Columns include:

- `iso3_countrycode`: country's [ISO_3166-1_alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code
- `country`: country name
- `lat`: centroid latitude for map
- `lon`: centroid longitude for map
- `year`: year
- `[variable]_[measure]_[technology]`:
  - `variable`: either `amount` (in either GWh for power generated or MW for capacity established) or `prop` for the proportion
  - `measure`: either `totalgen.gwh` for power generated or `totalcap.mw` for capacity established
  - `technology`: either `nuclear`, `renewable` or `nonrenewable`

## `irena-proportions-global.csv`

## `irena-src-*.csv`

These are source data fils downloaded from [IRENASTAT](https://pxweb.irena.org/pxweb/en/IRENASTAT):

* Installed electricity capacity by country/area (MW) by Country/area, Technology, Grid connection and Year
* Electricity generation (GWh) by Country/area, Technology, Grid connection and Year

They have been split up by grid status (on-grid and off-grid) in order to keep under IRENASTAT's 100k record extraction limit. They are processed by [`index.qmd`](/index.qmd).

## `nuclear-commodity-*.csv`

Files relating to the trade analysis:

`nuclear-commodity-categories.csv`: a mapping of various nuclear commodities into broad categories. Provided by Nigel Marks at Curtin University.

`nuclear-commodity-centroids.csv`: a list of country centroid locations (using the largest polygon), from https://github.com/360-info/country-centroids

`nuclear-commodity-data.csv`: processed annual data from the Nuclear Trade Atlas