# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# **Heart failure study**


## **1.Project overview and Motivation**

Heart failure is a condition where your heart cannot pump blood around your body as well as it should, which means the body's oxygen supply is constricted. It impacts the way a body works including breathing and muscles. There are many causes to heart failure, where it can happen suddenly or progress slowly over months or years. It is the number 1 cause of death globally, taking an estimated 17.9 million lives each year. (c. 31% of deaths worldwide) This study will look at some of the key reasons for heart failure and identify which illness or test is the most contributing factor. (source: <https://www.bhf.org.uk/informationsupport/conditions/heart-failure>)

With an undeniable constraint in healthcare globally, I have a strong desire to be involved in being part of the solution to alleviate these challenges and improve patient health through technology. Drawing from my own medical experiences I have had to wait over 6 to 7 months to receive sufficient tests or treatment from public health care. Throughout my studies, I have noticed data gaps in end-to-end visibility of the patient journey, that causes poor operational planning and reduce operational efficiency. By early identification of a patient's illness and therefore fatality we can provide earlier treatment plans to improve recovery time, reducing the constraint on healthcare and staff.

## **2\. Dataset & Source**

This project utilises the [Heart Failure Clinical Records Study dataset](https://www.kaggle.com/datasets/guriya79/heart-failure-prediction-dataset). It contains 299 patient records with 10 potential contributing illnesses, including age and sex.

## **3\. Objectives and Key research questions**

\- Understand which features in this dataset contribute the most to a patient's mortality in hear failure.

\- Understand which demographic in terms of age and sex are more likely to end in a patient's death

\- Use a patient's internal heart tests to predict the death of a patient via machine learning modelling

1\. Load data set from kaggle/ local files

2\. Use capstone project template provided by Code institute

3\. ELT: clean and transform dataset

4\. Initial analysis and detection of outliers

5\. Engineer usable medical features, that can be understood by hospital staff

6\. Explore dataset for research questions and Hypothesis testing

7\. Reflect findings on visualisations created by seaborn and matplot lib

8\. Prepare cleaned data for dashboarding in Tableau.

1\. Which features in patient are most important when considering death in heart failure?

&nbsp;   H1: Age plays a big role in determining the death of a patient through heart failure

2\. Which internal heart test plays the significant part in determining a patient's death?

&nbsp;   H2: Ejection fraction and serum creatinine play an important part in determining a patient's death

## **4\. GitHub project file and repository structure**

┣ 📂data_set

┃ ┗ 📜heart_failure_clinical_records_dataset.csv

┣ 📂jupyter_notebooks

┃ ┣ 📜dashboard_data.csv

┃ ┗ 📜heart_failure_clinical_study.ipynb

┣ 📜.gitignore

┣ 📜.python-version

┣ 📜.slugignore

┣ 📜dashboard_data.csv

┣ 📜Procfile

┣ 📜README.md

┣ 📜requirements.txt

┗ 📜setup.sh

## **5\. Tools and Technologies used**

Python 3.12

Pandas library

Matplotlib

Seaborn

ScikitLearn

Numpy

Tableau

Jupyter Notebook

GitHub

VS Code

AI tools: ChatGPT, Co pilot and Gemini

## **6\. Target Audience**

The dashboard and notebook are intended for:

- **Hospital staff-** to determine the likelihood of a patient's mortality so that early and more effective treatment can be provided to those who need it.
- **Patients at risk-** Early planning and effective lifestyle choices in place to reduce the risk of mortality.

## **7\. User story**

As a data analyst student, I want to build a predictive machine learning model for patients with common illness or characteristics that lead to heart failure so that it can be used as a real-life practical example for hospitals and health care globally. I would like to think this model could potentially be the stepping stone to save a lot of lives .

## **8\. Data Transformation summary**

| Original Column | Transformation Applied | Feature engineering/ New column created | Purpose/Notes |
| --- | --- | --- | --- |
| age | Kept mostly unchanged but kept into bins for histograms in the jupyter notebook<br><br>Converted columns from float data type to integer | Integer data type | Age is usually not in decimals and is stated as a whole number |
| anaemia | Remains unchanged for notebook but changed to categorical values for dashboard | 0-> not anaemic<br><br>1-> anaemic | More efficient working for tooltips and labels on pie chart |
| creatinine_phosphokinase | unchanged | unchanged | Unchanged |
| diabetes | Remains unchanged for notebook but changed to categorical values for dashboard | 0-> not diabetic<br><br>1-> diabetic | More efficient working for tooltips and labels on pie chart |
| ejection_fraction | unchanged | unchanged | Unchanged |
| high_blood_pressure | Remains unchanged for notebook but changed to categorical values for dashboard | 0-> normal blood pressure<br><br>1-> high blood pressure | More efficient working for tooltips and labels on pie chart |
| platelets | unchanged | unchanged | unchanged |
| serum_creatinine | unchanged | unchanged | unchanged |
| serum_sodium | Unchanged | unchanged | unchanged |
| sex | Remains unchanged for notebook but changed to categorical values for dashboard | 0-> Female<br><br>1-> male | More efficient working for tooltips and labels on pie chart |
| smoking | Remains unchanged for notebook but changed to categorical values for dashboard | 0-> non-smoker<br><br>1-> smoker | More efficient working for tooltips and labels on pie chart |
| time | column dropped | \-  | Not useful for the analysis because the context of it was arbitrary |
| DEATH_EVENT | Renamed column title to remain consistent with other titles<br><br>Remains unchanged for notebook but changed to categorical values for dashboard | Column name changed to death_event<br><br>0-> survived<br><br>1-> died | More efficient working for tooltips and labels on pie chart |

## **9\. Expected deliverables**

**Jupyter notebook visualisation:** Seaborn and Matplot lib were chosen as visualisation tools. Since seaborn is built on top of Matplot lib provides good interface for creating attractive statistical graphs. While I used seaborn to plot most graphs in the notebook, to make it attractive and visually pleasing; I used mat plot lib to lot visuals that have more than one graph contained in it for simplicity and readability. I have not use plotly for this project as in order to view the graph it needs to be opened on a webpage and I would rather have all the graphs show up in one notebook.

- **Seaborn:** Heatmap of feature correlation with/without additional feature engineering, 1 distribution plot to analyse trend of death event against age and sex (Hypothesis 1), 2 scatter plots to understand the trend for serum creatinine and ejection fraction regarding a death event. (Hypothesis 2)
- **Matplot lib**: Distribution graphs for the features to understand the variance in the data.

Jupyter Notebook Machine learning model: The best predictive model for the study was found to be Random Forest classifier according to its accuracy and F1 score. A box plot and confusion matrix were used to determine which model would be the most accurate and check the performance of the predictive model. Both were plotted using **Matplot lib.** The overall accuracy of the predictive model was **65%.**

Dashboarding in Tableau: Link to the dashboard [Heart failure | Tableau Public](https://public.tableau.com/app/profile/bhavita.lacmane/viz/Heartfailure_17689426786760/Heartfailuredashboard?publish=yes)

The dashboard aims to provide more insight into the numbers of additional illnesses the patients had during the study. The numbers were expected as the average age of a patient was 60 and most patients had anaemia or diabetes. The Dashboard looked more into the functioning of the hear (like the notebook) and looked to uncover more trends about which patient died or survived. You can use the interactive filters on the left hand side to go into greater detail of your analysis.

## **10\. Ethics**

Ethical use of patient data requires protecting privacy, ensuring informed consent, minimising harm, addressing bias, and complying with data protection regulations such as GDPR. Transparency, security, and responsible interpretation are essential to maintain public trust and ensure ethical research outcomes.

As I have no insight in how data was collected, I assume Patient's privacy and confidentiality was protected. Patients were aware of how their data might be use. (UK Health Research Authority). Only the data truly required by the study was used and information about the patient remained anonymous. Something to consider is healthcare data is sometimes bias as some ethnic groups are under represented or the sex and age is imbalanced. Every aspect of this project was shared and any conclusion made from the project was noted. The data should not be used irresponsibly. If this project is to be use in real life applications it should seek appropriate approvals from bodies such as NHS Research Ethics and Committees.

Other considerations in real life applications of the project: The machine learning model is likely to make some errors and unnecessarily panic the hospital staff or patient and use up valuable time and resources. Alternatively, it could make an error of a patient being severely unwell, but getting it wrong where the fate of the patient could end in mortality, when it could be prevented. While the ML model can be beneficial it is always a good idea for a doctor to check results and be available for real world advise as it can provide a human element of comfort and care.

## **12\. How to run this project locally**

**Clone the Repository**

git clone \[<https://github.com/BhavitaL/heart_failure_clinical_study\>]

**Install Dependencies**

You will need a requirements.txt file listing pandas, numpy etc. Open your terminal or a Jupyter cell and run:

pip install -r requirements.txt

**Run the Notebook**

Open heart_failure_clinical_study.ipynb and run all cells sequentially. The notebook will automatically download the data, run the ETL pipeline, and generate all seaborn/matplotlib visualizations.

## **11\. Key findings and next steps**

- Hypothesis 1: while age showed the greatest correlation to death event, upon deeper analysis the impact of age on males seemed to be more significant
- Hypothesis 2: There was sufficient evidence that if serum creatinine levels increased and ejection fraction was low there was a likelihood that the patient would have died
- Hypothesis results could further be improved with parametric or non-parametric testing
- Machine Learning model gave a low accuracy of 65% which is not high enough to be used in a real-life scenario.
- Data quality could be improved by integrating more patient records or by adding additional feature engineering columns
- Alternative machine learning models could be tried and tested to compare overall performance
- Standardisation/ Normalisation of some highly skewed data features.

## **12\. Credits and Acknowledgments**

- AI agents such as Chat GPT, Co pilot and Google Gemini- used for debugging, fixing errors and research
- John Anih, Code institute instructor and teaching for code workbook on Machine Learning Part 1 and Part 2
- Stack Overflow- Graph visualisation code
- YouTube tutorial videos by Penguin Analytics and Mo Chen for basic guides on tableau
- Code Institute teaching materials from the 'Data Analytics with AI Bootcamp 2025'-Newham cohort course were used.
- Kaggle for providing the data set
