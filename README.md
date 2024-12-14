# Team-Lazy-Foodies

 Predicting The Price Of A Flight Ticket
With The Use Of Machine Learning
Algorithms


Dataset link :https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh


Flight ticket prices can be something hard to guess, today we might see a price, check out the price of the same flight tomorrow, and it will be a different story.To solve this problem, we have been provided with prices of flight tickets for various airlines between the months of March and June of 2019 and between various cities, using which we aim to build a model which predicts the prices of the flights using various input features.

Description of the dataset :So our Data consist of  11 columns and 10683 rows
and has colunms
 1    Airline          
 2   Date_of_Journey  
 3   Source           
 4   Destination      
 5   Route            
 6   Dep_Time         
 7   Arrival_Time     
 8   Duration         
 9   Total_Stops      
 10   Additional_Info  
 11  Price     
 
 
 Data Preprocessing : Our data consisted of quite a few null values. To solve the problem of missing values, we followed the following steps : 
We will check whether the data contains any null values so that there are no discrepancies in our data by which we can predict precisely. And clean with no Nan values.
It can be observed that Date_of_Journey , Dep_Time and Arrival_Time have been assigned as object by default. We will convert this data type into a timestamp to use this column for prediction.Then Separate the column “Date_of_Journey” into “journey_day” and “journey_month”.And then delete the Date_of_journey as it is not useful. 
The third step Now we will be dealing with the “ Dep_time” and Arrival_Time”and fetching fetching minutes and hours.In some cases there are no hours and min so we replace it by ‘0 h’ and ‘0 m’ 


After performing a few visualizations to understand our data better, we split the data into 80% training data and 20% test data. Next, we used Machine Learning models to fit the data.


The various regression algorithms used to build the model are : linear regression, random forest regression ,DecisionTreeRegressor, KNN algorithm


1)Linear regression : Simple linear regression involves only one dependent and one independent variable. It can be represented as :

Y = a + bX (1)

where X is the independent variable and Y is the dependent variable. b represents the slope of the line and a is the intercept.

2)Random forest regression : The random forest regression algorithm combines the decisions and forms a sequence of base models. The model is formulated as follows :

g(x)=f0(x)+f1(x)+f2(x)+... (2)

where g is the sum of the base models 

3)KNN Regression : A simple implementation of KNN regression is to calculate the average numerical target of the K nearest neighbours.

After modeling the data,Before hyper tuning  the regression score of random forest was 80.00 After hyper tuning , the regression score is 83.5 
