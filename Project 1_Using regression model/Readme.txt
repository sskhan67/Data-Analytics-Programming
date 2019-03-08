Project Title: The Electrical Power Predication of Combined Cycle Power Plant using Regression Model

1. Objectives:
The demand for electrical power is growing rapidly. To meet the customer's requirements, the prediction of power plant output has gained researchers in recent days. Previously, the intuitive method has been used to estimate the power plant output. But the rise of machine learning algorithm it becomes available to predict the output in beforehand.

The purpose of this project is to predict the power plant power generation using a machine learning method. The study could be beneficial for power plant manager, transmission and distribution company i.e. Pacific Gas and Electric Company (PG&E). 
The electric power generation, transmission, and distribution board work together to supply electricity to the end users. To do so, the transmission and distribution company analyze the power demands so that they can continue the supply without intervention. The calculated demand is sent to several power plants authority by informing their real-time demand. Based on the power plant capacity and the required demand for transmission and distribution company, the power plant authority decides to produce the electrical power. The generated electrical power is constrained on several conditions of the power plant. Those parameters and their relations with output generation are the main subjects of this study. The predicted output will help the power plant authority to cope with power demand.

Project Report:
Introduction:

The demand of electricity has been increasing day by day. To meet up the power demand, the need of set up different power plants are necessary as well as it is necessary to operate the existing power plant in maximum operating condition. Because the operating cost of power plant is high. If power plant does not operate at highly efficient way, the operating cost will increase that will affect profit maximization.

In our project, we have used the dataset for combined cycle power plant. The power plant produces the electricity. The generated power is transmitted and distributed by transmission and distribution company i.e. PG & E. The power producing company (power plant) produces electrical power in according to the actual demand by transmission and distribution company. The company like PG & E calculates the real time load using old data. Then, transmission and distribution company send their actual demand to the power plant.

The power authority knows their maximum production capacity, but the actual producing varies time to time. It also depends on several parameters such power plant temperature, pressure, humidity, and exhaust vacuum. In our case, we have considered the combined cycle power plant. That’s means the power plant has two types of fuel. One type of the fuel is natural gas. As we know our high science that natural gas is affected by temperature, pressure, and natural gas turbine humidity. The other type of fuel is steam. The steam turbine is affected by plant exhaust vacuum. If we look into our dataset, we will find that our dataset has all of the above-mentioned parameters.

Objectives:

The objective of this study is to build machine learning model to predict the power plant generated electrical power. There are existing methods that we can use to predict the output power. For example, the thermodynamic model requires to solve several linear and non-linear equations. To solve those equation, it requires huge computational power and time. Therefore, machine learning is another alternative approach to predict the output power. The machine learning method analyzes the arbitrary input and output based on correlation.

Dataset: Our dataset contains five columns and near 10000 rows those are collected over 6 year’s time period. The input variable are AT (Ambient temperature), relative humidity (RH), AP (Ambient pressure), and V (Vacuum) that are considered as independent variable. PE (electrical power) is response variable in our case.

Dataset may contain irrelevant data. We need to get rid of those data. We have analyzed each parameter data range and found reasonable except relative humidity. RH contains value higher than 100% which seems irrelevant. Therefore, we have deleted those rows that contains meaningless data.

Before developing the linear regression model, it is worthy to look into how variables have correlated each other as well as target variable. The covariance statistics indicate that the variables are not independent. The highest correlation among input features is between T and V (0.84). The highest correlations with target variable are also observed with T (- 0.95) and V (-0.87).

Linear Regression Model:

There are two types of regression model: simple linear regression and multiple linear regression. In the following paragraph, we will discuss the building of regression model as well as the effects of different variables on the model. 
Simple Linear Regression Model:

a) Effect of Temperature (AT):

The effect of temperature is the most influential factor showing a correlation about -0.95. Fig.1 shows the scatter diagram of temperature and PE as well as their linear regression model to fit data. The resulting predictive model PE=497.097232-2.17*T with adjusted R-squared 0.8989.

b) Effect of Pressure (AP):

Effect of Ambient Pressure Among the ambient variables, the second most influential one is AP. However, it doesn’t have a strong correlation with the target variable sufficient for an individual prediction, as it can be observed from the scatter diagram shown in Fig. 3. The slope of the linear regression function tells us that unit increase in AP corresponds to 1.4 MW increase in PE. The resulting predictive model PE=-1.064e+03+1.499e+00*AP with adjusted R-squared 0.2706.

c) Effect of Humidity (RH):

Higher relative humidity increases which leads to an in increase in the power generated by the steam turbine. The resulting predictive model PE= 420.53092+ 0.46224*RH with adjusted R-squared 0.1535.

d) Effect of Vacuum (V):

The resulting predictive model PE= 517.91831- 1.16976*V with adjusted R-squared 0.7573.

Multiple Linear Regression Model: 

In the following paragraphs, we will discuss the effects of combining multiple variable. First, we will combine two variables. Later, we will investigate the model by including all parameters. Model 1: Temperature + Vacuum The adjusted R-squared value has increased to 0.9164 in compare to simple linear regression. Model 2: Temperature + Pressure The adjusted R-squared value is 0.9012. Model 3: Temperature + Humidity The adjusted R-squared value has increased to 0.9209. Model 4: Vacuum+ Pressure The adjusted R-squared value has decreased to 0.7738. Model 5: Vacuum+ Humidity

The adjusted R-squared value has increased to 0.7871.

Model 6: Pressure+ Humidity The adjusted R-squared value is 0.3843.

Model 8: All variables The adjusted R-squared value has increased to 0.9287 in compare to all models. The resulting predictive model PE= -1.97AT-0.23V+0.62AP-0.16RH+454.61

Conclusion:

The aim of this study was to investigate efficient machine learning methods for predicting electrical power to be generated. By investigating our dataset, we have found the most influential variable, T (temperature) that affects the generated electrical power. But the most accurate predictive model is achievable only by combining all the variables.