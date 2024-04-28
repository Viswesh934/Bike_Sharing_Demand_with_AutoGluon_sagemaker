# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Sigireddy Viswesh

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?

At the time of submission I faced some errors intially for the initial submission, added some features for the second submission and optimized parameters for the third. Done some exploratry analysis and optimized some on the way of submission.Kaggle refuses the submissions containing negative predictions values obtained from the predictor. All such negative outputs from respective predictors were replaced with 0

### What was the top ranked model that performed?
WeightedEnsemble_L3 is the top ranked model in all the 3 experiments

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I added month,day,hour and year using datetime as added features. Made the season,weather to categorical along with some data visualization

### How much better did your model preform after adding additional features and why do you think that is?
The model exhibited significantly improved performance, particularly evident when examining the hyperparameter optimization (HPO) process. The decision to decompose the date into distinct components proved instrumental, enabling the model to effectively discern and leverage seasonal patterns within the dataset. By augmenting the feature space with these temporal attributes, the model gained enhanced predictive capabilities, resulting in refined classifications and more accurate estimations of the target value.


## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I haven't seen a very drastic change in performance but the hyper tuning did contribute to the performance, some configurations are useful and helped a lot in the model's validation.

### If you were given more time with this dataset, where do you think you would spend more time?
I should have added heatmaps and scatter plots. I would have optimized the hyper parameters more and trained the model for more instances

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default_vals|default_vals|default_vals|1.80091|
|add_features|default_vals|default_vals|default_vals|0.66309|
|hpo|GBM: num_leaves: lower=25, upper=64|NN: dropout_prob: 0.0, 0.5|gbm: num_boost_round: 100|0.49844|

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![image](https://github.com/Viswesh934/Bike_Sharing_Demand_with_AutoGluon_sagemaker/assets/98519767/b9ba5b5c-a14f-4c50-b785-c6c66cd4ce57)


### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score](https://github.com/Viswesh934/Bike_Sharing_Demand_with_AutoGluon_sagemaker/assets/98519767/39e31824-b951-4ffe-85ac-f574b64e7f9f)


## Summary
In this project, I successfully applied the concepts covered in this unit of the course to develop a machine learning regression model using the AutoGluon framework. Leveraging the skills I acquired, I constructed a robust model that yielded promising results, as evidenced by a commendable Kaggle score. This hands-on experience not only solidified my understanding of machine learning techniques but also provided invaluable insights into real-world application scenarios. Overall, I thoroughly enjoyed working on this project and am pleased with the knowledge and achievements gained along the way.
