# Neural_Network_Charity_Analysis


*1. What variable(s) are considered the target(s) for your model?*

Our target is column **IS_SUCCESSFUL**

____________________________
*2. What variable(s) are considered to be the features for your model?*

**Initial model** - all columns except **EIN** and **NAME**

| APPLICATION_TYPE | AFFILIATION | CLASSIFICATION | USE_CASE | ORGANIZATION | STATUS | INCOME_AMT | SPECIAL_CONSIDERATIONS | ASK_AMT |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

**Optimized Model** - varies (see image on the bottom), but the one with the highest accuracy includes colum all columns and excluded only **EIN**

| **NAME** | APPLICATION_TYPE | AFFILIATION | CLASSIFICATION | USE_CASE | ORGANIZATION | STATUS | INCOME_AMT | SPECIAL_CONSIDERATIONS | ASK_AMT |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

__________________


*3. What variable(s) are neither targets nor features, and should be removed from the input data?*

* Initial model - **EIN** and **NAME**
* Optimized model - **EIN** only (after testing multiple scenarios (see image below)

_____________________
#### Compiling, Training, and Evaluating the Model

*4. How many neurons, layers, and activation functions did you select for your neural network model, and why?*

It varied. The best and most accuarte was with three layers and 100-40-10 neurons

*5. Were you able to achieve the target model performance?*

Yes (see table below that shows attempts and results). All twenty files are saved in folder Optimization

*6. What steps did you take to try and increase model performance?*


![](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/blob/main/Images/best_result.PNG)
