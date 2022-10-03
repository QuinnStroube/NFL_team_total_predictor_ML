# Texans_Win_Predictor_ML
---
## Project Summary
We created an NFL win predictor for the Houston Texans, determining win totals for the 2021-2022 season. This model is similar to financial algorithmic trading models because we use past data to predict future outcomes. These models are widely used in sports betting, using data retrieved from Pro football reference we collected win totals from 2000-2022 for the Texans.

---
## Database

We pulled all the data from [Pro Football Reference](https://www.pro-football-reference.com/). We could also find all the data we pulled In the resources file in the repository. These CSV files contain the Texans game results from 2002 up to 2022.
---
## Installation Guide
Please refer to the following documentation for installation:

[Pandas](https://pandas.pydata.org/docs/getting_started/index.html)<br/>
[Numpy](https://numpy.org/doc/)<br/>
[Hvplot](https://hvplot.holoviz.org/)<br/>
[Sklearn](https://scikit-learn.org/stable/install.html)<br/>
[Imblearn](https://imbalanced-learn.org/stable/install.html#getting-started)<br/>

---
## Libraries
This application is written in Python. The following Python libraries were used:
```
import pandas as pd
import numpy as np
import hvplot.pandas as hvplot
import matplotlib.pyplot as plt
from imblearn.under_sampling import RandomUnderSampler
from imblearn.over_sampling import RandomOverSampler
```
From Scikit Learn:
```
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, accuracy_score
from sklearn.svm import SVC
from sklearn import tree
from sklearn.neighbors import KNeighborsClassifier
```
---
## Model Results

A total of 3 models were used to accomplish this project's objective. The first one used is the random forest model, which scored an accuracy score of 86%, which may be high; however, we believe too high to be correct. We believe there was insufficient data for the model to train with and put out an accurate score. We performed under sampling and oversampling for a random forest to improve anti-aliasing performance, increase resolution, and reduce noise. For under-sampling, we got an accuracy score of 80%, while for oversampling, the model got an accuracy score of 81%. This, again, might be due to not having more data for the models to train on. 

[Random_Forest](images/Random_forest_1.png)

We then move to use the decision tree model to predict the outcome. The model came out with high precision scores for losses and high recall scores for wins. Finally, the model came out with an accuracy score of 78% with the test data.


(Place the image of the mode outcome here)

The last model we used was the SVM model using two different types of kernels radial basis function kernel (Rbf) and polynomial. The SVM RBF kernel performance showed an accuracy score of 71%, while the SVM polynomial kernel had an accuracy score of 68% with the test data. With this model seeming to be the best out of the three with the most accurate score percentage, we also wanted to test the new data with this model. It produced an accuracy score of 84%, with high precision and recall scores on predicting the losses.


(Place the Image of the model outcome here)



---
## Contributors
Alessandro Valentini<br/>
Quinn Stroube<br/>
David Contreras<br/>
Jerome Bright

---
## License
MIT
