# Custom Churn Project

This project aims to create accurate predictive models for customer retention using random forests.
Dataset was obtained from https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset.

## Procedure
  * Read in and prepared the dataset
  * Divided the dataset into a train/test split (70/30)
  * Created the baseline random forest model
  * Created a follow-up random forest model with hyperparameter tuning
    * Principal Component Analysis was also considered before this step but was not necessary as there weren't too many factors.
  * Compared baseline model to the tuned model.
  * Generated conclusions based on the models and generated actionable insights for future steps.

## Conclusion
Baseline Model Performance: 85.23%
                | Predicted: Stayed | Predicted: Left
Actual: Stayed  | 2333              | 56
Actual: Left    | 387               | 244

|               | First Header  | Second Header
| ------------- | ------------- | -------------
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Tuned Model Performance: 85.80%

The tuned model demonstrates a slightly better performance in contrast to the baseline model. Of particular significance is that the tuned model is better at predicting if a customer is going to leave the bank, which is arguably the most important criteria we are looking for in this type of analysis. Overall, the model demonstrates promising capacity to guide our decision-making processes regarding customer retention.

A first step of action can be to look into why a higher proportion of customers middle-aged and above (41+) churn. One possible explanation could be because of technology adaptation: as we move towards digital banking and online services, older customers may be uncomfortable dealing with technology and seek more familiar alternatives. Going forward, we have to pay special attention to our older customers and ensure they have the necessary user-friendly resources to facilitate a satisfactory banking experience with us.

## Future Direction
To make a more thorough model, we can generate more random forests by increasing the number of iterations and cross-validations.
From there, we can identify the values of hyperparamters that created the most successful models on average. 
After that, we use these specific hyperparameters to continue with a second round of hyperparameter tuning using GridSearchCV. GridSearchCV would then perform every combination of the hyperparameter values we gave it and return the model with the best hyperparameters. However, going through these steps take a lot more computation power. This project was made to be run-time friendly, and so these steps were not taken here.

This was my first dive into the realm of machine learning, so any feedback is welcome.


