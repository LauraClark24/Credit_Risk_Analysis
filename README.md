# Credit_Risk_Analysis

## Overview
This project is intended to find and code up a useful program to assess whether loans are a risk or a safe bet for the bank. In order to be sure to present only the most useful results, this repository includes multiple examples of models to potentially sort as desired with statistics to assess their successfulness. 
## Results
- Random Oversampling seems decently good at a test accuracy of 67%. The total precision is high at 99% and the recall is not as great, but still good at 65%. The confusion matrix also shows we have more correct than wrong, confirming it is a decent method to use.

![RandOvSmpl](https://user-images.githubusercontent.com/83182353/131281041-ba07420b-8497-4759-9fce-b012af0d9e7c.png)

- Smote Oversampling does almost just as well with a respectable 66% on the accuracy. The precision is exactly the same at 99% and the recall is up at 69%. Some may consider this an improvement, but it is doubtful if it is worth the processing. 

![SmoteOvSmpl](https://user-images.githubusercontent.com/83182353/131281052-a0fc67b4-d912-46b1-902a-a00164e38b7a.png)

- Cluster Centroids under sampling does, predictably, not as well with an accuracy score of 54%. The precision is on par with the other 99%, but the recall returns to the subpar expectation at a measly 40%. Unsurprisingly, removing data provides the worst predictability.

![CCUndrSmpl](https://user-images.githubusercontent.com/83182353/131281059-c602346f-f755-4d42-8157-5854c2fb20e8.png)

- Smoteenn combination sampling comes in at about the middle with an accuracy of 64%. Precision is still up at 99% while recall is a mere 58%. In both accuracy and recall, it is 10% or more above the under sampling, but still not quite on par with oversampling, especially in recall.

![SmoteennFudge](https://user-images.githubusercontent.com/83182353/131281073-263eb94b-28aa-4b00-87bc-01fb76b1a108.png)

I am aware that this is not the numbers I generated, and I decided to use this because I was unable to get the sampeling in the first cell to run.


- The more complicated Random Forest classifier manages to get the new higher accuracy at 68%. We immediately follow that up with a not so great 100% in both precision and recall, leading to the reasonable take that this model may be overfit and therefore less accurate for any other situation. 

![RndmForest](https://user-images.githubusercontent.com/83182353/131281082-5fa19c35-5a6a-4a42-a420-91c487b26f88.png)

- The Easy Ensemble classifier ends us off with another 68%. With a closer look, especially at the confusion matrices, we see the results are identical to the random forest. This leads to the same doubts about the viability of this model. 

![EsEnsmAdabost](https://user-images.githubusercontent.com/83182353/131281084-b43134e8-4f4e-4b56-80f3-02fff99beab8.png)

## Summary
 If you had to take one model out of this as it is and use it, hopefully not as the only judge. I should have to recommend the Random oversampling. Not only did it do well, it is also one of the fastest methods. With a little more effort, the Random Trees classifier would be better. By normalizing the data and shifting to a model that only focuses on a few of the most important features, this could easily become the best model to use in any situation. 
