## Data Science Take Home Challenge 1: Relax Challenge

### Author Julia Hu
## Summary of Findings 

### Key solution step 1:

  <li> <b>(1) Load data and process the time series columns for the first csv file</b>: 
  <li> <b>(2) Convert datetime to a readable format

### Key solution step 2:

  <li> <b>(1) Load data and process the time series columns< for the second csv file/b>: 
  <li> <b>(2) Convert datetime to a readable format, and remove the hour, minute and second info
  <li> <b>(3) calculate total number of membership enrollment date
  <li> <b>(4) calculate total number of time visited
  <li> <b>(5) calculate total number of time visited
    
### Key solution step 3: 

 <li> <b>(1) Use rolling window to calculate number of visit within each rolling 7 days. 3D_visit_count
 <li> <b>(2) Define adopted user as who visited 3 times in any 7 days
 <li> <b>(3) Merge the adopted user table with the original user dataframe, and create 'Label' for machine learning
    
### Key solution step 4:

 <li> <b>(1) Further Feature engineering to drop unnecessary features, 
 <li> <b>(2) Time dependant feature engineering: if the id invited any new user or not, total time enrolled in the membership, number of time visited during the membership
 <li> <b>(3) One-hot-encoding for categorical feature

### Key solution step 5:
 <li> <b>(1) Use XGBoost for initial prediction, very high accuracy, 99.6%, AUC score
 <li> <b>(2) Hyperparameter tuning for XGBoost: The final AUC score is 99.68%
 <li> <b>(3) List the feature importance. The importance of features are ranked as: 1. Total number of time visited 2. average visit time interval 3. total amount of time involved in membership, 4. org_id, 5. invite_or_not, 6. opted for email, 7. Membership enrollment method.
 <li> <b>(4) Data exploration: Plotted relationship between adopted and unadopted user with all features. From data exploration, it can be seen that total number of time visited has a positive impact on adopted or not, while average vist time interval has a negative impact on adopted or not. 
