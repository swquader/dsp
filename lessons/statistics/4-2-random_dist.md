[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
from random import random
import thinkstats2 as ts
import thinkplot as tp

sample = []

for x in range(1000):
    num = random()
    sample.append(num)

#plot pmf
pmf = ts.Pmf(sample)

tp.Pmf(pmf)
tp.Show(xlabel = 'numbers', ylabel = 'probability', axis = [0,1,0,.002])

#plot cdf
cdf = ts.Cdf(sample)
tp.Cdf(cdf)
tp.Config(xlabel = 'numbers', ylabel = 'probability')
```

The distribution is uniform. Every number has an equal probability of being generated and the cumulative probability increases linearly. The numbers generated are truly random.
