+++
author = "Shenger Zhang"
date = 2021-12-10T05:00:00Z
description = ""
image = "/images/image044.png"
image_webp = "/images/image044-copy.webp"
title = "R,Excel:Regression analysis of sales data regarding promotional programs"

+++
GoodMorning is a new line of probiotic juice products. Since its first product launch in 2015, GoodMorning were now on the shelves of nationwide retailers. GoodMorning had the challenge of raising product awareness, particularly about the benefit of probiotics and the great taste. As a recent stat-up in the fairly new probiotic market, GoodMorning did not have the funding to place nationwide advertisements. It instead allocated much of its small marketing budget to in-store demonstrations.

During in-store demonstration, GoodMorning representatives handed our product samples. The representative arrived at a specified store, set up a table, distributed samples, informed consumers about the product, and offered coupons to inspire purchase.

Another promotional program involved competitions among the five GoodMorning sales representatives for the most endcap displays. The endcap is the hub at the end of an aisle-one of the store’s most popular locations. Sales representatives competed for the highest number of stores they could convince to place GoodMorning’s products at the endcap. The winning sales representative received a big screen television. There was also a competition for the best-decorated endcap. The winning store received cases of product for the employees and gift cards.

The company’s in-store demo was launched in November of 2016. Due to limited marketing resources, management was pressured to cut any marketing expense that did not directly contribute to GoodMorning’s results. By July of 2017, several concerns were raised within the company about the effectiveness of the in-store demo program. Some questioned whether the demos boosted sales at all, while others were concerned that any boost was only temporary and that sales would revert to normal levels shortly afterward. Some executives questioned whether the increase in sales volume could justify the associated costs.

At the senior manager meeting, GoodMorning management asked Jim Martin, GoodMorning’s Marketing manager to justify the demo and endcap activities. Jim returned to his computer after the meeting and pored over the sales and promotion spreadsheet from the last few months. He recognized that statistics could be used to help his case. He decided to apply regression analysis to the sales and promotion data (GoodMorning.xlsx) to enable a decision on whether or not the company should continue its promotional programs.

**Model A:**

Build a regression model with all variables in the data to explain the relationship between sales and promotional efforts. Let us refer to this model as Model _A_. Create the residual plot and the scatter plot of fit vs. UnitsSold.

![](/images/blog/730data model/730_Team12_Doc_files/image003.png)

_Plots_

![](/images/blog/730data model/730_Team12_Doc_files/image005.png)

_![](/images/blog/730data model/730_Team12_Doc_files/image007.png)_

_visualizing the Residuals_

_![](/images/blog/730data model/730_Team12_Doc_files/image009.png)_

![](/images/blog/730data model/730_Team12_Doc_files/image011.png)

![](/images/blog/730data model/730_Team12_Doc_files/image013.png)

b)  Discuss the performance and validity of the model, and how to improve and refine the model.

● From the Regression summary, we observe that the R2 and the adjusted R2 values are 78 .7 % and 78.57 percent which is basically

● the proportion of total variation of units sold that is explained by the

● regression model A.

● We also observe that the p-value is very small for the f-statistics hence the overall regression model seems to be significant.

● Based on the **validity of the model** we observe that the independent variables are independent of **multicollinearity.**

● vif(ModelA)

![](/images/blog/730data model/730_Team12_Doc_files/image015.png)

● Normality Assumption: - when we look at the histogram and the Q-Q plot we observe that its symmetric and when we look at the Q-Q plot are close to a 45-degree line

![](/images/blog/730data model/730_Team12_Doc_files/image018.gif)![](/images/blog/730data model/730_Team12_Doc_files/image019.png)

![](/images/blog/730data model/730_Team12_Doc_files/image021.png)

● Based on the validity of the model when we look at the residuals we see that there are 3 clusters and seems like the errors are skewed 

● We see that there are quite a few **outliers** in the data and treating them appropriately might improve the model performance

