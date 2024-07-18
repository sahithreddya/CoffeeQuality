# CoffeeQuality
As an amateur in home brewing coffee, I am always fascinated by the amount of variables that affect the final cup of coffee. I came across a coffee dataset and started this project with the goal to get some insights into the factors that affect coffee quality.
<p align="center"><img src="https://dfamgkk1duyqq.cloudfront.net/wp-content/uploads/2020/04/farmer-picking-coffee-cherries.jpg.webp" width="50%" alt="coffee farmer collecting coffee fruit"/></p>

## Initial Dataset
<p align="center"><img src="https://github.com/user-attachments/assets/e645e57d-d423-44e6-8beb-d82903b8a6d0"/></p>

## Exploratory Data Analysis
### Looking at data distribution for all numeric variables
Most of the variables seem to have a healthy bell curve. The variables without bell curves will be looked at again after a correlation matrix is created. 
<p align="center"><img src="https://github.com/user-attachments/assets/dfbae0c8-8b22-4913-ba27-dba8d72b6b61" width=600/></p>

### Visualizing Average Total Cup Points by Country
>_Total Cup Points_ is the value which tells us the quality of the coffee bean.

The average __Total Cup Points__ value for each country seems to be very close to each other. This is apparent in the __low Standard Deviation__ value seen above. This means that the overall quality of coffee in this dataset is towards the higher end. This also means that differentiating the quality between two cups will be a challenge for any _Q Grader_(a professional coffee taster).

<div style="display: flex; justify-content: center" align="center"><img src="https://github.com/user-attachments/assets/04f270c0-692a-44c7-bf9c-dffeb0222f7c" width="45%"/><img src="https://github.com/user-attachments/assets/1eb2eb3b-a14c-4dc5-b601-25c16a38e296" width="45%"/></div>

### Visualizing Average Altitude of each Country where Coffee is grown
The average altitude of fields where coffee is grown is greatest in Vietnam and least in Taiwan.

<div style="display: flex; justify-content: center" align="center"><img src="https://github.com/user-attachments/assets/0def31e4-2fd2-4b93-abab-9e993b7d1a0c" width="45%"/><img src="https://github.com/user-attachments/assets/02bba2e6-3d5b-456b-b1da-0db54426c9ad" width="45%"/></div>

### Visualizing no. of Unique Coffee types from each country
Interestingly, Taiwan has the most coffee types in this dataset by a mile. After doing some research, Taiwan is not even in the top 10 of most coffee producing nations in the world. This means it is important to keep in mind that the data in this dataset cannot be relied on for making general assumptions towards coffee quality.

<div style="display: flex; justify-content: center" align="center"><img src="https://github.com/user-attachments/assets/216e99c4-7317-4aba-9d41-d028ff418536" width="45%"/><img src="https://github.com/user-attachments/assets/1d4eb30d-e5bb-448f-988e-f690e9789c81" width="45%"/></div>

### Looking at the top 10 countries in this dataset with the most coffee production
<div style="display: flex; justify-content: center" align="center"><img src="https://github.com/user-attachments/assets/8c7c9456-1e8b-4aad-b1b7-e5e1497b1c65" width="45%"/></div>

### Visualizing the average coffee tasting factors for each of the above 10 countries
It is seen in the below radar charts that __Ethiopia__ has the largest area of pentagon when it comes to the 5 tasting factors of coffee quality.

>__Reading the Chart__: The value of each factor ranges from the center of the pentagon(lowest) to the extremeties of the pentagon(highest). The country having the most area of its pentagon would mean that the average tasting factor quality is the highest for the respective country.
<div style="display: flex; justify-content: center" align="center">
  <img src="https://github.com/user-attachments/assets/7cd6b935-32b8-45c6-89e6-a6e0cc7f938f" width="20%"/>
  <img src="https://github.com/user-attachments/assets/17df2f1f-a001-4b1d-9947-b02938de6bcd" width="20%"/>
  <img src="https://github.com/user-attachments/assets/1b0597d3-2a54-4e13-8c85-09de617b76a9" width="20%"/>
  <img src="https://github.com/user-attachments/assets/ca8bf836-0e83-4150-b5e4-d251d1ccb7e2" width="20%"/>
  <img src="https://github.com/user-attachments/assets/58f5d6f1-73c9-471d-a64d-8c4de23e25c4" width="20%"/>
  <img src="https://github.com/user-attachments/assets/1d193e15-27f4-4f9c-a2ca-71b7ef184f4d" width="20%"/>
  <img src="https://github.com/user-attachments/assets/7738d3df-b605-4b20-8afd-a844a2821e76" width="20%"/>
  <img src="https://github.com/user-attachments/assets/999462ae-c4a8-4c30-a347-ee2943685505" width="20%"/>
  <img src="https://github.com/user-attachments/assets/6e97fa71-a806-4f32-bf8a-7d3a5fa2b4c5" width="20%"/>
  <img src="https://github.com/user-attachments/assets/dc1c564b-4095-40dd-a64a-d5aca9c3d2e1" width="20%"/>
</div>

### A correlation matrix to predict Total Cup Points
It is apparent with the below correlation matrix that Total Cup Points is positively affected by some factors.
- The variables _Aroma, Flavor, Aftertaste, Acidity, Body, Balance,_ and _Overall_ positively have a strong positive correlation with __Total Cup Points__.
- The variables _Quakers_ and _Category Two Defects_ have a weak negative correlation __Total Cup Points__.
<div style="display: flex; justify-content: center" align="center">
  <img src="https://github.com/user-attachments/assets/c86bd88c-9230-4404-8a4e-6750193a6140" width="70%"/>
</div>

## Predicting Total Cup Points using Linear Regression
### Plotting the attribute relation with Total Cup Points
<div style="display: flex; justify-content: center" align="center">
  <img src="https://github.com/user-attachments/assets/9936cc5a-030f-4aa8-b0a7-e1605c2e0ef6" width="60%"/>
</div>

### OLS Regression Results
<div style="display: flex; justify-content: center" align="center">
  <img src="https://github.com/user-attachments/assets/31f57ebe-602d-49d8-8a4f-e6696528b4ed" width="60%"/>
  <img src="https://github.com/user-attachments/assets/fc4e9275-25f2-49fd-ae1c-27987438903c" width="30%"/>
</div>

- The R2 value is almost close to 1, indicating that the relationship of factors we've considered is very strong.
- The addition of _const_ variable shows the lack of relation to _Total Cup Points_ as its __coef__ and __std err__ values are very high - The R2 value is almost close to 1, indicating that the relationship of factors we've considered is very strong.
- The addition of _const_ variable shows the lack of relation to _Total Cup Points_ as its __coef__ and __std err__ values are very high 

As expected from a 99% r2 score, the actual v/s predicted graph is almost a straight line.

***
<div style="display: flex; justify-content: center" align="center">
  <h1>Thank you!</h1>
  <img src="https://i0.wp.com/blog.beangenius.com/wp-content/uploads/2015/05/giphy-1.gif" width="40%"/>
</div>
