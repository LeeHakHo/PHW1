# PHW1
2022 Machine Learning PHW1

**Various algorithm test automation functions for one dataset**

**Result Example**

![](https://github.com/Machine-Learing/PHW1/blob/main/Screenshots/Aspose.Words.fc03db81-3384-430a-b521-e1dbe81e9210.001.png)

**Document**

Class getBest5(dataset= 'dataset path')

When a user inserts a dataset, the dataset is preprocessed and the best combination of hyper parameters, scaler, and model is found and Top5 is output. There are 3 scalers [MinMaxScaler(), StandardScaler(), RobustScaler()] and 4 algorithms [Logistic Regression(), Entropy Classifier(), Gini Classifier(), SVC()] and many hyper parameters for each algorithm Included.

LogisticRegression

C=[0.001, 0.01, 0.1, 1, 10, 25, 50, 100]

max\_iter=[50,100,150]

lver=['newton-cg', 'lbfgs', 'liblinear']

DecisionTreeClassifier

criterion = ['entropy']

max\_depth = [2,4,6,8,10,12]

min\_samples\_leaf = [1, 2, 5, 10]

min\_samples\_split = [2, 5, 10, 15]

max\_features = ['auto', 'sqrt','log2']

Gini Classifier

criterion = ['gini']

max\_depth = [2,4,6,8,10,12]

min\_samples\_leaf = [1, 2, 5, 10]

min\_samples\_split = [2, 5, 10, 15]

max\_features = ['auto', 'sqrt','log2']

SVC

C=[0.001, 0.01, 0.1, 1, 10, 25, 50, 100]

kernel=['linear', 'sigmoid', 'rbf', 'poly']

gamma=[0.001, 0.01, 0.1, 1, 10, 25, 50, 100]

**Examples**

dataset = 'breastCancer.csv'

print(getBest5(dataset))

**Methods**

preprocessing(dataset = 'dataset path'):

parameter:: dataset 

The path of the dataset you want to preprocess

return:: X\_train, X\_test, y\_train, y\_test 

Preprocessing the dataset and dividing it into a train set and a test set

modeling(X\_train, X\_test, y\_train, y\_test):

parameter:: X\_train, X\_test, y\_train, y\_test

The train set and test set of the dataset you want to experiment with

Return:: final\_top5.values.tolist() 

Combination of scaler, algorithm, and hyper parameters of the final Top 5 composed of a list
