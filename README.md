# Credit scoring on the dataset of clients' transactions
This repository contains Jupyter notebook with the code which was used for the Alfa Bank's competition. The task was to create a model which would most accurately match the clients with their credit ratings. Credit scoring task is one of the most important tasks for banks. There is almost two approaches for its solution: classic ML models (logistic regression, gradient boosting), or neural networks. The main feature of the dataset attached to the task is that it has a time component. All applications are given in the sequential order, so the data can be considered as time series. Considering this, the second RNN approach has been chosen.

## Dataset
The competition dataset contains information about previous credit applications. The data is anonymized and encrypted by categorical variables. Each row contains diiferent information about the previous client's credit loan, for example, the amount of it, open and close date, information about late payments and etc. Targets are binary, 0 for closing a loan, and 1 for a default. The dataset is presented in several Parquet files (12 files for train and 2 files for test). The key problem with it is very large size, and lack of RAM to process it.  

## Results
Results are evaluated by ROC-AUC metric. The quality achieved is 0.778 on the eval part of the train dataset. On the test dataset the quality is 0.767 (private leaderboard).
