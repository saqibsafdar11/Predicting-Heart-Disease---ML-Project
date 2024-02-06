# Predicting Heart Disease
 ML Project using KNN approach

The World Health Organization (WHO) estimates that 17.9 million people die from cardiovascular diseases (CVDs) every year.

There are multiple risk factors that could contribute to CVD in an individual, such as unhealthy diet, lack of physical activity, or mental illness. Identifying these risk factors early on could help prevent many premature deaths.

An R&D company that focuses on providing healthcare solutions. The company has collected anonymized data from multiple hospitals on several patients. The dataset includes relevant information for each patient, such as their personal information and some medical data, including whether or not they have had heart disease before. Our aim is to use the dataset to accurately predict the likelihood of a new patient having heart disease in the future.

The dataset has the following features:

- Age: age of the patient [years]
- Sex: sex of the patient [M: Male, F: Female]
- ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
-RestingBP: resting blood pressure [mm Hg]
- Cholesterol: serum cholesterol [mm/dl]
- FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
- RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
- MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
- ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
- Oldpeak: oldpeak = ST [Numeric value measured in depression]
- ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
- HeartDisease: output class [1: heart disease, 0: Normal]

We started by evlauating anomolalies such as zero values for HR and clean the data.

Next we selected features which may help predicted heart-disease by looking at their correlation cofficient

We will then  train the model on the training set and evalutae on the validation set. 

To train the model on all the features together, we scale the data and then use k-NN model to train.

We further refine the model through hyperparameter tuning before testing the model on the test set.


Our final model was trained using the following features:

- Oldpeak
- Sex_M
- ExerciseAngina_Y
- ST_Slope_Flat
- ST_Slope_Up

and had a test set accuracy of 86.96%. There are a few things we can try to get better results:

1. Explore what would happen if gender wasnt a feature to train on
2. What would happen on a different data set with more geneder balance or only men or women
3. Try different features
4. Explore other algorithms that might perform better than k-NN.
