# Breast Cancer Survival Rate
The [data](https://www.kaggle.com/datasets/reihanenamdari/breast-cancer) can be described as set of patient's clinical features. This dataset of breast cancer patients was obtained from SEER Program of the NCI, which provides information on population-based cancer statistics. The dataset involved female patients with infiltrating duct and lobular carcinoma breast cancer. Patients with unknown tumour size, examined regional LNs, positive regional LNs, and patients whose survival months were less than 1 month were excluded; thus, 4024 patients were ultimately included. This dataset was uploaded to U-BRITE for [AI against CANCER DATA SCIENCE HACKATHON](https://cancer.ubrite.org/hackathon-2021/).

# Goal
The goal was to create a (classifier) model that is able to take the data of the patient and output whether the model thinks the patient will survive or not and output how confident it is in such a prediction.

# Metrics
The model (SVM) was evaluated on its accuracy which reached 99.5% accuracy on the test set. below is the model confusion matrix and classification report:
<p align="center">
  <img src="https://github.com/mkldhz/Breast-Cancer-Survival-Rate/blob/main/Images/Confusion_Matrix.jpg?raw=true"/>
</p>
<br/>
<p align="center">
  <img src="https://github.com/mkldhz/Breast-Cancer-Survival-Rate/blob/main/Images/Classification_Report.PNG?raw=true"/>
</p>

# Challenges
The main challenge was to make sure the model is calibrated, so the output probability of the model matches the distribution in real life, to make sure of this calibration curve was utilized:
<p align="center">
  <img src="https://github.com/mkldhz/Breast-Cancer-Survival-Rate/blob/main/Images/Calibration_Curve.png?raw=true"/>
</p>
As we can see the (SVM) model follows the same distribution as the ideal calibarion, thusly the model is well calibrated.
