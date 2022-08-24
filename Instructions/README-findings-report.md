# Machine Learning Trading Bot (Optional)

![Decorative image.](Images/15-challenge-image.png)

Now, it's time to apply what you've learned about machine learning to new situations. For this optional assignment, you'll create an algorithmic trading bot that learns and adapts to new data and evolving markets. Be sure to give it your all&mdash;because the skills that you hone will become powerful tools in your fintech tool belt.

## Background

In this Challenge, I’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. My firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, my firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. I'm thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, I'll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

## What I Created

In a Jupyter notebook, I've done the following:

* Implement an algorithmic trading strategy that uses machine learning to automate the trade decisions.

* Adjust the input parameters to optimize the trading algorithm.

* Train a new machine learning model and compare its performance to that of a baseline model.

## Results

# 1. Established a Baseline Peformance

* Here I created the baseline cumulative return plot that shows the actual return vs. the strategy returns
* Using the SVC Model , the plot below shows the cumulative return of the strategy against the actual return. The inputs are short_windows = 4, long_window=100. For the base, a DateOffset for the training slice was 3 months. 
![svm_1](https://user-images.githubusercontent.com/101617571/186326346-8d5eaed9-ead9-4e2a-beec-a1fb1aecaf86.png)

* Classification report 
![SVC_1_classification_report](https://user-images.githubusercontent.com/101617571/186328632-a1414d25-30cd-4ce9-8769-10f76b499782.png)


# 2. Slice the dataset into different time periods in order to tune the model by adjusting the dataset size. Change one or both window sizes in order to tune the model by adjusting the SMA input features. 
* Here I tuned the SVC model by adjusting certain features. The inputs are short_window=8, long_window=200 and DateOffset = 6 months.
![svm_2](https://user-images.githubusercontent.com/101617571/186326379-d4388997-16e8-45d9-bef1-2a8ccdda2623.png)

* Classification report
![SVC_2_classification_report](https://user-images.githubusercontent.com/101617571/186328685-dad3718a-3c8b-4372-8a7e-ce6b2820dac6.png)

* Here I tuned the SVC model by adjusting certain features again. The inputs are short_window=12, long_window=400 and DateOffset = 12 months.
![svm_3](https://user-images.githubusercontent.com/101617571/186326453-82fe170e-2cad-48a6-8fc8-95bbeb3d5124.png)


* Classification Report
![SVC_3_classification_report](https://user-images.githubusercontent.com/101617571/186328706-ec037752-e2d8-465a-84cf-2d8f3131fd5b.png)



# 3. Evaluate a new Machine Learning Classifier
* Here I implemented a new Machine Learning Classifier, Logistic Regression. The graph below shows the return of the strategy against the actual returns. 
![lr_output](https://user-images.githubusercontent.com/101617571/186196989-1f736e9b-7b79-4f5d-a322-795d9d73e62d.png)

* Classification Report
![LR_classification_report](https://user-images.githubusercontent.com/101617571/186197301-9caec642-23a8-46a3-9bc9-26b5f749f455.png)

# Summary of Results
In this project, I evaluated both the SVC model and the logistic regression model. 

The results show that the SVC model was not effective at producing superior returns it either closely followed actual returns or peformed worse. 

Using the accuracy score in the classification report, we could see that the optimal data size and short long window sizes were as follows:
* Short Window: 4
* Long Window = 100
* DateOffset = 3 months

The Logistic Regression Model however appeared to model the actual returns until a certain point at which it began to almost do the opposite of the actual returns. This is somewhat reflected in the accuracy score which was 0.47. 

---
