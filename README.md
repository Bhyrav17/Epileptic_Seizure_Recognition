# Epileptic_Seizure_Recognition
  Epileptic Seizure Recognition using PCA and Clustering

<a target="_blank" href="https://colab.research.google.com/github/Bhyrav17/Epileptic_Seizure_Recognition/blob/main/EpilepticSeizureRecognition.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
  
 ## Data Description
  The following data has been downloaded from the UCI ML Repo. The following blurb has been taken directly from the data webpage (https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition)
  
  The original dataset from the reference consists of 5 different folders, each with 100 files, with each file representing a single subject/person. Each file is a recording of brain activity for 23.6 seconds. The corresponding time-series is sampled into 4097 data points. Each data point is the value of the EEG recording at a different point in time. So we have total 500 individuals with each has 4097 data points for 23.5 seconds. We divided and shuffled every 4097 data points into 23 chunks, each chunk contains 178 data points for 1 second, and each data point is the value of the EEG recording at a different point in time. So now we have 23 x 500 = 11500 pieces of information(row), each information contains 178 data points for 1 second(column), the last column represents the label y {1,2,3,4,5}. The response variable is y in column 179, the Explanatory variables X1, X2, ..., X178
  
  The categories of y pertain to:<br>
* 5 -> eyes open, means when they were recording the EEG signal of the brain the patient had their eyes open<br>
* 4 -> eyes closed, means when they were recording the EEG signal the patient had their eyes closed<br>
* 3 -> Yes they identify where the region of the tumor was in the brain and recording the EEG activity from the healthy brain area<br>
* 2 -> They recorder the EEG from the area where the tumor was located<br>
* 1 -> Recording of seizure activity

All subjects falling in classes 2, 3, 4, and 5 are subjects who did not have epileptic seizure. Only subjects in class 1 have epileptic seizure. Our motivation for creating this version of the data was to simplify access to the data via the creation of a .csv version of it. Although there are 5 classes most authors have done binary classification, namely class 1 (Epileptic seizure) against the rest<br>
For this reason we will use a binary classification.

# Main Objective<br>
The current primary objective is to compare how dimensionality reduction (PCA) and clustering affect classification performance.<br>
I will split these into 2 discrete objectives. I will then purue to test a few classification algos to determine the best approach to binary clf.
