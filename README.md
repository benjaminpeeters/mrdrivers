# Create GDP and Population Scenarios

R package **mrdrivers**, version **3.0.2**

[![CRAN status](https://www.r-pkg.org/badges/version/mrdrivers)](https://cran.r-project.org/package=mrdrivers)  [![R build status](https://pik-piam.github.io/mrdrivers/workflows/check/badge.svg)](https://pik-piam.github.io/mrdrivers/actions) [![codecov](https://codecov.io/gh/mrdrivers/branch/master/graph/badge.svg)](https://app.codecov.io/gh/mrdrivers) [![r-universe](https://pik-piam.r-universe.dev/badges/mrdrivers)](https://pik-piam.r-universe.dev/builds)

## Purpose and Functionality

Create GDP and population scenarios
    This package constructs the GDP and population scenarios used as drivers in both the REMIND and MAgPIE models.

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- # mrdrivers -->
<!-- badges: start -->
<!-- [![lucode2-check](https://github.com/pik-piam/mrdrivers/actions/workflows/lucode2-check.yaml/badge.svg)](https://github.com/pik-piam/mrdrivers/actions/workflows/lucode2-check.yaml) -->
<!-- [![Lifecycle: stable](https://img.shields.io/badge/lifecycle-stable-bright_green.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable) -->
<!-- [![Codecov test coverage](https://codecov.io/gh/pik-piam/mrdrivers/branch/main/graph/badge.svg)](https://app.codecov.io/gh/pik-piam/mrdrivers?branch=main) -->
<!-- badges: end -->
<!-- The goal of **mrdrivers** is to handle the construction of GDP, GDP per capita, Population and Urban Population share scenarios: all of which are important drivers to the REMIND and MAgPIE models. -->
<!-- ## Installation -->
<!-- ```{r, eval=FALSE} -->
<!-- # From the PIK rse-server -->
<!-- install.packages("mrdrivers", repos = "https://rse.pik-potsdam.de/r/packages") -->
<!-- # or from Github -->
<!-- remotes::install_github("pik-piam/mrdrivers") -->
<!-- ``` -->

## Framework

This package depends upon the
[madrat](https://github.com/pik-piam/madrat#readme) and
[magclass](https://github.com/pik-piam/magclass#readme) packages. It
integrates into the madrat framework and is structured accordingly. It
mainly uses magpie objects (from the magclass package). For more
information on madrat or magclass, please visit the respective github
repositories ([madrat](https://github.com/pik-piam/madrat#readme),
[magclass](https://github.com/pik-piam/magclass#readme)).

## Functions

The key `madrat::readSource()` and `madrat::calcOutput()` functions
provided by this package are listed below.

readSource:

    #> [1] "readWDI"            "readIMF"            "readEurostatPopGDP"
    #> [4] "readUN_PopDiv"      "readPEAP"           "readSSP"           
    #> [7] "readMissingIslands" "readJames2019"

calcOutput:

    #> [1] "calcGDP"        "calcGDPpc"      "calcPopulation" "calcLabour"    
    #> [5] "calcUrban"

## Scenarios

The current default scenarios returned for all drivers (i.e. GDP, GDP
per capita, Population, Labour, and Urban Population Share) are:

- the SSPs, i.e. SSP1-5

- the SDPs, i.e. SDP, SDP_EI, SDP_RC, and SDP_MC

- SSP2EU

see `vignette("scenarios")` for more information on available scenarios
and references of the default scenarios.

## Installation

For installation of the most recent package version an additional repository has to be added in R:

```r
options(repos = c(CRAN = "@CRAN@", pik = "https://rse.pik-potsdam.de/r/packages"))
```
The additional repository can be made available permanently by adding the line above to a file called `.Rprofile` stored in the home folder of your system (`Sys.glob("~")` in R returns the home directory).

After that the most recent version of the package can be installed using `install.packages`:

```r 
install.packages("mrdrivers")
```

Package updates can be installed using `update.packages` (make sure that the additional repository has been added before running that command):

```r 
update.packages()
```

## Tutorial

The package comes with a vignette describing the basic functionality of the package and how to use it. You can load it with the following command (the package needs to be installed):

```r
vignette("scenarios") # Scenarios
```

## Questions / Problems

In case of questions / problems please contact Johannes Koch <jokoch@pik-potsdam.de>.

## Citation

To cite package **mrdrivers** in publications use:

Koch J, Soergel B, Leip D, Benke F, Dietrich J (2024). _mrdrivers: Create GDP and Population Scenarios_. R package version 3.0.2, <URL: https://pik-piam.github.io/mrdrivershttps://github.com/pik-piam/mrdrivers>.

A BibTeX entry for LaTeX users is

 ```latex
@Manual{,
  title = {mrdrivers: Create GDP and Population Scenarios},
  author = {Johannes Koch and Bjoern Soergel and Deborra Leip and Falk Benke and Jan Philipp Dietrich},
  year = {2024},
  note = {R package version 3.0.2},
  url = {https://pik-piam.github.io/mrdrivers},
  url = {https://github.com/pik-piam/mrdrivers},
}
```
