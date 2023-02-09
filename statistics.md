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

# 2. Measures of Variability
## Range
Range = Largest value - Smallest value

## Interquartile Range
$\mathrm{IQR} = Q_{3} - Q_{1}$

## Variance
The variance is based on the difference between the value of each observation $x_{i}$ and the mean.
### Population Variance
$\sigma$ - Sigma, Denotes standard deviation\
$\sigma^2$ - Population Varience\
$\mu$ - Mu, Mean for the population

$\sigma^2 = \dfrac{\Sigma(x_{i} - \mu)^2}{N}$

### Sample Variance
Same as population varience but for a sample of a population

$s^2 = \dfrac{\Sigma (x_{i} - \bar{x})^2}{n - 1}$

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

# Measures of Association Between Two Variables
## Covariance
Measure of the directional relationship between two random variables
### Sample covariance
$s_{xy} = \dfrac{\Sigma (x_{i} - \bar{x}) (y_{i} - \bar{y})}{n-1}$
### Population covariance
$\sigma_{xy} = \dfrac{\Sigma (x_{i} - \mu_{x}) (y_{i} - \mu_{y})}{N}$
### Interpretation:
Points in quadrant $I$ correspond to $x_{i} > \bar{x}$ and $y_{i} > \bar{y}$\
Points in quadrant $II$ correspond to $x_{i} < \bar{x}$ and $y_{i} > y$

Thus, the value of $(x_{i} − x)(y_{i} − y)$ must be\
$>0$ for $I$ \
$<0$ for $II$ \
$>0$ for $III$ \
$<0$ for $IV$ 

Thus positive values indicate positive relationship vetween x and y\
However, this measure is affected by unit of measurement (ex: large x, small y)
<img width="828" alt="image" src="https://user-images.githubusercontent.com/50662246/212494422-d970d11e-bcaf-45be-bad3-ae1118aa9cca.png">

## Correlation Coefficient
Not affected by units of measurement\
Shows how strong the relationship between variables is

### Sample correlation
$r_{xy} = \dfrac{s_{xy}}{s_{x} s_{y}}$\
where\
$r_{xy} = \text{sample correlation coefficient}$\
$s_{xy} = \text{sample covariance}$\
$s_{x} = \text{sample standard deviation of x}$\
$s_{y} = \text{sample standard deviation of y}$

### Population correlation
$p_{xy} = \dfrac{\sigma_{xy}}{\sigma_{x} \sigma_{y}}$\
where\
$p_{xy} = \text{population correlation coefficient}$\
$\sigma_{xy} = \text{population covariance}$\
$\sigma_{x} = \text{population standard deviation of x}$\
$\sigma_{y} = \text{population standard deviation of y}$

## Interpretation
A sample correlation coefficient of +1 corresponds to a perfect positive linear relationship between x and y.\
This is true if points can be connected by a straight line

# Combinations & Permutations
## Counting rule for combinations
Selecting n objects from a set of N objects (order is not important)

$C_{n}^N = \dbinom{N}{n} = \dfrac{N!}{n!(N-n)!}$

## Counting rule for permutations
Selecting n objects from a set of N objects where order is important

$P_{n}^N = n! \dbinom{N}{n} = \dfrac{N!}{(N-n)!}$

# Probability
## Conditional probability
$P(A)$ - Probability of event A

$P(A^c)$ - Probability of complement of event A (opposite of event A)

$\cap$ - Intersection of two events\
<img width="528" alt="image" src="https://user-images.githubusercontent.com/50662246/213828302-09afb47e-3790-4282-96db-8afc5371dad9.png">

$\cup$ - Union of two events\
<img width="518" alt="image" src="https://user-images.githubusercontent.com/50662246/213828239-4acf8690-4f52-4957-b212-664191f07595.png">\
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$



Probability of an event A given that event B occured: P(A|B)

$P(A|B) = \dfrac{P(A \cap B)}{P(B)}$

$P(B|A) = \dfrac{P(A \cap B)}{P(A)}$

## Independent Events
$P(A | B) = P(A)$

or

$P(B | A) = P(B)$

## Multiplication law

$P(A \cap B) = P(B) P(A | B)$

## Bayes Theorem
$P(A | B) = \dfrac{P(A)P(B|A)}{P(B)}$

