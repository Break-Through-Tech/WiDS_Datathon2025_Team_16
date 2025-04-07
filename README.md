# WiDS_Datathon2025_Team_16

### **👥 Team Members**

| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Khushi Sinha | @khushi2012 | Built CNN model, performed data augmentation |
| Simran Prajapati | @sim-ran-p | Led EDA, visualized dataset distributions, handled missing data |
| Tuba Siddiqui | @/binarytown | Preprocessed and cleaned the dataset, handled categorical and numerical features|
| Nana Li | @nanali126| Implemented explainability tools |

---

## **🎯 Project Highlights**

* Built a Logistic Regression Model using \[techniques used\] to solve Women in Data Science Datathon 2025
* Achieved an F1 score of \[insert score\] and a ranking of \[insert ranking out of participating teams\] on the final Kaggle Leaderboard
* Used \[explainability tool\] to interpret model decisions
* Implemented \[data preprocessing method\] to optimize results within compute constraints

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)
🔗 [WiDS Datathon 2025 | Kaggle Competition Page](https://www.kaggle.com/competitions/widsdatathon2025/overview)

---
## **👩🏽‍💻 Setup & Execution**

**Follow the instructions given below to clone the repository, set up the environment, and run the code**

### 1. Clone the Repository 
To get a copy of the project, ytou need to run the following command in your terminal:

'''bash
git clone https://github.com/binarytown/Break-Through-Tech/WiDS_Datathon2025_Team_16.git
cd WiDS_Datathon2025_Team_16
'''

### 2. Install dependencies 
Once you've cloned the repository, install the required dependencies by running the following command:

pip install -r requirements.txt

This will help you in installing all the neccessary libraries to run the main code.


### 3. Set up the Environment
### 4. Access the Dataset(S)
### 5. Run the notebook or scripts

---

## **🏗️ Project Overview**

We created a machine learning model for The Women in Data Science Datathon 2025 Kaggle competition that we participated in through the Break Through Tech AI Program. The objective of the challenge is to create a model that can predict whether a person has ADHD and if they are female. In real life, women with ADHD often go undiagnosed for a long time and addressing this problem can bring more attention to it and people thinking about this in the world. Our model aims to help solve this problem and make it easier for women with ADHD to be diagnosed.

Data Science Skills Developed:
* Data cleaning and preprocessing for model development and analysis
* Understanding correlations
* Regression model selection (statistical, machine learning)
* Regression model fitting/testing (cross validation, avoiding over/underfitting, stratification of data during training)
* Explaining factors that drive the performance of the model
* Multi-outcome prediction
---

## **📊 Data Exploration**

**Dataset Folders**
1. the training folder *train_tsv* consists of three types of information about the 1,200+ subjects. They are:
  * the targets (ADHD diagnosis and sex)
  * functional MRI connectome matrices
  * socio-demographic information, e.g., subject’s “handedness” or “parent’s education level”, emotions (“Strength and Difficulties Questionnaire”), and parenting information (“Alabama Parenting Questionnaire”). These include both quantitative and categorical metadata.

2. the test folder *test_tsv* consists of unseen data frames for 300+ subjects. These data frames are as follows:

* functional MRI connectome matrices
* socio-demographic, emotions, and parenting information

**Data exploration and preprocessing approaches**
1. One-Hot Encoding:
   * Applied one-hot encoding to train_categorical_metadata by creating dummy variables.
   * Combined the processed categorical dataset with the functional connectome dataset to create the final training dataset.
2. Conversion of Integer Variables:
   * Converted integer variables to categorical values where appropriate.
3. Handling Missing Values:
   * Filled null values in the training dataset with the mean of the respective columns.
4. Feature Selection:
   * Used logistic regression to identify important features.

**Challenges and Assumptions**
1. Data Integration:
   * Assumed that the functional connectome dataset and the categorical metadata are compatible and can be merged without significant preprocessing.
2. Handling Missing Data:
   * Assumed that filling missing values with the mean is appropriate for the dataset and does not introduce significant bias.
3. Feature Engineering:
   * Assumed that converting integer variables to categorical values improves model performance.
4. Model Assumptions:
   * Assumed that logistic regression is a suitable method for feature selection given the nature of the dataset.

**Potential visualizations to include:**

1. Barplots used to get important features
![image](https://github.com/user-attachments/assets/abfe4f35-6b5d-49b1-a6ce-d3263de8918e)

![image](https://github.com/user-attachments/assets/52e736e5-23c8-4652-a9ca-13717cffdb52)

---

## **🧠 Model Development**

**Describe (as applicable):**

* Models we used were XGBoost, Multi-output classifier, and LightGBM Classifier
* For feature selection, we used Logistic Regression to find top coefficients of ADHD and Sex
* XGBoost Model was the most accurate of all the models we tried, with the mean cross-validations score = 0.67 at (n_estimators=100, learning_rate=0.5, max_depth=20). Upon tuning the learning rate to 0.7, the data was prone to overfitting and was similar for n_estimators to 200 or 300.

---

## **📈 Results & Key Findings**

**Describe (as applicable):**

* Our Kaggle Public Leaderboard score was 0.467!
* Overall, our model performed very well on data, given the time and our initial issues to even set up the notebook, which gave us limited time to improve the accuracy of our model.

**Potential visualizations to include:**

* Confusion matrix, precision-recall curve, feature importance plot, prediction distribution, outputs from fairness or explainability tools
* This is our XGBoost Model predictions head 
![image](https://github.com/user-attachments/assets/2c12aff4-2c6d-466b-8c84-a3923bbe77ab)

* The chart below shows Sex predictions made by XBG Model, where 0(Female) = 222, and 1(Male) = 82
* (Note: For Kaggle, the values of 1 and 0 are vice-versa)

![image](https://github.com/user-attachments/assets/d78ea641-969e-44f7-a473-98cb40a2aeec)



---

## **🖼️ Impact Narrative**

**Answer the relevant questions below based on your competition:**

**WiDS challenge:**

1. What brain activity patterns are associated with ADHD; are they different between males and females, and, if so, how?
2. How could your work help contribute to ADHD research and/or clinical care?


---

## **🚀 Next Steps & Future Improvements**

**Address the following:**

* What are some of the limitations of your model?
  - A limitation of our model was the amount of features we were able to use. Our kernel kept dying if our data got too big, so we were not able to work with as many features as we wanted to. 
* What would you do differently with more time/resources?
  - We would spend more time on optimizing our model and figuring out how we could use more of the dataset. Since it took us so long to get our IDE set up we didn't have much time to do anything about the optimization. 
* What additional datasets or techniques would you explore?
  - We would figure out other ways to preprocess our data and combine it to make it more helpful in training our model. 

---

## **📄 References & Additional Resources**

* Cite any relevant papers, articles, or tools used in your project

---
