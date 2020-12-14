# Neural_Network_Charity_Analysis

## Analysis Purpose:

Using knowledge of machine learning and neural networks, we had to use the features in the provided [dataset](https://raw.githubusercontent.com/jojobear2020/Neural_Network_Charity_Analysis/main/Resources/charity_data.csv) to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

-----------------

## Questions to Answer:

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

It varied. The best and most accuarte was with three layers and 100-40-10 neurons.

--------------------

*5. Were you able to achieve the target model performance?*

Yes (see table below that shows attempts and results). All attempts are also saved in folder called [Optimization](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/tree/main/Optimization).

-----------------------

*6. What steps did you take to try and increase model performance?*

* keep the column **NAME** - this seems to be the most important in increasing model accuracy
* switching layesr to `sigmoid`
* having 3 layers
* keeping epochs number at 100



![](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/blob/main/Images/best_result.PNG)
