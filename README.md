# 2016.M3.TQF-ML.Chinese-Stock-High-Bonus-Share-Prediction

Project Description

This project touches on a unique stock market phenomena in Chinese stock market called High Bonus Shares. 
High Bonus Shares is quite related to the net asset per share, reserved per share and undistributed profits per share.
It turns out that the companies that send high bonus shares to investors in Chinese A-stock market tend to have abnormal return in the future.
Then the goal of the project is to train the computer to select the companies in A-stock market that are very likely to send high bonus shares. 

Data

In this project, I will pick some accounting data the financial statement of the listed companies and use the financial ratios and other indicators to train the computer.
I use the TuShare to obtain the data. The data is mainly from the sina finance. Tushare is a utility for crawling historical and Real-time Quotes data of China stocks, it is easy to use since most of the data returned are pandas DataFrame objects and it is available  https://pypi.python.org/pypi/tushare/

Features

From the 27 futures I select 9 most relevent ones in the project

shares: high bonus shares per 10 shares
outstanding: the number of outstanding shares
totals: the number of total shares 
bvps: book value per share
reservedPerShare: including capital paid in excess of Par and corporate reserves
perundp: part of the retained earnings 
pb: Price-to-Book ratio
rev: the growth rate of sales
profit: the growth rate of net profit

Methods

Try SVC/decision tree/bagging classifier/AdaBoost classifier/Random Forest classifier/Voting classifier and  use GridSearchCV/PCA to improve the results.

The project process

1.Do the preprocessing of the data.
2.Use the traditional financial ratios as the inputs.
3.Add some other indicators as the inputs.
4.Try lots of the methods and vary parameters to improve the model.
5.Do some visualization.

Implementation

The python notebook file: https://github.com/goodgoodye/2016.M3.TQF-ML.Chinese-Stock-High-Bonus-Share-Prediction/blob/master/Chinese-Stock-High-Bonus-Share-Prediction.ipynb

Conclusion

The model I derive is not that good even though its accurancy is 95% more, but it predicts few high bonus share company.That is, 
some companies that turn out to send high bonus share are ignored by the model. 
However, if we focus on the pediction. we will find that if we believe in our model, we have 43% chance to select the companys that turn out to send high bonus shares in the future. If we select randomly, our chance to obtain the companys that turn out to send high bonus shares in the future is 7%. In this prospective, we really improve the prediction ability.








