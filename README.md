# Accelarousal Study (NAT1) Methods

## Getting Started
### Prerequisites
- R (3.6.1)
- RStudio (1.2.5019)
- Required packages

### Installing R Packages
To install required R packages, run script `setup.R`.

## Folder Structure
- `data`: Raw and processed data.
- `plots`: Output plots of correlation matrices, clustering dendrogram, linear models, machine learning models.
- `outputs`: CSV/Text outputs.
- `settings`: Common setting of the project.
- `scripts`: Main script for analysis and data modeling.
- `utils`: Common ultility functions.

## Configuration
All global settings are placed in `settings/settings.R`.

### Analysis Timing Settings
The default time-series anlysis is using data of 30 seconds before to predict the class of next 5 seconds. You can change these values for different analysis.
```R
TIME_PREV_SECONDS <- 30  # [5, 10, 15, 30]
TIME_NEXT_SECONDS <- 5
```

### Plotly
As the project is using Plotly as a visualization tool, you can set up your Plotly account in `settings/settings.R`.
```R
PLOTLY_USERNAME <- "<Your Plotly Username>"
PLOTLY_API_KEY <- "<Your Plotly API Key>"
```

### Orca
The Plotly lib needs `orca` as an static image exporting backend. 
Follow instruction at https://github.com/plotly/orca for installation.

## Script set
### Correllation Analysis
- Run `scripts/correlation.R`
### Clustering
- Run `scripts/clustering.R`
### Linear Model
- Run `scripts/linearModel.R`


## Additional Tools
### Style Guide
http://jef.works/R-style-guide/

### Install Styler
In RStudio, run following commands:
```r
install.packages("styler")
```