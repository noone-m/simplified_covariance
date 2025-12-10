# Covariance


The reason of this lab is that when I was preparing for my neural network exam, I encountered the formula of convariance as :

$$
\text{Cov}(x, y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{y})(y_i - \bar{y})
$$

but the standard and well known formula for Covariance is :

$$
\text{Cov}(x, y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})
$$

so I thought ther would be some kind of typo in my lecture formula but surpisingly after testing it on diffrent datasets, I got the same results for the two formulas.**That's weird!**

To understand how that could happen, I spend some time playing around and then It turned out that the number you subtract does not actually matter!!!

**this is correct:**

$$
\text{Cov}(x, y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - Number)(y_i - \bar{y})
$$

$$
Number\in{[-\infty,+\infty]}
$$

**and this is correct (covariance is commutative) :**

$$
\text{Cov}(x, y) = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})(y_i - Number)
$$

$$
Number\in{[-\infty,+\infty]}
$$

**so Number can be any value from $\bar{x}$ , $\bar{y} $ ,zero or any other number.**

In this notebook, I'll try to explain how this is happening.
