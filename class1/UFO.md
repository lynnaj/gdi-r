UFO Sightings Analysis with R
========================================================
author: Lynna Jirpongopas
date: Wed Mar 11 21:12:32 2015



***
![UFO 1 goes here](UFO1.jpg)



What is R?
========================================================

    "R is a free software programming language and software environment for statistical computing and graphics." 
                
    -Wikipedia


- Dialect of S language
- Free software
- In 2000, R version 1.0.0 is released


Learning goals
========================================================
- Install RStudio
- Using common features of RStudio
- Load a csv table 
- Use zoo package for dates data type 
- Subset data 
- Draw insights from data!


Download and installing RStudio
======================================================== 
1. Getting RStudio: http://www.rstudio.com/products/rstudio/download/ 

2. Customizing your GUI

3. Alternative: RGui from http://www.r-project.org/




Dive into R basics (works for RGui or RStudio)
======================================================== 
<small>

  Case sensitive
  
  For comments use #
  
  ; is not necessary, but optional
  
 <-  instead of =
  
  " " are required for strings
  
  : is used to generate sequence of numbers
  
  ? before a function name to get help with a function

</small>


Dive into R basics (works for RGui or RStudio)
======================================================== 

Hotkeys:
- up and down for last or recent line of code
- Ctrl + r is for running a line of code
- Ctrl + l is for clearing the console


RStudio tools
========================================================

- install packages
- RStudio has help tab
- set working directory
- preview data
- executing R code - try 2+3
- save and open your R file
- save data


A very hotkey stroke:
- "tab" for predictive keyboard

Load a csv table
========================================================
There are several methods:

1) use RStudio GUI to set working directory

2) use setwd()

3) your csv file name in read.csv() contains the entire directory



Load a csv table, method 3
========================================================







































```
Error in file(file, "rt") : cannot open the connection
```