![](/images/blog/730data model/730_Team12_Doc_files/image039.png)

● One way we could improve and refine the regression model is by removing the “Natural” and the “Fitness” and the Region variable from the model as their p-value seem to be very high.

● Another additional way of refining the model is by explicitly converting the categorical variables using the factor.

**Model B:**

Build the best valid regression model to explain the relationship between sales and promotional efforts. You may use any transformation of your variables. Let us refer to this model as Model _B_. Create the residual plot and the scatter plot of fit vs. UnitsSold.

a) (6 points) Copy and paste the regression output and the plots_._

![](/images/blog/730data model/730_Team12_Doc_files/image025.png)

![](/images/blog/730data model/730_Team12_Doc_files/image027.png)

![](/images/blog/730data model/730_Team12_Doc_files/image029.png)![](/images/blog/730data model/730_Team12_Doc_files/image031.png)![](/images/blog/730data model/730_Team12_Doc_files/image033.png)![](/images/blog/730data model/730_Team12_Doc_files/image035.png)![](/images/blog/730data model/730_Team12_Doc_files/image037.png)

b) (2 points) Discuss the validity of the model?

We observe that there are few outliers in the actual versus fitted plot and we need to use appropriate techniques to treat them and improve the performance of the model.

![](/images/blog/730data model/730_Team12_Doc_files/image039.png)

Also, when we observe the residual versus fitted plot we observe that the distribution of the errors is skewed we see 3 clusters

Finally, when we review the Multicollinearity effect using the VIF function we don't see any multicollinearity all the features are independent of each other

![](/images/blog/730data model/730_Team12_Doc_files/image042.png)

Based on model:

c)  Does the in-store demo program boost the sales? If so, for how long does the sales lift last? 

\-Yes the in-store demo program boosts the sales because , On an average, the units sold is 107 higher if store gave/had a Demo in the corresponding week (compared to no demo ), while all other variables remain the same.

\- The sales lift lasts for all 5 weeks after a demo is provided. Because all of Demo, Demo(1_3), and Demo(4_5) variables had +ve impact/coefficients on the Units sold variables.

\- From the regression model we observe that :

\-On average, the units sold are 73.7 higher if the store gave/had a demo 1-3 weeks ago (compared to no demo ), while all other variables remain the same.

\-On average, the units sold are 71.4 higher if the store gave/had a demo 4-5 weeks ago (compared to no demo ), while all other variables remain the same.

d) Does the placement of the product within the store (endcap promotion) affect the sales?

Yes it does because , on an average, the units sold is 441.007 higher if a store participated in an endcap promotion (compared to no participation ) , while all other variables remain the same.

e) What other factors affect the sales of GoodMorning product?

● Apart from the existing factors/features, the Good Morning product should focus on looking at customer demographics, so that they can promote the product to the right set of customers.

● They can also try different methods /techniques for placement of the product on the shelf /aisle so that it can attract more customers (like placing the product near the billing counter or on the 1st or 2ed shelf may affect the sales).

● Store's web presence is another important factor which can help them promote the product and reach as many ppl through internet.

● Finally, they can also look at the number of restaurants in the vicinity of the store and provide promotional discount to promote the probiotic drink.

f)  Based on the regression output, what are recommendations to Good Morning management?

\- Recommendations to Good Morning management based on the log regression model, which outperformed the other regression models are:

● Focus on the average retail price of the probiotic juice, which has a negative impact on units sold by looking at the coefficients of the variable from the regression model captured per store per week.

● Focus more on presenting a Demo in corresponding week for the store, Demo (1_3) weeks ago and Demo (4_5) weeks ago variables have high/positive impact to improve units sold based on the model coefficients.

● Identifying stores that participate in an endcap promotion because the coefficients for the endcap variable has a positive impact on the units sold based on the model coefficients

● Having a regional salesperson/representative would also assist raise unit Sold as the Sale_Rep variable has a positive impact on the unit’s sold variable.

**Case 2** 

