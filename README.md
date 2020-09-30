# Duke Textbook Estimation

## Introduction

In this project, we designed and implemented a survey to explore the expected expenditures on required textbooks for natural science students at Duke, if they buy them new at the [Duke textbook store](https://eposweb-320.sequoiars.com/ePOS?form=shared3/gm/main.html&this_category=17&store=320&design=duke_textbooks). The main goal of this survey is to estimate the following variables:

- the total cost of required books in the natural sciences at Duke  
- the average number of required books per course in the natural sciences at Duke  
-  the average of the (total) cost of required books per course in the natural sciences at Duke

## Study Design

Since our population can be naturally divided into 9 departments, we decided to use a stratified sampling method with 9 strata: department *Biology*, *Chemistry*, *Computer Science*, *Evolutionary Anthropology*, *Mathematics*, *Physics*, *Psychology*, *Neuroscience* and *Statistical Science*.   

## Data Collection

All of the data was collected at the [Duke textbook store](https://eposweb-320.sequoiars.com/ePOS?form=shared3/gm/main.html&this_category=17&store=320&design=duke_textbooks). We decided to sample 60 courses from the frame and used a stratified sampling with proportional allocation, which led to the following result:

                             |$N_h$ |$n_h$
-----------------------------|------|---------
*Biology*                    |47    |10
*Chemistry*                  |20    |4
*Computer Science*           |29    |6
*Evolutionary Anthropology*  |15    |3
*Mathematics*                |52    |11
*Physics*                    |27    |5
*Psychology*                 |55    |11
*Neuroscience*               |26    |5
*Statistical Science*        |24    |5
Total                        |295   |60

Having settled the course indices we decided to sample, we stored them, together with weights and Finite Population Correction Factor, in [`textbook.csv`](.Data/textbook.csv) file and went to the bookstore website to obtain relevant information (number of books and costs). With the collected information about book quantities and prices, we updated the dataset into [`textbook_new.csv`](.Data/textbook_new.csv).

## Result

The results were obtained based on the stratified sampling design in R package `survey`.

- the total cost of required books in the natural sciences at Duke (in dollars)

                 |total cost  |standard error 
-----------------|------------|---------------
cost of textbook |13145.93    |2623.78        

- the average number of required books per course in the natural sciences at Duke

                   |average no. of books  |standard error 
-------------------|----------------------|---------------
number of textbook |0.34                  |0.06

-  the average of the (total) cost of required books per course in the natural sciences at Duke (in dollars)

                 |average cost of books |standard error 
-----------------|----------------------|---------------
cost of textbook |44.56                 |8.89        

## Authors

- Mingxuan Yang  
- Jiawei Chen