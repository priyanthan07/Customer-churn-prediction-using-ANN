# Customer-churn-prediction-using-ANN
The main focus of this project is to predict the customer churn of the organization. 

## Required libraries
      => tensorflow
      => keras
      => matplotlib
      => numpy
      => pandas
      => sklearn
      => seaborn

## Data
     customer_churn.csv

## Data preprocessing
     => Dropped unwanted columns. ex: customerID
     => Replaced "yes" or "no" values with "0" and "1".
     => Replaced "male" or "female" values with "0" and "1".
     => Create dummies using Pandas for the required columns. 
     => Sclaing tenure, monthlycharges, totalcharges columns using MinMaxScaler

## Model building
     model = keras.Sequential([
         keras.layers.Dense(20, input_shape=(26,), activation="relu"),
         keras.layers.Dense(15, activation="sigmoid"),
         keras.layers.Dense(1, activation="sigmoid")
     ])

## Compile
     model.compile(optimizer = "adam",
             loss = "binary_crossentropy",
             metrics = ["accuracy"])

## Evaluation
     loss: 0.4662 
     accuracy: 0.7690

## Classification_report
     precision    recall  f1-score   support

           0       0.81      0.88      0.84       999
           1       0.63      0.50      0.56       408

    accuracy                           0.77      1407
    macro avg       0.72      0.69     0.70      1407
    weighted avg    0.76      0.77     0.76      1407


  
    
  

     
