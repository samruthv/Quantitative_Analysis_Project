# Quantitative_Analysis_Project
Analysis of change of ETF return and the Price of Gold, Crude Oil and JP Morgan Stock

### Data description 

This data includes four columns/random variables: the daily ETF return; the daily relative change in the price of the crude oil; the daily relative change in the gold price; and the daily return of the JPMorgan Chase & Co stock. The sample size is 1000. 

![image](https://user-images.githubusercontent.com/24830955/131888172-e10570ea-5cdf-4bf1-a19c-cc27906a2ab3.png)
![image](https://user-images.githubusercontent.com/24830955/131888195-be268f76-c36b-4f56-b79b-05cc2a1dac89.png)
![image](https://user-images.githubusercontent.com/24830955/131888203-231c7324-24df-4206-8872-2d49cd5b01c2.png)

The first observations can be made about this data. First, the Close_ETF has a much larger mean and standard deviation than any of the three categories. The means for the other 3 categories are below 1. Also, the Pearson correlation data shows that none of the data is highly correlated or correlated at all.

![image](https://user-images.githubusercontent.com/24830955/131888629-3ec0dd7d-d21f-4bf2-aac9-22d7327f00b6.png)
![image](https://user-images.githubusercontent.com/24830955/131888671-273a2217-82a9-4886-8ea3-373001e71bc0.png)
![image](https://user-images.githubusercontent.com/24830955/131888708-1b1b6c07-3746-46dc-9ed3-4897a6ed7477.png)

The main takeaway is that the histograms show the data can follow a bell-curve normal distribution.  The main takeaway is from the time series plots. First, it can easily be seen how much greater Close ETF is than oil, gold, and JPM. Close ETF tends to grow steadily over time, while the other categories tend to fluctuate over time. There is no relationship between each category in the scatter plot.

Proposing an assumption/a hypothesis regarding the type of distribution each column of the data set may follow (i.e., the ETF, OIL, GOLD, and JPM column), based on the plots! Then verify or object that assumption/hypothesis with appropriate tests!

![image](https://user-images.githubusercontent.com/24830955/131889411-d613e97f-b639-42a1-a65a-614d3cd5a02d.png)
![image](https://user-images.githubusercontent.com/24830955/131889463-d4774b44-9a12-4459-ba29-072e3d5dd235.png)
![image](https://user-images.githubusercontent.com/24830955/131889542-98c4d44f-af2c-4c8f-9614-95ee7497000f.png)

The original hypothesis is that each category followed a normal distribution, with gold being right-skewed. The best_fit_distribution function will compare the data to 86 distributions in the scipy python package. The function will return the best fitting distribution with the appropriate parameters.  The function assumes a normal distribution and compares each distribution. If a distribution fits better than the current distribution, then the distribution is replaced.

Close ETF best follows a Mielke Beta-Kappa / Dagum continuous random variable distribution with the parameters k = 21.7  and s = 15.029.  Oil follows a t distribution. The loc and scale parameters are 0.00108 and 0.018 respectively. Gold follows a Tukey lambda distribution. The lambda parameter is -0.097. Finally, JPM is a Johnson SU continuous random variable with parameters a=-0.045 and b=1.62.

You can see from the normalized histogram plots how well each distribution fits.  The probability density function is the bell curve while the data is the bar graphs in the histogram plot. The Close-ETF might have the worst fit of all the distributions.

















