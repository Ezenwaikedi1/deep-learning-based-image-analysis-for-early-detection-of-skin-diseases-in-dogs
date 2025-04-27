### deep-learning-based-image-analysis-for-early-detection-of-skin-diseases-in-dogs

##   Overview 

This project builds a deep learning pipeline to detect various dog skin diseases from images, using transfer learning and ensemble methods. It leverages MobileNetV2, DenseNet121, and a Hybrid Model (XGBoost + SVM + Deep Neural Network with EfficientNetB3 features).

## Dataset 

link to the dataset: https://www.kaggle.com/datasets/yashmotiani/dogs-skin-disease-dataset

The dataset uses a Dog Skin Disease Dataset containing 438 images categorized into 4 classes:

- Fungal Infections

- Bacterial Dermatosis

- Hypersensitivity Dermatitis

- Healthy

Note:

This dataset is not perfect and may contain mislabeled or low-quality images.
Users are encouraged to review and clean the dataset according to their specific needs before applying it in critical settings.

## Exploratory Data Analysis 

i performed some visulaization so as to get insight on the dataset, 

i plotted graphs like;

1. Bar chart and pie chart to show the image categories

## Preprocessing steps 

-  Image resizing
-   normalization
-   Train (80%)
-   val (10%)
-   test split(10%).

## Model used

Model 1 - MobileNetV2: Pretrained MobileNetV2 used for classification.

Model 2 - DenseNet121: Another deep CNN model evaluated on the dataset.

Model 3 - Hybrid Model:

- Feature extraction using EfficientNetB3

- Dimensionality reduction with PCA

- Class balancing using SMOTE

- Classification using XGBoost, SVM, and Deep Neural Network (Ensemble Voting)

## Evaluation:

- Classification Reports

- Confusion Matrices

## Model Comparison Charts (each classification report percentage is gotten based on the mean of the image categories)

Model 1 - MobileNetV2

- precision = 64%

- recall= 62.75%

- f1 score= 61.75%

Model 2 - DenseNet121:

- precision= 50.50%

- recall=51%

- f1 score=48.75%

Model 3 - Hybrid Model

- precision= 86%

- recall=88.50%

- f1 score=86%

## Key Observations:

- MobileNetV2 performed moderately well, achieving 64% precision and 62% recall, showing it can serve as a fast and light baseline model.

- DenseNet121 underperformed compared to MobileNetV2, achieving lower precision and recall, and struggled with slight overfitting and learning stability.

-Hybrid Model clearly outperformed both individual models, achieving 86% precision, 88.5% recall, and 86% F1-score.

-It demonstrates that combining multiple approaches (XGBoost, SVM, and Deep Neural Networks) after feature extraction leads to much stronger generalization and robustness.

-Ensemble techniques greatly helped improve both the precision and recall across all disease classes.

-Conclusion:

The Hybrid Model is the best performing model and is recommended for deployment or further research on this dataset.

## Interactive User Testing:

Users input the disease type.

Random image prediction based on the best model which hybrid model 

## Results

Hybrid Model achieved the best results in Precision, Recall, and F1-Score.

## How to Run

- Mount your Google Drive.

- Make sure the dataset path /content/drive/MyDrive/archive/Dogs is correct.

- Run all the cells step by step:

- Data Loading

- EDA

- Preprocessing

- Training Models

- Evaluations

- User Interaction Section

