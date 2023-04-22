# Breast Cancer Classification
Classification of breast cancer masses into benign or malignant.

## Dataset
The Breast Cancer (Diagnostic) dataset can be found in this [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29).

The dataset consists on a set of 569 digitized images of a fine needle aspirate (FNA) of a breast mass. For each image, a set of 32 features are provided including:

* ID number 
* Diagnosis (M = malignant, B = benign)

Ten values computed for each cell nucleus:

* radius (mean of distances from center to points on the perimeter)
* texture (standard deviation of gray-scale values)
* perimeter
* area
* smoothness (local variation in radius lengths)
* compactness (perimeter^2 / area - 1.0)
* concavity (severity of concave portions of the contour)
* concave points (number of concave portions of the contour)
* symmetry
* fractal dimension ("coastline approximation" - 1)

The mean, standard error, and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features.

## Classification results
A random forest with a grid search for parameter optimization and a 10-fold CV was used. The classification results are:

```python
              precision    recall  f1-score   support

      Benign       0.99      0.94      0.96        71
   Malignant       0.91      0.98      0.94        43

    accuracy                           0.96       114
   macro avg       0.95      0.96      0.95       114
weighted avg       0.96      0.96      0.96       114

```

## Best features based on Gini impurity

<p align="center">
    <img width="600" src="https://github.com/MariaGoniIba/Breast-Cancer-Diagnosis/blob/main/FeatureImportance.png">
</p>

# Relevant Papers
* [Nuclear feature extraction for breast tumor diagnosis.](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/1905/1/Nuclear-feature-extraction-for-breast-tumor-diagnosis/10.1117/12.148698.short)
* [Breast cancer diagnosis and prognosis via linear programming.](https://pubsonline.informs.org/doi/abs/10.1287/opre.43.4.570)
* [Machine learning techniques to diagnose breast cancer from fine-needle aspirates.](https://www.sciencedirect.com/science/article/abs/pii/030438359490099X)
