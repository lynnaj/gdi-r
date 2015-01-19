R programming
========================================================
author: Lynna Jirpongopas
date: Sun Jan 18 16:53:45 2015

What is R?
========================================================

    "R is a free software programming language and software environment for statistical computing and graphics." 
                
    -Wikipedia


- Dialect of S language
- Free software
- In 2000, R version 1.0.0 is released


Why R?
========================================================
- Other statistical tools: Stata, SPSS, and SAS


- Lots of resources
  - help
      - eg. Stack Overflow
  - packages
      - eg. ggplot, reshape, zoo, shiny
- Commercial support for R


Download and installing RStudio
======================================================== 
1. Getting RStudio: http://www.rstudio.com/products/rstudio/download/ 

2. Customizing your GUI

3. Alternative: RGui from http://www.r-project.org/


Dive into R basics
======================================================== 

Often see <- , instead of =

Comments ##

Case sensitive

; is not necessary, but optional

?mean means to get help with function mean

Strings require " "

: is used to generate sequence of numbers



Data Types
========================================================
**basic classes of objects**
- vectors: character, numeric, integer, complex, logical

**other classes of objects**
- list
- matrix
- factor
- data frame
      
**misc.**
- missing values
- names


Basic classes of objects
========================================================


```r
a <- c("a", "b", "c")       ##character
b <- c("0.25", ".3", "4.5") 
##note the quotation marks!

c <- c(0.25, .3, 4.5)       ##numeric
d <- 10:20                  ##integer
e <- c(T, F)                ##logical
f <- c(1+0i, 3+i)           ##complex
```

Try class() function!

There are other types of classes: "raw" and "expression"


Vectors
========================================================
- Most basic object is a vector
- A vector must contain objects of the same class


```r
a <- c("h", 1, 2)     
class(a)
```

```
[1] "character"
```

```r
x <- vector(mode="logical", length=10)
```

Check previous slide vectors by typing the vector names, eg. d

Create empty numeric vector


Lists
========================================================
A list can contain objects with different classes


```r
a <- list("h", 1, 2)
```

For lists, [[ ]] is used to select any single element, whereas [ ] returns a list of the selected elements.


Lists
========================================================

```r
class(a) 
```

```
[1] "list"
```

```r
class(a[[1]])
```

```
[1] "character"
```

```r
class(a[[2]])
```

```
[1] "numeric"
```


Matrices
========================================================

- an atomic vector
- contructed column-wise
- all elements must be of same class


```r
m <- matrix(nrow=2, ncol=3)
m
```

```
     [,1] [,2] [,3]
[1,]   NA   NA   NA
[2,]   NA   NA   NA
```

```r
m <- matrix(1:6, nrow=2, ncol=3)
l <- cbind(a = 1:3, pi = pi)
```

Matrices
========================================================

Try class(), attributes(), dim() functions on these matrices


```r
class(m)
```

```
[1] "matrix"
```

```r
class(l)
```

```
[1] "matrix"
```

Factors
========================================================
Categorical data
The different categories are called, levels


```r
f <- factor(c("small", "large", "large", "medium", "small"),
            levels=c("small", "medium", "large"))
f
```

```
[1] small  large  large  medium small 
Levels: small medium large
```

Dataframes
========================================================
Like matrices but can contain different classes.


```r
df <- data.frame(colOne = 1:4, colTwo = c("small", "large", "small", "medium"))
df
```

```
  colOne colTwo
1      1  small
2      2  large
3      3  small
4      4 medium
```

Dataframes
========================================================
nrow() and ncol() can be used to find out the number of rows and columns of the dataframe


```r
nrow(df); ncol(df)
```

```
[1] 4
```

```
[1] 2
```

```r
dim(df) #alternatively
```

```
[1] 4 2
```

Names
========================================================
names() function output the variable names 

(aka. column names)

```r
names(df)
```

```
[1] "colOne" "colTwo"
```


Missing Values
========================================================
Use is.na() function to look for missing values NA and NaN.
It won't find completly empty elements like a space.
You can also use is.nan(), but it only works for missing values that are labeled as NaN

```r
k <- c(8, 6, 4, NA)
is.na(k)
```

```
[1] FALSE FALSE FALSE  TRUE
```

```r
is.nan(k)
```

```
[1] FALSE FALSE FALSE FALSE
```


