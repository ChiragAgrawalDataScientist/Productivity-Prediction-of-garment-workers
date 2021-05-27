# Productivity-Prediction-of-garment-workers

<img src = "https://github.com/ChiragAgrawalDataScientist/Productivity-Prediction-of-garment-workers/blob/master/images/Growth.png" width = "1000" height = "300">


The Garment Industry is one of the key examples of the industrial globalization of this modern era. It is a highly labour-intensive industry with lots of manual processes. Satisfying the huge global demand for garment products is mostly dependent on the production and delivery performance of the employees in the garment manufacturing companies. So, it is highly desirable among the decision makers in the garments industry to track, analyse and predict the productivity performance of the working teams in their factories

e-mail :- chiragagrawal196@gmail.com <br>
LinkedIn :- https://www.linkedin.com/in/chirag-agrawal-0bb939182/ <br>

## Files Description
### Data
- <strong>garments_worker_productivity.csv</strong> :- The initial training data downloaded from kaggle. <br>
- <strong>garments_cleaned_train_data.csv</strong>  :- cleaned data after EDA and Preprocessing. <br>

### Jupyter Notebooks
- <strong>Productivity_EDA_and_Preprocessing.ipynb</strong>           :- All the EDA and preprocessing work done in this file. <br>
- <strong>Models_and_tuning_Garments_Data.ipynb</strong>              :- This file includes the different model tunings to find the best model.<br>
- <strong>Productivity_Prediction_system_Complete_code.ipynb</strong> :- This is the whole code combined with the final model.<br>

### Other important file
- <strong>catboost.pickle</strong> :- The final model stored in a pickle format.<br>

## Discussion

#### Lets Discuss about this data and what I have done to get the my final model.

This data is downloaded from <a href= "https://www.kaggle.com/ishadss/productivity-prediction-of-garment-employees">kaggle.com .</a><br>
While working on this dataset, I was introduced to some new concepts for better cleaning the data.<br>
For Missing value imputation I was introduced with concept of MissForest.<br>
For Data encoding, BaseN encoding, TargetEncoding, CatBoostEncoding.<br>
For data Modeling, CatBoost.<br>

Lets dive in to understand the data and I will also compare the findings of all concepts that was new for me.<br>
So, lets see what our data is:
Our data looks like this:
<img src= "https://github.com/ChiragAgrawalDataScientist/Productivity-Prediction-of-garment-workers/blob/master/images/head.PNG">

It has 1197 data instances and 15 columns<br>
#### Features description
Attribute Information:

<strong>01 date :</strong> Date in MM-DD-YYYY<br>
<strong>02 day :</strong> Day of the Week<br>
<strong>03 quarter :</strong> A portion of the month. A month was divided into four quarters<br>
<strong>04 department :</strong> Associated department with the instance<br>
<strong>05 teamno :</strong> Associated team number with the instance <br>
<strong>06 noofworkers :</strong> Number of workers in each team <br>
<strong>07 noofstylechange :</strong> Number of changes in the style of a particular product<br>
<strong>08 targetedproductivity :</strong> Targeted productivity set by the Authority for each team for each day. <br>
<strong>09 smv :</strong> Standard Minute Value, it is the allocated time for a task<br>
<strong>10 wip :</strong> Work in progress. Includes the number of unfinished items for products<br> 
<strong>11 overtime :</strong> Represents the amount of overtime by each team in minutes<br>
<strong>12 incentive :</strong> Represents the amount of financial incentive (in BDT) that enables or motivates a particular course of action.<br>
<strong>13 idletime :</strong> The amount of time when the production was interrupted due to several reasons <br>
<strong>14 idlemen :</strong> The number of workers who were idle due to production interruption<br>
<strong>15 actual_productivity :</strong> The actual % of productivity that was delivered by the workers. It ranges from 0-1.<br>

Some of its features have outliers. With a single columns have 47% missing values. Generally we delete such columns with so much missing values but as I am not from this data domain, so I need to check whether this feature is important or not before deleting. <br>

After some EDA, it was the time to encode some(3) features. When I LabelEncoded it, the department column became highly multicollinear with some other columns. So, I decided to use some other encoding method




