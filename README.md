# BST 260 Project: Team Po-Data Science

## Guide for Readers
### You will need to download separately from GitHub:
- **[https://stacks.stanford.edu/file/druid:db586ns4974/district%20by%20year%20by%20grade%20covariates%20from%20acs%20and%20ccd%20master_v1_1.dta](https://stacks.stanford.edu/file/druid:db586ns4974/district%20by%20year%20by%20grade%20covariates%20from%20acs%20and%20ccd%20master_v1_1.dta)** - input data from Stanford Education Data Archive (SEDA)  

---

#### Overview and Motivation
This work is inspired the work of the Stanford Education Data Archive (SEDA) is an initiative aimed at harnessing data to help us—scholars, policymakers, educators, parents—learn how to improve educational opportunity for all children.  
We were motivated to use this first national database of academic performance to ask questions about predictors of academic achievement and school funding between states and at the national level.

SEDA includes a range of detailed data on educational conditions, contexts, and outcomes in schools and school districts across the United States. It includes data at a range of institutional and geographic levels of aggregation, including schools, districts, counties, metropolitan areas, and states. In this project, our aims were to examine academic achievement, achievement gaps, school and neighborhood racial and socioeconomic composition, school and neighborhood racial and socioeconomic segregation patterns, and other features of the schooling system for students grades 3-8. 

#### Related Work
Our group was inspired to pursue this project after many of us took a statistics course at Harvard Graduate School of Education during the Spring of 2021. For this class we often applied the methods we were learning to data from The Education Opportunity Project at Stanford University. This dataset, referred to as the Stanford Education Data Archive (SEDA) provides detailed information on educational outcomes by various levels (school, district, county, community, and state).

To expand upon the Data Archive, we wanted to examine the real-world implications of the redrawing of Congressional boundary lines based on the 2020 Census. Gerrymandering is a threat to democracy and has serious real-world consequences. When districts are drawn unfairly, the public is prevented from electing representatives that accurately reflect the views of the population. Most often marginalized groups are redistributed to minimize their voices and votes. 


#### Data
Sources: 
- The American Ideology Project (2015 update), available from: https://americanideologyproject.com/
- Stanford Education Data Archive, (codebook_covariates_v1_1.xlsx, ), available from: https://exhibits.stanford.edu/data/catalog/db586ns4974
- 113th Congressional District coordinates, available from: https://github.com/ropensci/USAboundaries

#### Objectives
Specifically we are aiming to answer the following questions:  
- What are some of the most important predictors of academic achievement at the national level?
- How is unemployment, poverty, and socioeconomic status associated with academic achievement in Massachusetts, Washington, Nebraska, and California?
- How is percent free or reduced lunch associated with academic achievement in districts at the national level?
- How is constituent ideology (right-leaning or conservative vs. left-leaning or liberal) associated with congressional district expenditure per pupil and per instructor?


#### Our Approach
We approached these questions using a variety of methods. To determine the most important predictors of academic achievement, we first used exploratory visualization of the correlations between various predictors and academic achievement. We then used a Random Forest model to determine the relative importance of these predictors as demonstrated by their Gini coefficient.   

To explore the relationship between unemployment, poverty, and socioeconomic status and academic achievement we create plots of association to see how these variables are correlated. Moreover, to estimate the effect of percent free or reduced lunch on academic achievement in districts we use a regression model, controlling for socioeconomic status and geography (urban vs. rural).  

To look at how spending on education varies by political leaning within each congressional district, we create an interactive map that shows pupil expenditure in a district by political leaning. Lastly, we create a Shiny app to select predictors and visualize how they map to academic achievement.


#### Analysis
Analyses can be found in two parts:  

- Part I: Predictors of Academic Acheivement 
- Part II: Political Ideology & Educational Spending



