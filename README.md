
# Summary
In this project I will fetch Baltimore City crime data to see if it can be used within models to be able to predict the weapon used in a given victim based crime.  The task at hand is to use classification models to classify the weapon used as one of: FIREARM, KNIFE, HANDS, OTHER.

# Goals

The question at hand here is if we can we predict what weapon will be used in a particular victim based crime.  This would benefit police officers by either knowing before the crime happens what to be on the lookout for/prepared for or after the fact for when they arrive on the scene to know what to expect ]/ be prepared for.

Based on a dummy model, if we simply predicted that every crime was commited with a FIREARM??? we would have an accuracy score of: 78.7%.

So, we will make it our goal to beat that accuracy score with out model.  Can we predict what weapon will be used in a particular crime with a higher accuracy rate than 78.7%

# Motivation and Background

The motivation in analyzing this data is to find patterns and trends in crimes as well as run predictive analytics so that we may learn more information and be better prepared to stop crime.  This can be useful in numerous ways.  For example, say police are expecting a crime in a certain location at a certain time, and know a general description of it - they could also try to predict what weapon will be used in the crime to know what they will be up against and be prepared.  If there is a crime expected and a firearm is likely to be used, police should be ready for a gun fight.  Secondly, say the crime already happened and the police officer recieved a call giving a general location, and description - when enroute to the crime and arriving on the scene it would be helpful for them to know what kind of weapon they are up against.  This information can inform the officer of whther or not the suspect is likely to be armed, and what kind of person they are going to have to deal with so that they may be best prepared for the situation.

# Data Description
[Baltimore City Crime Data](https://data.baltimorecity.gov/Public-Safety/BPD-Part-1-Victim-Based-Crime-Data/wsfq-mvij/data)

To perform this analysis, I will use a data set named "BPD Part 1 Victim Based Crime Data" from Open Baltimore.  This data is updated every Monday, with a 9 day time lag to minimize changes to the data as records move throughout the BPD review process.  I exported this data as a CSV file and began the cleaning of it from there.  The data contains 16 columns and 313,634 rows.  One limitation is that a lot of the weapons in the dataset are null, since for the purpose of this project our goal is to predict the type of weapon used, we will drop those rows with a null weapon.  These cases where the weapon is null include cases where it is fairly obvious that no weapon is really applicable such as a car theft where there was no intervention between people, just the car stolen; or a burglary where the suspect broke in somewhere and robbed the place without a weapon or any interaction with a victim.  For the purpose of this project we will focus on the victim based crimes where a weapon was used.  This leaves us with 66908 crimes to base our model on which should still be plenty.  Another limitation is that the weapon may be classified as only one of 4 categories: HANDS, KNIFE, FIREARM, OTHER.  With this, we can only predict one of those from this dataset and the OTHER category may not be too useful for an officer to know about.  But the cases of knowing when a FIREARM / KNIFE / HANDS are used would be very useful it is still a very important prediction as that informaiton is vital to saving lives on the streets of Baltimore.

# Summary of Files

**Data Source:**
<br>
[Baltimore City Crime Data](https://data.baltimorecity.gov/Public-Safety/BPD-Part-1-Victim-Based-Crime-Data/wsfq-mvij/data)


**Python Notebooks:**
<br>
[Data Load and Clean](https://github.com/zvance1/predict-crime/blob/main/notebooks/load_and_clean.ipynb)
<br>
[Data Exploration](https://github.com/zvance1/predict-crime/blob/main/notebooks/explore.ipynb)
<br>
[ML Data Analysis](https://github.com/zvance1/predict-crime/blob/main/notebooks/ml-analysis.ipynb)
Note: Not all exploratory analysis made it into the final techincal report - only what I saw as most relevant.
<br>
[Technical Notebook](https://github.com/zvance1/predict-crime/blob/main/notebooks/technical_report.ipynb)

**Data Folder (all data in csv format, used in our final python notebooks):**
<br>
[Data](https://github.com/zvance1/predict-crime/tree/main/data)

**Data Visualizations Folder (all visualizations used in our final python notebook):**
<br>
[Data Visualizations](https://github.com/zvance1/predict-crime/tree/main/images)

**Python Folder (python technical report notebook, notebook for the ML analysis, and one for cleaning):**
<br>
[Python Files and Notebooks](https://github.com/zvance1/predict-crime/tree/main/notebooks)


# Project Info
<pre>
Contributors : <a href=https://github.com/zvance1>Zach Vance</a>
</pre>

<pre>
Languages    : Python3
Tools/IDE    : Anaconda, Jupyter Notebook
Libraries    : pandas, sklearn, matplotlib
</pre>

<pre>
Duration     : September 2020
Last Update  : 10.29.2020
</pre>