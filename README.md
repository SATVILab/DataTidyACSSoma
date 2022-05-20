# DataTidyACSClinical

The goal of `DataTidyACSSoma` is to provide easy, documented access to the ACS SOMALogic dataset.

The processing is actually performed in `FredHutch/TuberculomicsCompendium`, but that package is at present restricted to Tuberculomics members and so we make available the `soma_data_tidy` dataset from there here for in-SATVI use.

## Installation

To install the latest version of `DataTidyACSSoma` from [GitHub](https://github.com/), run the following:

``` r
if (!requireNamespace("remotes", quietly = TRUE)) install.packages("remotes")
remotes::install_github("SATVILab/DataTidyACSSoma")
```

## Data sets

The following datasets are available:
```{r , results = "asis", echo = FALSE}
data_tbl <- tibble::tibble(
  Dataset = c(
    "data_tidy_soma"
  ),
  Description = c(
    "Full ACS SOMALogic dataset"
  )
)
pander::pandoc.table(data_tbl)
```

Use `?DataTidyACSSoma::<dataset_name>` to see documentation for each dataset.

## Project structure

The data are processed using `Rmd` files inside `data-raw/`.