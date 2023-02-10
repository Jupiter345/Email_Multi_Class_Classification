# Foundation of Machine Learning - Multi-class Email Classsification Based on Meta-Data

## Multi-Class Email Classification
## Team name - ‘PlanetFood’

### Problem Definition
We often face the problem of searching meaningful emails among thousands of promotional emails. This project focuses on creating a multi-class classifier that can classify an email into different classes namely, Updates, Personal, Promotions, Forums, Purchases, Travel, Spam, and Social based on the metadata features extracted from the email.

### Dataset Description
The metadata extracted from the dataset of emails contains information on the date received, sender’s organization, top level domain of the organization, number of ids in cc, flag denoting if this mail is part of bcc list. The mail type denotes if a mail has just plain text or any further additional image/hyperlinks. The count of images and count of URLs in the mail is given. Finally flags denoting if there is a salutation in the mail and if the designation of the sender is mentioned have been captured.

### Process Overview
1. Understanding the data and data wrangling
* Checking for missing values and imputing them (mean for numeric and mode for categorical data)
* Cleaning of columns with string datatype
* Feature engineering was performed for date, org, and the tld columns for standardizing the data columns
* Importance of all features was checked.
2. Model selection
* Using the “LazyClassifier” method from the “lazypredict” package to see which model performs well
* Boosting algorithms worked best so we tried two – XGBoost, and Catboost (since most of the data is categorical)
* Label encoder was used to transform the categorical data for XGBoost and neural network.
3. Model tuning
* For Catboost, the inbuilt “randomized search” method was used
* For XGBoost, the GridsearchCV method was used.
4. Model training and evaluation
* Trained the 3 different models to predict the class of the emails
* Calculated the respective F1 scores.

### Team Members
* Pallav SAHU - pallav.sahu@student-cs.fr
* Akshay SHASTRI - akshay.shastri@student-cs.fr
* Anmol KATIYAR - anmol.katiyar@student-cs.fr
* Arun JEGATHESH - arun.jegathesh@student-cs.fr
