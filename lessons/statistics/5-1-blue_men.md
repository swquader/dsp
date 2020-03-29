[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
from scipy import stats

low = (5*12 + 10)*2.54
high = (6*12 + 1)*2.54
mu = 178
sig = 7.7

stats.norm.cdf(high, loc=mu, scale=sig) - stats.norm.cdf(low, loc=mu, scale=sig)
```
>>>Around 34% of the population is eligible to join the Blue Man Group.
