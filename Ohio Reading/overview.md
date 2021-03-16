## Ohio Reading Overview
#### To view the Juptyer notebooks in this project, it is best to copy and paste the notebook URL [here](https://nbviewer.jupyter.org/).

#### The goal of the project:
 - Use a difference-in-difference model to determine the impact of the Ohio Third Grade Reading Guarantee (TGRG).

#### Background
In 2009, Ohio began implementing the TGRG. This program meant to improve reading comprehension and ability of students by the time they finished third grade. In order to see if the project was successful, I decided to find another U.S. State that did not implement a similar program during the years of interest and use them as a control group for a difference-in-difference model.

#### Methodology and Hypotheses 
The panel data used for this analysis came from the Ohio and Iowa Department of Education and the U.S. Census Bureau. Observations were taken from before the implementation of the Ohio TGRG in both Ohio and Iowa as well as after the full implementation of the program.
* **Null Hypothesis:** The null hypothesis is that the Ohio Third Grade Reading Guarantee had no impact on students as measured by the Ohio Achievement Assessment (OAA) and its Iowa equivalent.
* **Alternative Hypothesis:** The alternative hypothesis is that the Ohio Third Grade Reading Guarantee did have an impact on students as measured by the OAA and its Iowa equivalent.

#### Difference-in-Difference Model
Percent_Proficient_or_Abovei = β0 + β1Ohioi + β2Afteri + β3Ohio*After_Implementationi + β4-nControlsi + εi

**Pct_Proficient_or_Abovei = β0 + β1Ohioi + β2Afteri + β3Ohio*After_Implementationi + β4-nControlsi + εi**

In the model equation, Y is the dependent variable, percent proficient or above, and β0 is the constant. β1 is the treatment group specific effect, β2 is the after implementation effect common to the control and treatment groups, and β4 represents the coefficients on each of the remaining socioeconomic control variables. Finally, the error term is represented by εi. The dummy variable for Ohio was coded as 1 if the observation is from Ohio and 0 if it was from Iowa. The After Implementation variable is also a dummy variable that is 0 if the observation was collected before the implementation of the Ohio TGRG and 1 if the observation was collected after the Ohio TGRG was fully implemented. The coefficient on the interaction term of Ohio and After Implementation is what determines if there was a statistically significant impact of the Ohio TGRG. If this coefficient is statistically significant, ceteris paribus, then one can say that the Ohio TGRG made an impact. If the coefficient is positive, then the impact was positive, improving test scores. If it is negative, then the impact was negative, lowering test scores. Control variables are were used to hold socioeconomic changes constant and isolate the impact of the program.

#### Modeling
The final model showed that there was some multicollinearity concerns with the 'Ohio','After', and interaction term that was needed for the difference-in-difference model. While they were slightly higher than I would normally allow, they did not exceed a VIF of 8. All three models that were run showed had similiar residual results. The null hypothesis of the Breusch-Pagan test for heteroskedasticity indicated that there was no heteroskedasticity present, which meant that there was constant variance in the error term. The test on the final model returned a p-value of .143 which meant that the null hypothesis cannot be rejected. Therefore, there was no heteroskedasticity detected.

#### Results
The results of the final regression model showed the interaction term of Ohio and After Implementation was positive and statistically significant. The interaction term was found to be significant at the 1% level as its p-value was 0.002. Due to this significance level, the null hypothesis that the reading program had no impact on test scores can be rejected.
