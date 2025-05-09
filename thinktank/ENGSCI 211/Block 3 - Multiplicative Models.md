- Models that are built by transforming using the log function

This is good for:
- Break up the relationship between the variables
- The data is right skewed to the extent that the mean is no longer a good measure of centrality

123 Mazda cars
- Price (AUD)
- Years of manufacture

![[Pasted image 20250509142149.png]]

Mean is much higher than median, very right skewed.

We want to deal with this and still use linear models (lm)

![[Pasted image 20250509142251.png]]

The right skew violates the assumption but the CLT applies so that average price looks good.


### But how do we get an estimate of the median (more accurate when right skewed) using the linear model approach?
Log, usually meaning natural log.
 $$
 log(a times b) = log(a) + log(b)
 $$

This can help reduce the multiplicative relationship into additive.

![[Pasted image 20250509142853.png]]

Logging values and logging summary:
![[Pasted image 20250509143025.png]]

### The Lognormal distribution
![[Pasted image 20250509143054.png]]

Logged median and mean are the same. 

Undoing the log, we just use the exponential. 
![[Pasted image 20250509143351.png]]

WITH THE LOG TRANSFORM WE CAN ONLY MAKE INFERENCES AGAINST THE MEDIAN

## Assumption checks
![[Pasted image 20250509143655.png]]

Now the logged version:
![[Pasted image 20250509143711.png]]

## Relationship between medians of samples
We can say the $log("price")$ of budget cars are on average between $0.3$ and $0.77$ **units** lower than the Mazda cars. Let $m_i$ be median in the original untransformed space:

$$
exp(log(m_1) - log(m_2)) &= exp(log(m_1/m_2)) \
&= m_1/m_2
$$

This gives us the ratio between the two medians.

![[Pasted image 20250509144247.png]]

