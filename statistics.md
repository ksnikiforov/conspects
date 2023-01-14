# 1. Measures of Location
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

# 1. Measures of Variability
## Range
Range = Largest value - Smallest value

## Interquartile Range
$\mathrm{IQR} = Q_{3} - Q_{1}$

## Variance
The variance is based on the difference between the value of each observation $x_{i}$ and the mean.\
### Population Variance
$\sigma$ - Sigma, Denotes standard deviation\
$\sigma^2$ - Population Varience\
$\mu$ - Mu, Mean for the population

$\sigma^2 = \dfrac{\Sigma(x_{i} - \mu)^2}{N}$

### Sample Variance
Same as population varience but for a sample of a population

$s^2 = \dfrac{\Sigma (x_{i} - \bar{x})}{n - 1}$

## Standard deviation
Is calculated as a square root of varience

The standard deviation is measured in the same units as the original data.\
For this reason the standard deviation is more easily compared to the mean and \
other statistics that are measured in the same units as the original data.

Sample standard deviation: $s = \sqrt{s^2}$\
Population standard deviation: $\sigma = \sqrt{\sigma^2}$

## Coefficient of Variation
Descriptive statistic that indicates how large the standard deviation is relative to the mean

$\left( \dfrac{\text{Standard deviation}}{\text{Mean}} \times 100 \right)$%

## Skewness
<img width="861" alt="image" src="https://user-images.githubusercontent.com/50662246/212482587-5d6aa02c-f769-4302-8d8d-8ba7811ded51.png">

## z-Scores
number of standard deviations $x_{i}$ is from the mean $\bar{x}$.

$z_{i} = \dfrac{x_{i} - \bar{x}}{s}$

Chernobyshev's Theorem:
At least $(1 - 1/z^2)$ of the data values must be within $z$ standard deviations of the mean,\
where $z$ is any value greater than 1.

<img width="763" alt="image" src="https://user-images.githubusercontent.com/50662246/212482913-40540818-937f-4f6d-ab58-4c8ad3e72462.png">

## Detecting outliers

1. Using z-Score: 
   -  $-3 < \text{z-Score} < 3$ (99.7%)
2. Using interquartile range:
   - Lower Limit = $Q_{1} − 1.5(\text{IQR})$
   - Upper Limit = $Q_{3} + 1.5(\text{IQR})$
3. Box plot (5 numbers)
   - Values
     - Smallest value
     - First quartile ( $Q_{1}$ )
     - Median ( $Q_{2}$ )
     - Third quartile ( $Q_{3}$ )
     - Largest value
   - How the graph is drawn
     - Bounds are computed using $\pm 1.5(\text{IQR})$
     - Important: Whiskers are lowest and highest values INSIDE the $\pm 1.5(\text{IQR})$ bound
     - Outliers are shown as asterisks
<img width="821" alt="image" src="https://user-images.githubusercontent.com/50662246/212493871-4125184f-795c-4ecc-9112-d0357599ecb3.png">