For multiple events\
$P(A_i | B) = \dfrac{P(A_i)P(B | A_i)}{P(A_1)P(B | A_1) + P(A_2)P(B | A_2) + \dots + P(A_n)P(B | A_n)}$

# Probability Distributions

## Uniform Distribution

$$
f(x) = 
    \begin{cases}
       \dfrac{1}{b-a} & \quad \text{for } a <= x <= b \\
       0              & \quad \text{elsewhere}
    \end{cases}
$$

<img width="632" alt="image" src="https://user-images.githubusercontent.com/50662246/213918793-07a55fd9-26b4-41eb-8b51-4aee0b660662.png">


## Normal probability distribution

$f(x) = \dfrac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}(\frac{x - \mu}{\sigma})^2}$

<img width="500" alt="image" src="https://user-images.githubusercontent.com/50662246/213919330-0421c4eb-5b3a-4b28-8be8-9161a4029c6e.png">

Standard normal probability density function\
Special case where $\mu = 0$ and $\sigma = 1$\
Benefit is that values are precomputed and can be easily converted to the actual distribution

$f(z) = \dfrac{1}{\sqrt{2\pi}}e^{\dfrac{-z^2}{2}}$

<img width="371" alt="image" src="https://user-images.githubusercontent.com/50662246/213919521-b8f0c531-d81a-4505-a851-abc4ab32ac75.png">

Converting to standard normal random variable

$z = \dfrac{x - \mu}{\sigma}$

## Exponential probability distribution

$f(x) = \dfrac{1}{\mu} e^{-x/\mu}  \quad \text{for } x >= 0$\
$\text{where }\mu = \text{expected value or mean}$

<img width="313" alt="image" src="https://user-images.githubusercontent.com/50662246/213919890-e595aa87-dde7-4f2a-81f1-256f51945410.png">

# Sampling
## Expected value of $\bar{x}$
Expected value for mean of sample is population mean

$E(\bar{x}) = \mu$

## Standard deviation of $\bar{x}$

Depends on whether the population is finite or infinite

### Infinite population
OR sample size $<=$ 5% of the total population\
$\sigma_{\bar{x}} = \dfrac{\sigma}{\sqrt{n}}$

### Finite population
$\sigma_{\bar{x}} = \sqrt{\dfrac{N - n}{N - 1}} \left( \dfrac{\sigma}{\sqrt{n}} \right)$

### Central limit theorem
The sampling distribution of the sample mean $\bar{x}$ can be approximated by a normal distribution as the sample size becomes large.\
General statistical practice: if n > 30, $\bar{x}$ can be estimated using normal distribution\
In cases when population is highly skewed or outliers are present n > 50 is recomended

<img width="500" alt="image" src="https://user-images.githubusercontent.com/50662246/213938162-68258a18-9a1c-4819-9b3e-b577c90ad800.png">

## Sampling Distribution of $\bar{p}$ (7.6)
The sample proportion $\bar{p}$ is the point estimator of the population proportion $p$.
The formula is the same as for whole population: number of elements with characteristic / total number of elements

$\bar{p} = \dfrac{x}{n}$

## Expected value of $\bar{p}$

$E(\bar{p}) = p$

## Standard deviation of $\bar{p}$

### Infinite population
OR sample size $<=$ 5% of the total population\

$\sigma_{\bar{p}} = \sqrt{\dfrac{p(1 - p)}{n}}$

### Finite population

$\sigma_{\bar{p}} = \sqrt{\dfrac{N - n}{N - 1}} \sqrt{\dfrac{p(1 - p)}{n}}$

## Form of sampling distribution of $\bar{p}$
Same as binominal distribution, form can be approximated by normal distribution IF:

$np >= 5 \quad \text{and} \quad n(1-p) >= 5$

## Other Sampling Methods (7.8)
1. Stratified Random Sampling
2. Cluster Sampling
3. Systematic Sampling
4. Convenience Sampling
5. Judgment Sampling

# Interval estimation (8)
Because point estimation cannot be expected to provide the exact value of the population parameter,\
an interval estimate is computed\
$\text{Interval estimate} = \text{Point estimate} \pm \text{Margin of error}$

## Population mean: $\sigma$ Known
Usually the population mean is unknown\
However, there are scenarios where population mean IS known (or can be estimated with high accuracy)\
For example:\
1. When large amount of historical data is present and can be used to estimate the population standard deviation prior to sampling
2. In quality control applications where a process is assumed to be operating correctly

