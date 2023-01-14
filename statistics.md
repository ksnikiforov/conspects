# Measures of Location
## Mean (Average)
Simple average\
Can be trimmed, ex: Removing top and bottom 5% to deal with extreme values

$\bar{x} = \dfrac{\Sigma x_{i}}{n}$


## Geometric mean
$\bar{x_{g}} = \sqrt[n]{(x_{1}) (x_{2}) \dots (x_{n})}$

Difference from standard mean:
1. Used for compounding interest
1. Simmilar concept to CAGS

## Percentile
The _pth percentile_ divides the data into two parts:\
approximately p% of the observations are less than the pth percentile

$L_{p} = \dfrac{p}{100}(n+1)$

## Quartiles
Same as Percentiles, but divided into four parts
- Q1 = 1st quartile, or 25th percentile
- Q2 = 2nd quartile, or 50th percentile (also the median)
- Q3 = 3rd quartile, or 75th percentile

# Measures of Variability
## Range
Range = Largest value - Smallest value

## Interquartile Range
$\mathrm{IQR} = Q_{3} - Q_{1}$

## Variance
The variance is based on the difference between the value of each observation $x_{i}$ and the mean.\
### Population Variance
$\sigma$ - Sigma, Denotes standard deviation\
$\sigma^2$ - Population Varience

$\sigma^2 = \dfrac{\Sigma(x_{i} - \mu)^2}{N}$
### Sample Variance
