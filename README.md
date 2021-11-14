## Tidyverse Solo Exercise

In this project, you'll practice working with data using the tidyverse libraries. 
You'll be working with data on each of 145 school districts and the State of Tennessee. This data contains, for the 2014-2015 school year:
* Proficiency rates on state tests
* Student demographics
* Chronic absenteeism
* Discipline (suspension, expulsion) rates
* High school graduation, dropout rates
* Average ACT composite scores
* A region in Tennessee  

Create an RMarkdown file to answer the following questions.

1. Read in `districts.csv` into a tibble named `districts`. How many rows and columns does it contain?

2. Notice that the first row corresponds to the whole State of Tennessee. Remove this row and save the result back to `districts`.

3. How many districts have a proficiency rate of at least 80% for both alg_1 and eng_1?

4. How many districts have a proviciency rate less than 50% for either alg_1 or eng_1?

5. Which district has the lowest graduation rate?

6. Which district has the highest dropout rate?

7. Within the Mid Cumberland region, which district has the highest ACT composite?

8. Create a histogram showing the distribution of graduation rates. What can you say about this distribution?

9. Create a scatter plot to compare alg_1 proficiency rates to alg_2 rates. What do you notice? Facet this plot by region. Does anything stand out when you facet the plots?

10. Create a bar chart showing the total enrollment by region. Which region has the highest total enrollment? Which has the smallest?

11. When creating this bar chart you may have noticed that some districts have missing enrollment values. For how many districts is this the case?

12. What is the mean graduation rate across all districts? What might be wrong with using just the regular mean to assess average graduation rates?

13. Redo the previous question but use a weighted average (`weighted.mean`) graduation across all districts, weighing by enrollment. How much does this change your answer? Can you explain using the data the reason for the big change from using the mean?

14. Create a boxplot showing enrollment rates per region. Does anything stand out?

15. Create a boxplot showing graduation rates per region. Does anything stand out?

16. Find the weighted average of graduation rates by region using enrollment as weights. Compare the results you get for the weighted average to what you see from the boxplots. Can you explain any discrepancy?

17. For many districts, values for `alg_2` are lower than for `alg_1`. Create a histogram showing the distribution of differences (`alg_1` - `alg_2`). Which school had the largest drop from `alg_1` to `alg_2`? For what percentage of schools is it true that `alg_2` is larger than `alg_1`? Is there a similar dropoff for `eng_2` and `eng_3`?

18. You may have noticed that a lot of rows are missing values. Which district has the largest number of missing values? What do you notice about schools that have a lot of missing values?

19. Find the correlation between graduation rate and all other variables. Create a horizontal bar chart showing these correlations. Make sure that your plot is ordered by correlation values. What do you notice from these correlations?

20. Create a scatterplot for `grad` vs. `suspended`. Does what you see make sense given your answer from the previous part?

21. Create a linear regression model using `lm` with target variable `grad` and predictor variable `suspended`. What R^2 value does this model have? What is the interpretation of this number?

22. Add the regression line to your scatterplot using `geom_smooth` with `method='lm'`. How do you feel about the regression line after seeing it plotted on the scatterplot?

**Continued Exploration and Practice**

23. Read in the school-level testing data for 2014, available [here](https://www.tn.gov/content/dam/tn/education/data/data_2014_school_base.xlsx). You might find the readxl library useful for this task. If you use this library, be sure to look at the `na` argument for the `read_excel` function.

24. How many schools have at least 20 percent of students below bsc for Algebra I? Which districts do these schools belong to?

25. How many schools have at least 20 percent of students below bsc for _both_ Algebra I and English I?

26. Which grade has the highest pct_adv for Algebra I? Plot the average pct_adv per grade level as a bar chart. Make sure that the bars are ordered by grade level.

27. Find the correlation between pct_adv for Algebra I and pct_adv for Algebra II by school. Create a scatterplot showing Algebra II scores vs. Algebra I scores by school.

28. Find all schools in Rutherford County that have "High School" in their name. For these schools, create a chart (your choice) showing the differences in pct_below_bsc, pct_bsc, pct_prof, and pct_adv for Algebra I when looking across all subgroups and grades.

29. I claim that smaller schools do a better job preparing students for Algebra I standardized tests. Find the average number of valid tests (a proxy for the school size) for schools where the pct_prof_adv for Algebra I is greater than 95. Compare this to the average number of valid tests for all schools. In light of this result, how does my claim look?

30. I also claim that smaller schools do a worse job preparing students for Algebra I standardized tests. Find the average number of valid tests (a proxy for the school size) for schools where the pct_prof_adv for Algebra I is less than 25. Compare this to the average number of valid tests for all schools. In light of this result, how does my claim look now?

31. Create a scatterplot showing pct_prov_adv vs. valid_tests. Can you use this to explain the result for numbers 26 and 27?

If you finish all of the above questions, continue to explore the two datasets and see what else interesting you can find.

Also, check out the plotly library for R. The `ggplotly` function makes it very easy to convert ggplot plots into interactive plotly plots.