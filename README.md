### EX NO: 3
### DATE: 8/4/2022
# <p align="center">MULTI CLASS CLASSIFICATION</p>
## Aim:
To write a python program to implement the multi class classification algorithm .

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab

## Related Theoritical Concept:
Multiclass Classification
In multi-class classification, the neural network has the same number of output nodes as the number of classes. Each output node belongs to some class and outputs a score for that class. Class is a category for example Predicting animal class from an animal image is an example of multi-class classification, where each animal can belong to only one category.

The number of classifier models depends on the classification technique we are applying to.
•One vs. All:- N-class instances then N binary classifier models.
•One vs. One:- N-class instances then N* (N-1)/2 binary classifier models.
•The Confusion matrix is easy to derive but complex to understand.



## Algorithm
1.define dataset with centers=3. <br>
2.summarize dataset shape.<br>
3.ummarize observations by class label.<br>
4.summarize first few examples.<br>
5.plot the dataset and color the by class label
```






```


## Program:
```
Program to implement the multi class classifier.
Developed by: ASHWIN A O
RegisterNumber: 212220230005
```
```python
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot
X,y=make_blobs(n_samples=1000,centers=3,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)
for i in range(10):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()
```
## Output:
![164032777-9a1bfac4-2642-489a-ba54-5072a6a78423](https://user-images.githubusercontent.com/75235601/164069737-f24b768e-714b-4218-9ce4-87634055bf7c.jpeg)


## Result:
Thus the python program to implement the multi class classification was implemented successfully.
