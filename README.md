# Machine Learning Trading Bot - Optional

![Decorative image.](Images/15-challenge-image.png)

In this Challenge, I have assumed the role of a financial advisor at one of the top five financial advisory firms in the world. My firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, my firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. I am planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. I will enhance the existing trading signals with machine learning algorithms that can adapt to new data.

### I have created the following 

* Implemented an algorithmic trading strategy that uses machine learning to automate the trade decisions.

* Adjusted the input parameters to optimize the trading algorithm.

* Trained a new machine learning model and compare its performance to that of a baseline model.

---

#### Establish a baseline performance and tune the baseline algorithm 

* Baseline cumulative return plot that shows the actual returns vs. the strategy returns
* SVC Model cumulative return plot that shows the actual returns vs. the strategy returns. Inputs are short_windows = 4, long_window = 100, DateOffset for training slice = 3 months.

![[returns_actual_vs_strategy]](https://github.com/Nithy29/Algorithmic-Trading/blob/main/Images/svm_returns_actual_vs_strategy_1_1.png?raw=true)

- Classification Report

![[Classification Report]](Images/SVM_Classification_Report_1_1.png?raw=true)



#### Turning the model by adjusting the dataset size and adjusting the SMA input features.

* SVC Model cumulative return plot that shows the actual returns vs. the strategy returns. 
  Inputs are short_windows = 8, long_window = 200, DateOffset for training slice = 6 months.
  
![[returns_actual_vs_strategy_6_months]](https://github.com/Nithy29/Algorithmic-Trading/blob/main/Images/svm_returns_actual_vs_strategy_1_2.png?raw=true)

- Classification Report

![[Classification Report]](Images/SVM_Classification_Report_1_2.png?raw=true)


* SVC Model cumulative return plot that shows the actual returns vs. the strategy returns. 
  Inputs are short_windows = 16, long_window = 400, DateOffset for training slice = 12 months.
  
 ![[returns_actual_vs_strategy_12_months]](https://github.com/Nithy29/Algorithmic-Trading/blob/main/Images/svm_returns_actual_vs_strategy_1_3.png?raw=true)

- Classification Report

![[Classification Report]](Images/SVM_Classification_Report_1_3.png?raw=true)


---

#### Evaluate a new machine learning classifier 

* LogisticRegression Model cumulative return plot that shows the actual returns vs. the strategy returns. 
  Inputs are short_windows = 4, long_window = 100, DateOffset for training slice = 3 months.

![[returns_actual_vs_strategy_LogisticRegression]](https://github.com/Nithy29/Algorithmic-Trading/blob/main/Images/LogisticRegression_returns_actual_vs_strategy.png?raw=true)

- Classification Report

![[Classification Report]](Images/LogisticRegression_classification_report.png?raw=true)

### Summary of findings

Predictions using SVC along side LogisticRegression have been modelled. 

It is very evident that the SVC model is not useful at all with short_windows = 8, 16, long_window = 200, 400, DateOffset for training slice = 6 and 12 months.

The optimal data set size and short and long window size that I tested with was.

 - SVM Model
 - Short Window Size = 4
 - Long Window Size = 100
 - Date Offset = 3 months

 These parameters produces the best accuracy score. 