Interval estimate of a population mean: $\sigma$ Known

$\bar{x} \pm z_{\alpha/2}\dfrac{\sigma}{\sqrt{n}}$\
Where $(1 - \alpha)$ is confidence level and $z_{\alpha/2}$ is the $z$ value\
providing an area of $\alpha/2$ in the upper tail of the standard normal probability distribution.

## Population mean: $\sigma$ Unknown

When the sample standard deviation is used to estimate $\sigma$,\
the margin of error and interval estimate are based on t-distribution.\
Although t-distribution is based on assumption of normal distribution\
research shows that it can be applied in cases where distribution differs significantly from normal.

t-distribution relies on degrees of freedom paramtere. \
The higher the degrees of freedom, the closer is t-distribution to normal-distribution\
<img width="504" alt="image" src="https://user-images.githubusercontent.com/50662246/216847720-af9e490f-3584-4656-8688-6273480a58e1.png">

Interval estimate of a population mean: $\sigma$ Unknown


$\bar{x} \pm t_{\alpha/2}\dfrac{s}{\sqrt{n}}$\
Where $(1 - \alpha)$ is confidence level and $t_{\alpha/2}$ is the $t$ value\
providing an area of $\alpha/2$ in the upper tail of the t distribution with $n - 1$ degrees of freedom.


The reason degrees of freedom in the expression is $(n - 1)$ concerns the use of $s$ as an estimate of population $\sigma$\
$s = \sqrt{\dfrac{\Sigma(x_{i} - \bar{x})^2}{n-1}}$\
Degrees of freedom refer to the number of independent pieces of information that go into the computation of $\Sigma(x_{i} - \bar{x})^2$

## Determening the sample size (8.3)
$n = \dfrac{(z_{\alpha/2})^2 \sigma^2}{E^2}$\
Where $E$ is the margin of error that the user is willing to accept\
and $z_{\alpha/2}$ follows directly from the confidence level desired (usually 95%)


The equation requres $\sigma$ to be known. However, $\sigma$ is usually not known.\
We can use following to estimate $\sigma$:
1. Use data of previous studies as the planning value for $\sigma$
2. Use a pilot study to select a preliminary sample
3. Use judgment or a "best guess". Estimate of largest and smallest values of data. Dividing this range by 4 provides a rough estimate of $\sigma$

## Population propotion (8.4)
Interval estimare for population proportion:

$\bar{p} \pm z_{\alpha/2} \sqrt{\dfrac{\bar{p}(1 - \bar{p})}{n}}$

Sample size for an interval estimate of population proportion

$n = \dfrac{(z_{\alpha/2})^2 p^{\ast}(1-p^{\ast}))}{E^2}$\
Where $p^{\ast}$ is a planing value.\
Same estimation methods as for $\sigma$ apply. \
If none are possible one can use $p^{\ast} = .50$ \
This is the case because the largest value for $p^{\ast}(1-p^{\ast})$ is obtained when $p^{\ast} = .50$ 

# Hypothesis testing
## Type 1 & Type 2 Errors
<img width="615" alt="image" src="https://user-images.githubusercontent.com/50662246/217712660-0700f890-c40f-4814-a64b-7823b37f1b5a.png">

## Hypothesis test formulas
<img width="804" alt="image" src="https://user-images.githubusercontent.com/50662246/217447468-444d82d0-9ef2-4730-aec8-29a8379fff4c.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/50662246/217701326-d3408d35-e859-40c0-a9da-da7bc85816e7.png">

## Computing probability of Type 2 error
If the decision is binary, ie we either reject or accept null hypothesis (instead of usually not rejecting)\
Then a Type 2 error can occur - we accept the result which should have been rejected.

For any true median of population, the probability of type 2 error is calculated by this formula:\
$z = \dfrac{\bar{x} - \mu}{\sigma / \sqrt{n}}$\
Where $\bar{x}$ is the bound of accepting the null hypothesis.

<img width="749" alt="image" src="https://user-images.githubusercontent.com/50662246/217712404-a142ccc1-fc94-445b-a6ae-0ee65aca1d67.png">

Power curves are usefull when assesing the probability of Type 2 error.\
(also operating characteristic curve)
<img width="749" alt="image" src="https://user-images.githubusercontent.com/50662246/217712529-a7708720-f5cf-4221-97b4-fc2497d521c9.png">


