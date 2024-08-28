# Bike-sharing-assignment
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

# General Information
   A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 
   
### The company wants to know:
- Which variables are significant in predicting the demand for shared bikes.
- How well those variables describe the bike demands

## Technologies Used
- numpy - version 1.20.3
- pandas - version 1.3.4
- matplotlib - version 3.4.3
- plotly - version 5.6.0
- seaborn - version 0.11.2
- statsmodels - version 0.12.2
- sklearn - version 0.24.2
- scipy - version 1.7.1   

Observations & Insights:
![image](https://github.com/user-attachments/assets/7a053483-972a-4ce3-8ea6-82a91b263d04)

There are four types of weathersit viz., 1. Clear, 2. Mist, 3. Light Snow, 4. Heavy Rain
Weathersit – After looking at box plot we can observe that clear weather situations are good, while mist weather situations mean is lower than clear weathersit. 
Post creating linear regression equation we can observe following:
Light Snow (3) has major negative impact with coefficient of -0.28. Which means whenever there is light snow, it has negative impact on bike sharing cnt. 
Mist cloud (2) also has negative impact with coefficient of -0.07. This has lower impact than light snow, but still significant and should be considered. 
Clear (1) does not have significant impact in predicting dependent variable i.e., cnt
Heavy Rain (4) was not observed in the dataset

Season – After looking at box plot mean is highest for Fall (3), followed by Summer (2), then Winter (4) and then Spring (1).
Post creating linear regression equation we can observe following:
Spring (1) has negative impact with coefficient of -0.11. Which means customers do not prefer bike sharing in spring season 
Winter (4) has positive impact with coefficient of 0.04. Which means customers prefer bike sharing more in winter season compared to others
Summer (2) is neutral and hence not taken in linear regression model
Fall (3) is neutral and hence not taken in linear regression model

yr – After looking at box plot mean is high for yr (1), followed by yr (0).
Post creating linear regression equation we can observe following:
yr has positive impact with coefficient of 0.23. Which means bike sharing has gained popularity from 2018 -> 2019.  

mnth – After looking at box plot mean increases to mid year and then drops again.
Post creating linear regression equation we can observe following:
mnth does not have any significance in predicting cnt.  

holiday – After looking at box plot mean is higher for 0 and lower for 1.
Post creating linear regression equation we can observe following:
Holiday has negative impact in predicting cnt with coefficient of -0.0892.

Workingday, weekday – not much insights coming out of box plot or regression.  

Overall inference for categorical variables:
1.	It is observed that popularity has increased year over year. 2018 -> 2019. Hence, once situation stabilizes, company can expect increase in bike sharing business
2.	On holidays, there is less demand
3.	Weathersit light snow has negative impact on business
4.	Weathersit mistcloud has negative impact on business
5.	Season spring has negative impact on business
6.	Season winter has positive impact on business and this time can be used to promote business

Based on the final model, three most important predictors are following:
1. Temp (0.42): This shows that favourable higher temperatures days have high demand of the shared bikes 
2. Weathersit (3) Light Snow (-0.28): This shows that whenever there is snow, rain, thunderstorms, scattered cloud, customers do not prefer bike sharing. Which means unfavourable weather situation has negative impact on demand of the shared bikes 
3. Yr (0.23): Positive 0.23 indicates that year on year, popularity and demand of the shared bike has increased
These are the top 3 features contributing significantly towards explaining the demand of the shared bikes.



## Conclusion
There are **8** Significant variables to predict the demand for shared bikes

- Year
- holiday
- temp
- windspeed
- weathersit(Light Snow)
- weathersit (Mist + Cloudy)
- Season (Spring)
- Season (Winter)
