[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

We can look at the means of the first born weights and others weights by sorting out using birthord. Then we can use the Series function mean() to calculate the above statistics.

```python
	firsts = live[live.birthord == 1]
	others = live[live.birthord != 1]
	print((firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()))
	print(firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean())
```

This yields First Born weight average of 7.20lbs and Other Born weight average of 7.33lbs, with the first born babies weighing on average 0.12lbs less than the others.

We can also look at the Cohen Effect to see if the differences in the mean weight between the First born and the others are significant.

```python
	CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
```

This yields 0.0886 standard deviations, which is about 3 times larger than the Effect of Size for differences in pregnancy lengths between the first born and the others (0.29 SD). 