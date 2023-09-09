# Predicting The Likelihood of Opioid Addiction Based on Age and Previous Drug Use
## _A Project Focused on Health Claims Analysis_

### _Disclaimer_
> This is merely for personal research purposes and I, the author, am not a trained medical professional, merely a university student who is immensely curious in medical insights that could be gained through artificial intelligence. Please do not take any of the information presented here as medical advice.

## Motivation:🤔
Methadone is often used in the treatment of heroin and other opioid dependencies. Though not necessarily the only case of its usage, creating a model based on certain factors inherent to a patient from health claims data and their use of methadone may provide health care authorities with insight into the most optimal ways in which to target opioid addiction.

## Process of Data Analysis: 🔨

### 1. Obtaining The Data
- The data used was obtained from Big Query Sandbox, specifically the [cms synthetic patient dataset](https://console.cloud.google.com/bigquery?project=awesome-aurora-382808&ws=!1m4!1m3!3m2!1sbigquery-public-data!2scms_synthetic_patient_data_omop).
- I used SQL to select the columns regarding a particular heart disease patient's prior drug use, their age during their heart disease procedure, the duration of this drug use, and whether they had used methadone from the concept, drug\_exposure and procedure\_occurrence tables.

### 2. Machine Learning Process
- The machine learning process was conducted in jupyter notebook.
- The data was split into training and testing samples in a ratio of 4:1.
- From sklearn, the logistic regression model was used to classify the likelihood of methadone usage based on the age and the duration of exposure to previous drugs of the training dataset.
- This model was then used to evaluate the test dataset and the accuracy of the score was then determined.

## Results: 💡
The model has an accuracy of 72.0 +/- 0.5%. This is only with regards to the prediction of methadone usage so it may not be a direct 1 to 1 relationship with opioid usage although it is primarily a pain killer for opioid addiction treatment. 

## Discussion: 📖
The model created did not consider many other relevant health factors such as the patient's exercise rate, smoking habits, location of living and etc. Perhaps the usage of opioids may depend more on where its distribution is more dominant and hence an average individual would have more access to it. Perhaps there may be a relationship between familial members using opioids and their children using opioids. These mere speculations should be researched further to provide a more holistic approach on how this model could be improved.

Furthermore, the use of methadone dosage as an indicator of opioids use does not consider those who do not seek treatment for their opioid addiction. In fact, in a 2020 survery by the [https://www.samhsa.gov/data/release/2020-national-survey-drug-use-and-health-nsduh-releases](NSDUH), only approximately 13% of drug addicts sought treatment. This model would thus likely be a significant underestimate of the reality of opioid addiction.

## Conclusion: 🧑‍🏫
This project was an interesting exploration into the possibility of predicting a patient's affinity to opioid addiction based on their age, heart health and previous drug use. However, it is clear that the task of using machine learning to prevent opioid addiction does not stop by looking at only 3 factors. Using health claims to predict future drug usage clearly leaves a lot more to be desired.

## Software Used: 🖥️

- Python 3.9
- Sci-kit learn
- Matplotlib
- Pandas
- Numpy
- Google Big Query
- SQL

## Techniques Used: 🥋

- Primary data extraction
- Data processing and cleaning
- Logistic Regression

## Author ✏️
>[@Raymond Shao](https://github.com/rsha0)

## References: 🔗
1. Arrindell D., 'Data Science for Healthcare Claims Data', last updated August 2023, retrieved and completed course on April 17th 2023: <https://www.udemy.com/course/data-science-for-healthcare-claims-data/learn/lecture/24373414#overview>
2. Galarnyk M., 'Logistic Regression using Python (scikit-learn)', published on September 14th 2017, retrieved on April 15th 2023: <https://towardsdatascience.com/logistic-regression-using-python-sklearn-numpy-mnist-handwriting-recognition-matplotlib-a6b31e2b166a>
3. Health Direct, 'Methadone', publishing date unknown, retrieved on April 18th 2023: <https://www.healthdirect.gov.au/methadone#:~:text=Methadone%20is%20prescribed%20for%20the,work%20or%20cannot%20be%20tolerated.>
4. National Institute on Drug Abuse (US), 'Making Addiction Treatment More Realistic and Pragmatic: The Perfect Should Not be the Enemy of the Good', published on January 4th 2022, retrieved on April 17th 2023: <https://nida.nih.gov/about-nida/noras-blog/2022/01/making-addiction-treatment-more-realistic-pragmatic-perfect-should-not-be-enemy-good>
5. Substance Abuse and Mental Health Services Administration (US), '2020 National Survey of Drug Use and Health (NSDUH) Releases', published on 2020, retrieved on April 15th 2023: <https://www.samhsa.gov/data/release/2020-national-survey-drug-use-and-health-nsduh-releases>






