[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

Given the fact that distribution of heights is roughly normal with parameters mu = 178 and sigma = 7.7 for men, we can use scipy.stats.norm to represent that.

```python
	import scipy.stats
	mu = 178
	sigma = 7.7
	dist = scipy.stats.norm(loc=mu, scale=sigma)
```

Then to determine the percent of population between 5'10" and 6'1", we can look at the cdf of the normal distribution above at 5'10" and 6'1" and look at the difference (5'10" ~ 177.8cm, 6'1" ~ 185.4cm):

```python
	dist.cdf(185.4)-dist.cdf(177.8)
```

This yields about 34.2% of male population being eligible for Blue Man Group.