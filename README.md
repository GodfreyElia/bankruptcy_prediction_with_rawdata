## Title: Predicting Failure of Johannesburg Stock Exchange Companies Using Machine Learning

#### 1. Description
The dynamic nature of the contemporary business environment has made corporate failures commonplace, and so raised the alarm for corporation to start considering their going concern seriously. On the higher end, all sorts of businesses can benefit from knowing their likelihood of failure with a good degree of statistical certainty. In this project I adopt and compare 7 different techniques of predicting bankruptcy, namely:

  (i). Machine Learning - Ensemble
  
    1. Random Forest
    2. Gradient boosting
    3. Bagging
    
  (ii). Machine Learning - Base Learner
  
    4. Support Vector Machines (SVM)
    5. Artificial Neural Networks (ANN)

  (iii). Traditional Statistical Methods
  
    6. Logistic regression

  (iv). Other
  
    7. k-Nearest Neighbours

#### 2. Data

Dataset:
   
This project has employed financial statements data of 512 Johannesburg Stock Exchange companies (270 dead and 242 alive) obtained from DataStream database. The companies represent 11 different industries including industrials, financials, and consumer services. 

Furthermore, the data spans 25 years spanning 1997 and 2022. This has been done deliberately to capture the impact of the two prominent global crises, namely: the financial crisis of 2008 and the Covid 19 pandemic of 2019, on the predictive ability of the models being studied.

<br clear="both">

<div align="Left">
  <img height="60%" width="60%" src="https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/blob/main/Files/Industries%20Summary.png"  />
</div>
<br>

Variables:

The below lists down all the independent variables used in this project. The dependent variable was a dummy variable called 'Bankruptcy' whereby 0 represented live companies and 1 represented defunct companies.

<br clear="both">

<div align="Left">
  <img height="60%" width="60%" src="https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/blob/main/Files/Variables.png"  />
</div>
<br>

Sampling procedure:

This project’s target population was all JSE companies currently existent on the exchange and those companies that delisted from the exchange between 1997 and 2022.  An initial sample consisting of 967 JSE companies was drawn from the DataStream database to begin with. Among the 967 companies, 721 companies had been delisted from the exchange between 1997 and 2023 for various reasons including bankruptcy. The rest of the companies, 246, were still listed on the exchange. The paper applied the following criteria to select the final pool of companies to use in model training, validation, and testing:

    1.	The company was still alive or had been delisted on the exchange between 1997 and 2022.
    2.	All the companies have at least five years of data available (see the attached image for a concession on this).
    3.	Those delisted, had been delisted because of bankruptcy and not any other causes such as mergers or being acquired by another company.

<br clear="both">

<div align="Left">
  <img height="60%" width="60%" src="https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/blob/main/Files/Sample%20Selection%20Process.png"  />
</div>
<br>

#### 3. Exploratory Data Analysis

Exploring our data allows us to form judgements on the nature of our data and distribution of our variables. This is inviriable in any statistical and modeling undertakingas as it enables the analyst to gauge the suitability of the descriptors for the task at hand. In this project, I use two main methods of exploring our data, namely: descriptive statistics and graphical visualisation. 
<br>

3.1. Descriptive Statistics

Descriptive statistics offers a tremendous way of appreciating how our data is spread across the descriptors. The main summary statistics explored in this project include measures of central tendency, location, and dispersion.

<br clear="both">

<div align="Left">
  <img height="60%" width="60%" src="https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/blob/main/Files/Summary_Stats.jpg"  />
</div>
<br>

3.2. Graphical Visualisation

Presenting our data visually complements summary statistics by enabling us the opportunity to appreciate the distribution of our data visually. Thus we can solidify our judgements and conclusions regarding the nature of our data. In this project, I use an array of visualisations to understand the data more clearly before using it for any analysis and modeling.

  3.2.1.  Distribution of Companies by Industry
<br clear="both">

<div align="Left">
  <img height="60%" width="60%" src="https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/blob/main/Files/Industry_Distribution.png"  />
</div>
<br>

Briefly, one can safely conclude that there are by far many financials and industrials companies represented in the dataset than any other industry. This observation is crucial as financial statements and hence variables vary significantly by industry.

3.2.1  Age Distribution of Companies by Industry.
<div align="Left">
  <img height="60%" width="60%" src=![image](https://github.com/GodfreyElia/bankruptcy_prediction_with_rawdata/assets/92586834/62e26e0f-37d8-4fcb-a6db-869371d4a3a8)  />
</div>
<br>


