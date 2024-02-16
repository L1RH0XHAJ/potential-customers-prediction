# Prediciting potential customers for ExtraaLearn

## Part of MIT IDSS's "Data Science and Machine Learning: Making Data-Driven Decisions" program


Note: The project can be accessed through the provided HTML or the Jupyter Notebook file.   

### Context

The EdTech industry has been surging in the past decade immensely, and according to a forecast, the Online Education market would be worth $286.62bn by 2023
with a compound annual growth rate (CAGR) of 10.26% from 2018 to 2023. The modern era of online education has enforced a lot in its growth and expansion beyond 
any limit. Due to having many dominant features like ease of information sharing, personalized learning experience, transparency of assessment, etc, it is now preferable to traditional education.

In the present scenario due to the Covid-19, the online education sector has witnessed rapid growth and is attracting a lot of new customers. 
Due to this rapid growth, many new companies have emerged in this industry. With the availability and ease of use of digital marketing resources, 
companies can reach out to a wider audience with their offerings. The customers who show interest in these offerings are termed as leads. There are
various sources of obtaining leads for Edtech companies, like

* The customer interacts with the marketing front on social media or other online platforms.
* The customer browses the website/app and downloads the brochure
* The customer connects through emails for more information.

The company then nurtures these leads and tries to convert them to paid customers. For this, the representative from the organization connects with the lead on call or through email to share further details.

## Objective

ExtraaLearn is an initial stage startup that offers programs on cutting-edge technologies to students and professionals to help them upskill/reskill. 
With a large number of leads being generated on a regular basis, one of the issues faced by ExtraaLearn is to identify which of the leads are more likely to convert so that they 
can allocate resources accordingly. 


The goals of this project is to:
* Analyze and build an ML model to help identify which leads are more likely to convert to paid customers,
* Find the factors driving the lead conversion process
* Create a profile of the leads which are likely to convert
* Provide conclusions of the potential customers analysis to ExtraaLearn  

### Techniques applied

* Data cleaning and exploratory data analysis using: histograms, boxplots, barplots/countplots, heatmaps/correlation matrices, and pairplots.    
* Classification and Hypothesis Testing
* Decision Trees
* Random Forest

### Data Dictionary

- `ID`: ID of the lead
- `age`: Age of the lead
- `current_occupation`: Current occupation of the lead. Values include 'Professional','Unemployed',and 'Student'
- `first_interaction`: How did the lead first interacted with ExtraaLearn. Values include 'Website', 'Mobile App'
- `profile_completed`: What percentage of profile has been filled by the lead on the website/mobile app. Values include Low - (0-50%), Medium - (50-75%), High (75-100%)
- `website_visits`: How many times has a lead visited the website
- `time_spent_on_website`: Total time spent on the website
- `page_views_per_visit`: Average number of pages on the website viewed during the visits.
- `last_activity`: Last interaction between the lead and ExtraaLearn.
  - ***Email Activity***: Seeking for details about program through email, Representative shared information with lead like brochure of program , etc
  - ***Phone Activity***: Had a Phone Conversation with representative, Had conversation over SMS with representative, etc
  - ***Website Activity***: Interacted on live chat with representative, Updated profile on website, etc
- `print_media_type1`: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Newspaper.
- `print_media_type2`: Flag indicating whether the lead had seen the ad of ExtraaLearn in the Magazine.
- `digital_media`: Flag indicating whether the lead had seen the ad of ExtraaLearn on the digital platforms.
- `educational_channels`: Flag indicating whether the lead had heard about ExtraaLearn in the education channels like online forums, discussion threads, educational websites, etc.
- `referral`: Flag indicating whether the lead had heard about ExtraaLearn through reference.
- `status`: Flag indicating whether the lead was converted to a paid customer or not.

### Dependecies 

Install/import the following libraries for:
- 
  - *pandas*
  - *numpy*
  - *matplotlib.pyplot* 
  - *seaborn* 
# To tune model, get different metric scores, and split data
from sklearn import metrics
from sklearn.metrics import r2_score, mean_squared_error, mean_absolute_error

from sklearn.model_selection import train_test_split, StratifiedKFold, cross_val_score

# To be used for data scaling and one hot encoding
from sklearn.preprocessing import StandardScaler, MinMaxScaler, OneHotEncoder, LabelEncoder

# To impute missing values
from sklearn.impute import SimpleImputer

# Importing the Machine Learning models we require from Scikit-Learn
from sklearn import tree;
from sklearn.tree import DecisionTreeClassifier;
from sklearn.ensemble import RandomForestClassifier;

# To help with model building
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import (
    BaggingRegressor,
    RandomForestRegressor,
    GradientBoostingRegressor,
    AdaBoostRegressor,
    StackingRegressor,
)

# Importing the other functions we may require from Scikit-Learn
from sklearn.model_selection import train_test_split, GridSearchCV, RandomizedSearchCV;
from sklearn.metrics import recall_score, roc_curve, classification_report, confusion_matrix;
from sklearn.preprocessing import StandardScaler, LabelEncoder, OneHotEncoder;
from sklearn.compose import ColumnTransformer;
from sklearn.impute import SimpleImputer;
from sklearn.pipeline import Pipeline;
from sklearn import metrics, model_selection;

### Using the code

Please make sure to save the Jupyter Notebook (*.ipynb*) file and the ***foodhub_order.csv*** dataset in the same directory.
