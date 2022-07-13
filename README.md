# Machine-Learning-Accelerometer
Accelerometer
You can view the project here.
https://rpubs.com/kfitzpatrick5003/923491

Machine Learning Accelormeters for belt, arm, forearm and dumbell

The first steps in the machine learning processes of determining which exercises were performed correctly (classe =A) was to tidy the data. First, columns that were blank or contained NA in the test dataset were deleted from both datasets. Second, was to explore the variables and use a variety of methods for cross validation. If there were variables with low to zero variability they were deleted from the sets. The nearZeroVar() function was used to eliminate variables whose standard deviations were close to zero and would in turn lead to low predictability power in the model. All variables came back false, so we did not need to eliminate any of the variables.

The next method for cross validation I looked at the correlations between variables to eliminate variables with high correlations but running different models based on this method lead to lower accuracy rates of about 40%. I ended up leaving in all 51 variables.

The last method of cross validation I used was to look at the variable importance and try and only use variables with high impact to predict the five difference classes (A,B,C,D,E) this also resulted in models with lower accuracy rates.

I used qplot() to determine that the linear discriminant analysis “lda” model would be the best approach because the data seemed to be clustered in groups when I explored several plots in the exploratory phase. I only show two qplots for this report.

Preprocessing was performed to evaluate the data points and see how the means compared to the standard deviations to see if any transformations of the data was needed. This did not seem necessary in the analysis. I also ran a few models with the preprocessing features and again this did not improve accuracy rates. The final model included all 51 variables with an accuracy rate of 70% therefore the out of same error was 30%. Any recommendation for improving accuracy beyond the 70% would be appreciated. Thank you for reviewing this project.
