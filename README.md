# Accidents-Vs-Age
This project uses the dataset downloaded from kaggle.The dataset gives various kinds of information on the road accidents including the conditions in which the accidents occured.


The features taken from the dataset are skidding and over turning,hit object on carriageway, road surface conditions,hit object off carriage way and whether it is urban or rural areas. These features do not contain any null values and hence do not have to be cleaned. The y values or the labels are taken as the age of the casualty and the age of the driver. These contain null values , hence modification and cleaning of data is required.

The label values are modified into categorical data before passing it to the algorithm. For ex. if the age is below 20, we replace the value by 0, if it is greater than 20 and less than 40, we replace it by 1 and so on.. 
This makes sure that the algorithm considers a slight variation in the data as true while predicting the value.

Now that the cleaning and modifying of data is done, the X values and the y value should be passed to train_test_split module which splits the data into training and testing. Two algorithms each for age of casualty and age of driver is used which gives differnt predicted values and different outputs. 
After splotting the data, we use OnevsRestClassifier to find the predicted data.This algorithm fits one classifier per class.Each class is represented by only one classifier. 

The first model(age of casualty ) is around 70 percent. The train score is 68.4% and test score is 67.9% which are close values. The indicates that the model is neither overfitting nor underfitting. 
Similiarly, for age of driver, the accoracy is around 60% , the train and test score are 58.85 percent and 57.25 percent respectively. 
The accuracy of the model can be increased by consider more features, considering more trained and test data, but too high of an acccuracy can be a result of overfitting which is not preferred. 
After finding out the accuracy and predicted value, we now analyse the importance of the features or how much each feature contributes in the algorithm. On plotting the graphs we find that hit_object off caariage way contributes most to the algorithm and whether it the place is urban or rural contributes the least. This is found out by using the feature_importances_ function. 

Next by plotting graphs between different features and different labels, we find that,the age group of 20 to 40 are affected to a greater intensity from skidding and overturning etc. As no description is given in kaggle on the features, we assume that the features data represent intensity of accidents. Age group of 40 -60 (driver) is is more affected by bad road surfae conditions , while for the casualty age group of <20,20-40 and 40-60 are affected to the same extent in road surface conditions. This data might not be accurate as it is taken on predicted data which is 60-70% accurate. 
