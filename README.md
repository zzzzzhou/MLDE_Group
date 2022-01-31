# MLDE_Group
Considering prediction context, we treat it like time series problem, because before one customer give review on platform, you never know what he is going to say. So, the model can't see the future data. Based on this hypothesis, we sort the data by datetime, and we are going to use 80% data to train, 20% data to test. Approximately, data after 2018 July will be test data, before that time will be train data.

We use decision tree to build our model, based on the intuition that differnt customer have different perception of shopping experience. After training and re-sampleing, it prove that our model can indeed improve review rating, with precision of 82%. In this case, we consider precision is the most important metric, because you are going to invite poeple to write review if model say positive, if model say positive but actually it is negitive, ti won't help the business. Higher precison means more confident with positive prediction.

In data exploration stage, we found that data from 2016 it quite different to 2017 and 2018, 2017 and 2018 is relatively stable. ![image](https://user-images.githubusercontent.com/19428196/151775980-debe5369-3a8b-458f-9690-8d8be0b27fa9.png) 
Maybe in 2017 and 2018, platform had improved alot with its operation. So we drop the data of 2016, and 2016 data is a small group, it has no contribution to model![image](https://user-images.githubusercontent.com/19428196/151776690-98663313-5c64-44c2-b66d-b1702fa76ef8.png)

Given that the data is imbalanced, we try over sampling to imrpove prediction precision. In notebook #construct train and test data by Piggy BMW# you can find RandomOverSampler method. And it indeed improve precision from 80% to 82%

Conclusion
