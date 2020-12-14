# Neural_Network_Charity_Analysis

## Analysis Purpose:

Using knowledge of machine learning and neural networks, we had to use the features in the provided [dataset](https://raw.githubusercontent.com/jojobear2020/Neural_Network_Charity_Analysis/main/Resources/charity_data.csv) to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

-----------------

## Questions to Answer and Results:

*1. What variable(s) are considered the target(s) for your model?*

Our target is column **IS_SUCCESSFUL**

____________________________
*2. What variable(s) are considered to be the features for your model?*

**Initial model** - all columns except **EIN** and **NAME**

| columns |
| --- |
 APPLICATION_TYPE
 AFFILIATION 
 CLASSIFICATION
 USE_CASE
 ORGANIZATION
 STATUS
 INCOME_AMT
 SPECIAL_CONSIDERATIONS
 ASK_AMT

**Optimized Model** - varies (see image on the bottom), but the one with the highest accuracy includes colum all columns and excluded only **EIN**

| columns |
| --- |
**NAME**
 APPLICATION_TYPE
 AFFILIATION 
 CLASSIFICATION
 USE_CASE
 ORGANIZATION
 STATUS
 INCOME_AMT
 SPECIAL_CONSIDERATIONS
 ASK_AMT

__________________


*3. What variable(s) are neither targets nor features, and should be removed from the input data?*

* Initial model - **EIN** and **NAME**
* Optimized model - **EIN** only (after testing multiple scenarios (see image below)

_____________________
#### Compiling, Training, and Evaluating the Model

*4. How many neurons, layers, and activation functions did you select for your neural network model, and why?*

It varied. The best and most accuarte was with three layers and 100-40-10 neurons.

(![](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/blob/main/Images/otimization_parameters.PNG)

--------------------

*5. Were you able to achieve the target model performance?*

Yes (see table below that shows attempts and results). All attempts are also saved in folder called [Optimization](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/tree/main/Optimization).

![](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/blob/main/Images/optimization_rerun_7725accuracy.PNG)

-----------------------

*6. What steps did you take to try and increase model performance?*

* Modifying what columns to keep and drop (keep the column NAME - this seems to be the most important in increasing model accuracy)
* switching layers between `relu` and`sigmoid`
* switching number of layers from 2 to 5
* swicthing epochs between 50 to 200, but mostly keeping at 100 as it seemed to be the most optimal number



![](https://github.com/jojobear2020/Neural_Network_Charity_Analysis/blob/main/Images/best_result.PNG)

---------------------------

## Summary

* While I was able to achieve accuracy at over 75%, it took multiple attempts and combinations to do so. From my experience, column **NAME** is extremely important for the model accuracy. Only after I re-evaluated the dataset and kept the column (plus used the binning method), my accuracy increased to higher levels (see table above).

* There are multiple variations how to keep the accuracy above the 75% mark, however the highest for me was to drop only column EIN, adding 3 layers with 100-40-10 nodes while using `sigmoid` for acivaton and epochs at 100.

* I would recommend to use a simpler model like Logistical Regression. Another alternative is Random Forest model, which is easier to utilize for smaller datasets and that produces high accuracy results.

* Another suggestion would be to use a larger dataset.



