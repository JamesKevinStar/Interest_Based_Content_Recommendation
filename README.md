# Interest_Based_Content_Recommendation

## Description:
This project recommend posts acording to person's preferences using a Multilayer Perceptron to recommend the top 3 posts.


## Table of Contents
- [Data](#data)
- [Procedure](#procedure)
- [Results](#results)
- [Conclusions](#conclusions)

## Data 
The project uses 3 datasets:
  - **Users**: Contains information about the user, and the top 3 posts the user likes.
  - **Posts**: Contains post details, including the type of content.
  - **Engagements**: Shows which kind of post likes every user.

    
 
## Procedure

### 1. Data Exploration. 
- Explores all columns in all datasets.
- Trying to find some irregularities.

### 2. Preprocessing.
- Removed extra spaces from string values.
- Applied one-hot encoding.
- Convert all categorical columns into numerical.
- Scaled values in a range [0, 1].
- Split into train and test data, with 90% - 10%.

### 3. Model Architecture.
- Built a Multilayer Perceptron (MLP), with 5 Dense layers and 2 Dropout layers.
- Training the model with batch_size = 32 and epochs = 20.

### 4. Model Evaluation. 
- Evaluate the model with 2 metrics: Accuracy and HitRate@k.

## Results
- The performance of the model is:
  - Accuracy: 49%
  - HitRate@3: 66%.

## Conclusions
- Using a more specialized model or algorithm could improve performance.
- Experiment with different feature combinations, excluding or adding columns.
- With more time, further experimentation could lead to better results.
