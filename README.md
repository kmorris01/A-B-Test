# A-B-Test Kristy Morris Project 7-- Udacity 


Metric Choice--Gross Conversion/Retention/Net Conversion

The metrics I chose are listed below and why--

Gross conversion: evaluation metric. The numbers of users who decide to start the free trial are expected to depend on how the "start free trial" page is rendered --- whether a "5 or more hours per week" is suggested --- this is one question we would like to understand through this A/B test. Therefore, this is a good evaluation metric.

Retention: evaluation metric. Similar to the above, we would like to understand whether rendering a "5 or more hours per week" suggestion is helpful to increase ratio of users who make payments over those who finish the free trial, and therefore this metric is good for evaluation.

Net conversion: evaluation metric. The net conversion is the product of previous two evaluation metrics: gross conversion and retention, and it can be considered as a more general goal of the A/B test --- whether rendering a "5 or more hours per week" suggestion helps increase the ratio of users who make payment over those who see the start free trial page. Therefore it is also a good evaluation metric.


Measuring Variability--

For Bernoulli distribution with probability p and population N, the analytical standard deviation is computed as std = sqrt(p * (1-p) / N).  To understand whether the analytical estimates of standard deviation are accurate, i.e. whether it matches the empirical standard deviation, we consider whether or not the unit of analysis and unit of diversion matches up.

