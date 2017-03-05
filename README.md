# A-B-Test Kristy Morris Project 7-- Udacity 


# Metric Choice--Gross Conversion/Retention/Net Conversion

The metrics I chose are listed below and why--

Gross conversion: evaluation metric. The numbers of users who decide to start the free trial are expected to depend on how the "start free trial" page is rendered --- whether a "5 or more hours per week" is suggested --- this is one question we would like to understand through this A/B test. Therefore, this is a good evaluation metric.

Retention: evaluation metric. Similar to the above, we would like to understand whether rendering a "5 or more hours per week" suggestion is helpful to increase ratio of users who make payments over those who finish the free trial, and therefore this metric is good for evaluation.

Net conversion: evaluation metric. The net conversion is the product of previous two evaluation metrics: gross conversion and retention, and it can be considered as a more general goal of the A/B test --- whether rendering a "5 or more hours per week" suggestion helps increase the ratio of users who make payment over those who see the start free trial page. Therefore it is also a good evaluation metric.


# Measuring Variability--

For Bernoulli distribution with probability p and population N, the analytical standard deviation is computed as std = sqrt(p * (1-p) / N).  To understand whether the analytical estimates of standard deviation are accurate, i.e. whether it matches the empirical standard deviation, we consider whether or not the unit of analysis and unit of diversion matches up.

# Sizing--

Number of Samples vs. Power

I decided not to use Bonferroni correction, because the metrics in the test has high correlation and the Bonferroni correction will be too conservative to use it.

I calculated the number of samples needed for each metric using the online calculator, with alpha = 0.05, 1 - beta = 0.2. The baseline conversion rate and minimum detectable effect (d_min) are listed individually below. Also note that the number produced by the online calculator is per branch, and in order to have both control and experiment, we need to double the number of required page views.

Gross conversion. The baseline conversion rate is 0.20625, and d_min is 0.01. The required number of samples calculated from the online calculator is 25835. Note that this is the number of clicks on "start free trial", and in order to get that number, we need 25835 / 0.08 * 2 = 645875 page views.
Retention. The baseline retention rate is 0.53, and d_min is 0.01. The required number of samples calculated from the online calculator is 39115. Note that this is the number of users who finished the 14 days free trial, and in order to get that number, we need 39115 / 0.08 / 0.20625 * 2 = 4741212 page views.
Net conversion. The baseline conversion rate is 0.1093125, and d_min is 0.0075. The required number of samples calculated from the online calculator is 27413. Note that this is the number of clicks on "start free trial", and in order to get that number, we need 27413 / 0.08 * 2 = 685325 page views.
If we keep the retention rate as a evaluation metric, the number of required pages will be too large (in order to get 4.7 million page views, it takes 117 days of full site traffic, which is not realistic). Therefore we decide to drop the retention rate evaluation metric, and use gross conversion and net conversion as evaluation metrics, and the required number of page views (take the larger one) is 685325.
