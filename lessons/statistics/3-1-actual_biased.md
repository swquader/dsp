[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
import thinkstats2 as ts
import thinkplot as tp
cd code
import nsfg

#actual distribution for # of children in a household
df = nsfg.ReadFemResp()

children_per_hh = df.numkdhh.value_counts()

p = {}
for x in children_per_hh.index:
    p[x] = children_per_hh[x] / children_per_hh.sum()

CPH_pmf = ts.Pmf(p)

tp.Hist(CPH_pmf)
tp.Config(xlabel = 'number of children', ylabel = 'probability')

#mean of actual distribution
total = 0
for x in children_per_hh.index:
    total += x*children_per_hh[x]
    
mean = total/children_per_hh.sum()

#biased distribution
biased_CPH = {}

for x in children_per_hh.index:
    biased_CPH[x] = x * children_per_hh[x]
    
biased_pmf = ts.Pmf(biased_CPH)

tp.Hist(biased_pmf)
tp.Config(xlabel = 'number of children', ylabel = 'biased probability')

#mean of biased distribution
btotal = 0
blength = 0

for x in biased_CPH.keys():
    btotal += x * biased_CPH[x]
    blength += biased_CPH[x]
    
biased_mean = total/length
biased_mean
```
