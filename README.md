# Venture Funding with Deep Learning

![venture](Images/13-challenge-image.png)

### Module 13 Challenge: Neural Networks
---
## Table of Contents
1. [Data_preprocessing](#1-Data-Preprocessing)
2. [Model_Development](#2-Model-Development)
3. [Neural_Network_Architecture](#3-Neural-Network-Architecture)
4. [Deep_Neural_Network_Models](#4-Deep-Neural-Network-Models)
5. [Conclution](#5-Conclution)
---

 **This report outlines the development and optimization of a deep neural network model to predict the success of startups funded by Alphabet Soup, based on historical data. The model ingests preprocessed data, utilizes a binary classification approach, and undergoes optimizations to improve its accuracy, or attempts to!**

##  1. [Data_preprocessing](#1-Data-Preprocessing)

  - Data Import: The applicants_data.csv file was converted into a Pandas DataFrame.
Feature Identification: Categorical and numerical features were identified.
  - Cleaning: Irrelevant columns ("EIN" and "NAME") were dropped.
  - Encoding: Categorical variables were encoded using OneHotEncoder.
  - Feature/Target Split: Features (excluding "IS_SUCCESSFUL") and target variable ("IS_SUCCESSFUL") were defined.
  - Train/Test Split: Data was split into training and testing sets.
  - Scaling: Features were scaled using StandardScaler.


## 2. [Model_Development](#2-Model-Development)
![Neural Network](Images/NNetworks.jpeg)
## 3. [Neural_Network_Architecture](#3-Neural-Network-Architecture) 
A deep neural network was designed with TensorFlow's Keras, based on the number of input features and desired hidden layers and neurons.
 - Compilation and Fitting: The model was compiled using the binary_crossentropy loss function, adam optimizer, and accuracy metric.
 - Evaluation: Loss and accuracy were calculated on the testing data.
 - Saving: The model was saved as an HDF5 file ("AlphabetSoup.h5").
 - Model Optimization:

### Multiple Models: Three models were created, aiming to improve accuracy through:
 - Network expansion: Adding hidden layers or neurons.
 - Activation function changes: Exploring different activation functions.
 - Epoch modification: Adjusting the training duration.
 - Evaluation and Comparison: Each model's accuracy was recorded and compared.
 - Saving: Optimized models were saved as separate HDF5 files.

---
## 4. [Deep_Neural_Network_Models](#4-Deep-Neural-Network-Models)

 ### 1) Original Model
 - Input Features: 116
  - 1st Hidden layer nodes: 58 (relu)                   
   - 2nd Hidden layer nodes: 29   (relu)                  
   - Output nodes: 1 
   - Epochs ran: 50    

#### *Loss result: 56.29%.*
#### *Accuracy results: 72.55%*

**File:** [original model report](/Resources/AlphabetSoup.h5)


---

 ### 2) Alternative Model 1 (A1)
- Input Features: 116
- 1st Hidden layer nodes: 39 (relu)                                    
- Output nodes: 1 
- Epochs ran: 50    

#### *Loss result: 56.08%.*
#### *Accuracy results: 72.65%*

**File:** [A1 model report](/Resources/AlphabetSoup_A1.h5)


---
 ### 3) Alternative Model 2 (A2)
  - Input Features: 116
  - 1st Hidden layer nodes: 33 (activation=swish)                   
   - 2nd Hidden layer nodes: 111(activation=swish)      
   - 3rd Hidden layer nodes: 11 (activation=relu)           
   - Output nodes: 1 
   - Epochs run: 111
#### *Loss result: 55.96%.*
#### *Accuracy results: 72.75%*
**File:** [A2 model report](/Resources/AlphabetSoup_A2.h5)

---
![model chart](Images/Screenshot%202024-02-08%20022005.png)
---
## 5. [Conclution](#5-Conclution)
---
### This report details the development and optimization of a deep neural network model for predicting startup success. While further refinement is possible, the model demonstrates potential for Alphabet Soup in making informed funding decisions. 

*The data is not very good at returning accurate results. The 3 models, while, very different all resulted in similar predictions. It seems that the deep learning models and are over fitted. I would recommend further preproccessing the data to reduce the "noise", filtering out some of the input features to further improve the correlation of the data.* 

Recommendations:

Gather additional data for improved model accuracy.
Explore more advanced model architectures and techniques.
Consider deploying the model in a production environment for continuous learning and improvement.
Note: This report provides a general overview. Specific details on data preprocessing, model architecture, optimization techniques, and results will vary depending on the actual implementation.


Tools Used:
---
   -  TensorFlow
   - Keras
   - Pandas
   - Scikit-learn

**Link to code** [Module 13 code](/venture_funding_with_deep_learning.ipynb)
