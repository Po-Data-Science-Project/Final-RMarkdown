# BST 260 Project: Team Po-Data Science

## Guide for Readers
### You will need to download separately from GitHub:
- **[https://stacks.stanford.edu/file/druid:db586ns4974/codebook_covariates_v1_1.xlsx](https://stacks.stanford.edu/file/druid:db586ns4974/codebook_covariates_v1_1.xlsx)** - input data from Stanford Education Data Archive (SEDA)  

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

- Part I: can be in the top tab
- Part II: can be found in the to tab

# **Hey group mates!!!**  

- Delete all of the below after everyone is done to replace with the actual Project ReadMe.md

### For the html knitting settings, please copy this in the upper header:
- [Image of what it looks like in the Rmd](https://raw.githubusercontent.com/Po-Data-Science-Project/SEDA-Maps/main/Screen%20Shot%202021-12-12%20at%207.40.32%20AM.png?token=AVNFGN32C3QOFCDAX2SUS3LBWXXDO)

`title: "Part X – name here"`  
`author: "Your name here"`   
`date: "12/12/2021"`    
`output:`  
  `html_document:`  
   `theme:`  
     `bootswatch: 'cosmo'`  
    `df_print: paged`  
  `pdf_document: default`  
  
### For the graphs please add this theme:  
  - `+ theme_light()`

### Naming your the Rmarkdowns and associated files (for ease of TA's grading):  
  -  Part1.1_MachineLearning.Rmd (or if all of Part1 is in one RMarkdown: Part1.Rmd)
  - Part1.2_ ... etc. 

### For updating the website: [github repo linked here](https://github.com/amesluo/amesluo.github.io)
  1. In folder \"_posts", you can directly edit your parts in github! 
  2. For readability, its helpful to **bold** important parts, or to use numbered lists
  3. To get divders between sections, the code is  `---`
  4. To get empty line breaks between sections, the code is `<br>`
  5. To insert graph pictures, the code is:  

`\<p align="center" width="100%">`  
     `\<img width="some percentage (i.e. 80%)" src="your source URL here">`  
`\</p>`  

   - You can play around with the width percentage to optimize how big you want your image to be  
   - the second line is tabbed (can see examples of such already in the Posts.md files)  

*Now, how do I get my source URL?*  
1. In folder \"_images", you can directly upload your screenshots in github!
2. After uploading in the \"images" folder, [click on the image and drag it to a new tab](https://raw.githubusercontent.com/Po-Data-Science-Project/SEDA-Maps/main/Screen%20Shot%202021-12-12%20at%207.54.42%20AM.png?token=AVNFGNY2ZAEACK75VBGP3X3BWXZCW)
3. Copy the URL of the new tab with only the image in it, [that is the **source URL**](https://raw.githubusercontent.com/Po-Data-Science-Project/SEDA-Maps/main/Screen%20Shot%202021-12-12%20at%207.56.41%20AM.png?token=AVNFGNYJTAXC35PTJRNGQVTBWXZC6)
4. Insert into the code above ^, and the webpage will now have your image in it (yay!)

