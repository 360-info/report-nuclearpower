# `/data`

## `irena-src-*.csv`

These are tables downloaded from [IRENASTAT](https://pxweb.irena.org/pxweb/en/IRENASTAT):

* Installed electricity capacity by country/area (MW) by Country/area, Technology, Grid connection and Year
* Electricity generation (GWh) by Country/area, Technology, Grid connection and Year

They have been split up by grid status (on-grid and off-grid) in order to keep under IRENASTAT's 100k record extraction limit. They are processed by [`index.qmd`](/index.qmd).

## `nuclear-commodity-*.csv`

Files relating to the trade analysis:

`nuclear-commodity-categories.csv`: a mapping of various nuclear commodities into broad categories. Provided by Nigel Marks at Curtin University.

`nuclear-commodity-centroids.csv`: a list of country centroid locations (using the largest polygon), from https://github.com/360-info/country-centroids

`nuclear-commodity-data.csv`: