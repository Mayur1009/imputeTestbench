
## imputeTestbench

#### *Neeraj Bokde, <neerajdhanraj@gmail.com>, Marcus W. Beck, <beck.marcus@epa.gov>*

[![Travis-CI Build
Status](https://travis-ci.org/fawda123/imputeTestbench.svg?branch=master)](https://travis-ci.org/fawda123/imputeTestbench)

[![AppVeyor Build
Status](https://ci.appveyor.com/api/projects/status/github/fawda123/imputeTestbench?branch=master&svg=true)](https://ci.appveyor.com/project/fawda123/imputeTestbench)

[![Downloads from the RStudio CRAN
mirror](http://cranlogs.r-pkg.org/badges/grand-total/imputeTestbench)](https://CRAN.R-project.org/package=imputeTestbench)

This is the development repository for the imputeTestbench package. This
package provides a testbench for comparing imputation methods for
missing data in univariate time series.

The development version of this package can be installed from GitHub:

``` r
install.packages('devtools')
library(devtools)
install_github('neerajdhanraj/imputeTestbench', ref = 'development')
```

The current release can be installed from CRAN:

``` r
install.packages('imputeTestbench')
```

#### Basic use

The core function is `impute_errors()`. See the help documentation for
more details.

``` r
library(imputeTestbench)
a <- impute_errors(data = nottem)
a
```

    ## $Parameter
    ## [1] "rmse"
    ## 
    ## $MissingPercent
    ## [1] 10 20 30 40 50 60 70 80 90
    ## 
    ## $na.approx
    ## [1]  0.9126667  1.3668795  1.8426935  2.6618272  3.7385688  5.3712847  6.5980827
    ## [8]  8.3407465 10.6986736
    ## 
    ## $na.interp
    ## [1]  0.8216307  1.1131238  1.3823202  1.6205857  1.9014233  2.1002091  2.3966999
    ## [8]  2.7278460 10.6986736
    ## 
    ## $na_interpolation
    ## [1]  0.9126667  1.3668795  1.8426935  2.6618272  3.7385688  5.3712847  6.5980827
    ## [8]  8.3407465 10.6986736
    ## 
    ## $na.locf
    ## [1]  1.855190  2.695737  3.893174  5.240849  6.308034  7.714301  9.331696
    ## [8] 10.843248 11.918100
    ## 
    ## $na_mean
    ## [1] 2.671651 3.911746 4.634842 5.311242 6.116699 6.695346 7.128735 7.659977
    ## [9] 8.498380

``` r
plot_errors(a, plotType = 'line')
```

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

#### Citation

Neeraj Bokde and Marcus W. Beck (2016). imputeTestbench: Test Bench for
the comparison of imputation methods. R package version 3.0.
<http://www.neerajbokde.com/cran/imputetestbench>

#### Bug reports

Please submit any bug reports (or suggestions) using the
[issues](https://github.com/neerajdhanraj/imputeTestbench/issues) tab of
the GitHub page.

#### License

This package is released in the public domain under the creative commons
license CC0.

<!-- README.md is generated from README.Rmd. Please edit that file -->
