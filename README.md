# The State of COVID-19 in South Korea 
Final project for Python for Data Management & Analytics, Spring 2020

## Overview
* Explored epidemiological data to research patient outcome (released, isolated, or deceased) patterns in South Korea
* Used the Naive Bayes algorithm as well as the kNN algorithm to train and test data
* Wrote a final research paper in IEEE conference format

## Intro
* I chose to research the outcomes of people who contracted COVID-19 (Coronavirus Disease 2019). As a Chinese person in the midst of this viral outbreak, I have felt pretty strongly about the virus due to its origin in China and the public’s reaction to it. Since COVID-19 is spreading widely and quickly, I thought it would be useful to look at patterns of who it has been affecting the most. 
* Anyone who is planning on travelling to heavily infected areas or anyone who is simply worried about the virus could somewhat benefit from my model. I looked at datasets with patient information and analyzed the effects of the virus on the patients based on variables such as location, age, gender, and the date that the patient contracted the virus. 

## Data
* I used an open dataset that is based on report materials from the Korea Centers for Disease Control & Prevention and local governments, containing patient information from January to March 2020.
* Cleaned the data by removing unnecessary variables, dealing with null values, and ensuring the data was consistent.
  - Removed columns that didn't not give much nsight on deciding the state of the patient.
  - Dropped columns with too much null data, choosing more indicative factors with more telling data.
  - In other cases, replaced rows with null data with the mean of the column.
* Generated several graphs (histograms, box plot) to check out some of the variables and hypothesize the impact of the virus on the patients.

## Analysis & Results
* I chose to use the Naive Bayes algorithm to train and test the data due to it being able to perform well in multiclass class prediction and with categorical input variables. I also chose to use the k-nearest neighbors (KNN) algorithm, as it naturally handles multiclass cases and is flexible to feature choices.
* The Naive Bayes algorithm resulted in an accuracy score of approximately 0.717 and a k-fold cross-validation score of approximately 0.643. The KNN algorithm resulted in an accuracy score of 0.778 and a k-fold cross-validation score of 0.654.

## Discussion
* Both of the algorithms resulted in cross-validation scores that are lower than the original accuracy scores, indicating that the models may not be the best at determining a patient’s state. However, the models would still be able to predict a patient’s state to some degree of accuracy. One contributing factor to that might be the distribution of state in the original dataset. The vast majority of the patients have a state of either “isolated” or “released,” and very few have a state of “deceased,” likely making it difficult to accurately predict a “deceased” state based on the features. 
Whether or not a patient had any previous underlying diseases would likely be a large deciding factor in a patient’s state. Had there not been so much unknown data for this factor, the models would have probably been more accurate, given that every patient in the dataset that was indicated to have had an underlying disease had a state of “deceased.” 
