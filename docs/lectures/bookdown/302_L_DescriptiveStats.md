



# Descriptive statistics


## Summary

Data visualisation

- Grammar of graphics
- ggplot2

**Next**: Descriptive statistics

- stat.desc
- dplyr::across



## Libraries and data


```r
library(tidyverse)
library(magrittr)
library(knitr)

library(pastecs)

library(nycflights13)

flights_nov_20 <- nycflights13::flights %>%
  filter(!is.na(dep_delay), !is.na(arr_delay), month == 11, day ==20) 
```




## Descriptive statistics

Quantitatively describe or summarize variables

- `stat.desc` from `pastecs` library
    - `base` includes counts
    - `desc` includes descriptive stats
    - `norm` (default is `FALSE`) includes distribution stats


```r
nycflights13::flights %>%
  filter(month == 11, carrier == "US") %>%
  select(dep_delay, arr_delay, distance) %>%
  stat.desc() %>%
  kable()
```


## stat.desc output


|             |    dep_delay|    arr_delay|     distance|
|:------------|------------:|------------:|------------:|
|nbr.val      | 1668.0000000|  1667.000000| 1.699000e+03|
|nbr.null     |   58.0000000|    35.000000| 0.000000e+00|
|nbr.na       |   31.0000000|    32.000000| 0.000000e+00|
|min          |  -17.0000000|   -63.000000| 9.600000e+01|
|max          |  193.0000000|   191.000000| 2.153000e+03|
|range        |  210.0000000|   254.000000| 2.057000e+03|
|sum          |  961.0000000| -4450.000000| 9.715580e+05|
|median       |   -4.0000000|    -7.000000| 5.290000e+02|
|mean         |    0.5761391|    -2.669466| 5.718411e+02|
|SE.mean      |    0.4084206|     0.518816| 1.464965e+01|
|CI.mean.0.95 |    0.8010713|     1.017600| 2.873327e+01|
|var          |  278.2347513|   448.706408| 3.646264e+05|
|std.dev      |   16.6803702|    21.182691| 6.038430e+02|
|coef.var     |   28.9519850|    -7.935179| 1.055963e+00|



## stat.desc: basic

- `nbr.val`: overall number of values in the dataset
- `nbr.null`: number of `NULL` values -- NULL is often returned by expressions and functions whose values are undefined
- `nbr.na`: number of `NA`s -- missing value indicator



## stat.desc: desc

- `min` (also `min()`): **minimum** value in the dataset
- `max` (also `max()`): **minimum** value in the dataset
- `range`: difference between `min` and `max` (different from `range()`)
- `sum` (also `sum()`): sum of the values in the dataset
- `mean` (also `mean()`): **arithmetic mean**, that is `sum` over the number of values not `NA`
- `median` (also `median()`): **median**, that is the value separating the higher half from the lower half the values
- `mode()`functio is available: **mode**, the value that appears most often in the values



## Sample statistics

Assuming that the data in the dataset are a sample of a population

- `SE.mean`: **standard error of the mean** -- estimation of the variability of the mean calculated on different samples of the data (see also *central limit theorem*)

- `CI.mean.0.95`: **95% confidence interval of the mean** -- indicates that there is a 95% probability that the actual mean is within that distance from the sample mean

<!--
Excerpt From: Field, Andy. “Discovering Statistics Using R.” iBooks. 

Section 2.5.1

“If you were to calculate the standard deviation between sample means then this too would give you a measure of how much variability there was between the means of different samples. The standard deviation of sample means is known as the standard error of the mean (SE). Therefore, the standard error could be calculated by taking the difference between each sample mean and the overall mean, squaring these differences, adding them up, and then dividing by the number of samples. Finally, the square root of this value would need to be taken to get the standard deviation of sample means, the standard error.”

“as samples get large (usually defined as greater than 30), the sampling distribution has a normal distribution with a mean equal to the population mean, and a standard deviation of: stddev / sqrt(N)”

“This is known as the central limit theorem and it is useful in this context because it means that if our sample is large we can use the above equation to approximate the standard error (because, remember, it is the standard deviation of the sampling distribution).7 When the sample is relatively small (fewer than 30) the sampling distribution has a different shape, known as a t-distribution, which we’ll come back to later.”
-->



## Estimating variation

- `var`: **variance** ($\sigma^2$), it quantifies the amount of variation as the average of squared distances from the mean

$$\sigma^2 = \frac{1}{n} \sum_{i=1}^n (\mu-x_i)^2$$

- `std.dev`: **standard deviation** ($\sigma$), it quantifies the amount of variation as the square root of the variance

$$\sigma = \sqrt{\frac{1}{n} \sum_{i=1}^n (\mu-x_i)^2}$$

- `coef.var`: **variation coefficient** it quantifies the amount of variation as the standard deviation divided by the mean

<!--
## Broom

Part `tidymodels` (under development), converts statistical analysis objects into tidy format


```r
library(broom)

nycflights13::flights %>%
  filter(month == 11, carrier == "US") %>%
  select(dep_delay, arr_delay, distance) %>%
  stat.desc() %>%
  tidy()
```

```
## # A tibble: 3 x 13
##   column     n   mean     sd median trimmed   mad   min    max  range  skew
##   <chr>  <dbl>  <dbl>  <dbl>  <dbl>   <dbl> <dbl> <dbl>  <dbl>  <dbl> <dbl>
## 1 dep_d…    14   245. 4.83e2   30.0   148.   31.8   -17   1668   1685  2.22
## 2 arr_d…    14  -134. 1.32e3   11.1    75.2  22.4 -4450   1667   6117 -2.58
## 3 dista…    14 95996. 2.70e5  550.  31032.  550.      0 971558 971558  2.76
## # … with 2 more variables: kurtosis <dbl>, se <dbl>
```
-->



## dplyr::across

TODO



## Summary

Descriptive statistics

- stat.desc
- dplyr::across

**Next**: Exploring assumptions

- Normality
- Skewness and kurtosis
- Homogeneity of variance