A company is considering whether to market a new product. Assume, for simplicity, that if this product is marketed, there are only two possible outcomes: success or failure. The company assesses that the probabilities of these two outcomes are p and (1-p) respectively. If the product is marketed and it proves to be a failure, the company will have a net loss of $450,000. If the product is marketed and it proves to be a success, the company will have a net gain of $750,000. If the company decides not to market the product, there is no gain or loss.

The company can first survey prospective buyers of this new product. The results of the consumer survey can be classified as favorable, neutral, or unfavorable. Based on similar survey for previous products, the company assesses these probabilities of favorable, neutral, or unfavorable results to be 0.6, 0.3, and 0.1 for product that will eventually be a success, and it assesses these probabilities to be 0.1, 0.2, and 0.7 for a product that will eventually be a failure. The total cost of administering this survey is C dollars.

Let p=0.5 and C= $15,000.

The company wants to construct a decision tree for this problem. The first step is to compute the posterior probabilities that the product will be eventually success and failure using the result from the consumer survey. The probabilities are given in Exhibit A.

The company would like to find the strategy that maximizes the company’s expected net earnings (EMV).

a) Construct a decision tree for this problem (Exhibit A). Generate the optimal decision strategy tree

![](/images/blog/730data model/730_Team12_Doc_files/image046.png)

● Does the optimal strategy involve conducting the survey?

Yes.

● What is the EMV under the optimal strategy?

EMV= 255000

b) Suppose that the total cost of administering this survey is $50,000.

● Does this change the company’s decision?

No.

![](/images/blog/730data model/730_Team12_Doc_files/image050.png)

![](/images/blog/730data model/730_Team12_Doc_files/image052.png)

● What is the maximum amount that the company is willing to pay for the survey?

$120000.

The strategy changes from Yes to No at $120000 according to the strategy report.

c) Conduct sensitivity analysis between 0.3 and 0.9 with 10 steps. 

![](/images/blog/730data model/730_Team12_Doc_files/image054.png)

● What is the approximate value of p that changes the optimal strategy?

The approximate value of p is 0.68.

● Explain the results in detail.

From the starting point of 0.3, the probability of success is quite low. The company will choose to conduct the survey and decide to launch the product based on the survey outcome. For not conducting the survey they will not launch the product until the p is higher than approximately 0.38.

As the probability of success increases, at approximately 0.68 the company will switch from conducting the survey to not conducting the survey before making a decision whether they should launch the new product or not.

As the probability continues to increase, the value of information derived from the survey will reduce . Hence the difference between EMV of Not conducting the survey and conducting will be close to parallel as seen from the above graph and this difference is nothing but the money paid for the survey.

**Now, we would like to find the strategy that maximizes the company’s expected utility with the risk tolerance of R= 500,000.**

d)  Generate the optimal decision strategy tree. Does this change the company’s decision?

![](/images/blog/730data model/730_Team12_Doc_files/image049.gif)

**The model is based on the $15,000 survey fees**

**No, it doesn’t change.**

e)  Conduct a sensitivity analysis on p: between 0.3 and 0.9 with 10 steps. How the second stage decision changes as p increases.

![](/images/blog/730data model/730_Team12_Doc_files/image056.png)

![](/images/blog/730data model/730_Team12_Doc_files/image058.png)

![](/images/blog/730data model/730_Team12_Doc_files/image060.png)

With a risk tolerance of R= 500,000, the company is now risk-averse.

From the starting point of 0.3, the probability of success is quite low. Both conduct the survey and not conduct the survey will choose not to launch the product.

As the probability of success increases, the company will choose to conduct a survey and launch the product according to the survey outcomes. For not conducting the survey, the EMV will remain 0 until they think the probability of success is high enough at approximately 0.64 from strategy region graph pasted above, then they will launch the new product.

As the probability continues to increase, the information obtained from the survey will get less. And the company will choose not to conduct the survey and launch the product anyway when the probability is higher than 0.9.