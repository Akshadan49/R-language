# R-language
1.Try to write a code for printing sequence of numbers from 1 to 50 with the differences of 3, 5, 10 
> seq(1,50, by=3)
 [1]  1  4  7 10 13 16 19 22 25 28 31 34 37 40 43 46 49
> seq(1,50, by=5)
 [1]  1  6 11 16 21 26 31 36 41 46
> seq(1,50, by=10)
[1]  1 11 21 31 41

2.What are the different data objects in R? and write syntax and example for each and every object 
Ans:R consists of a number of data objects to perform various functions. There are 6 types of objects in R Programming. They include vector, list, matrix, array, factor, and data frame.
Vectors are one of the basic R programming data objects. They are six types of atomic vectors- logical, integer, character, raw, double, and complex.
# Create two vectors.
v1 <- c(3,8,4,5,0,11)
v2 <- c(4,11,0,8,1,2)

# Vector addition.
add.result <- v1+v2
print(add.result)

# Vector subtraction.
sub.result <- v1-v2
print(sub.result)

# Vector multiplication.
multi.result <- v1*v2
print(multi.result)

# Vector division.
divi.result <- v1/v2
print(divi.result)
[1]  7 19  4 13  1 13
[1] -1 -3  4 -3 -1  9
[1] 12 88  0 40  0 22
[1] 0.7500000 0.7272727       Inf 0.6250000 0.0000000 5.5000000

Lists are data objects of R that contain various types of elements including strings, numbers, vectors, and a nested list inside it. It can also consist of matrices or functions as elements. It can be created with the help of the list() function.
# Create two lists.
list1 <- list(1,2,3)
list2 <- list("Sun","Mon","Tue")

# Merge the two lists.
merged.list <- c(list1,list2)

# Print the merged list.
print(merged.list)
[[1]]
[1] 1

[[2]]
[1] 2

[[3]]
[1] 3

[[4]]
[1] "Sun"

[[5]]
[1] "Mon"

[[6]]
[1] "Tue"
Matrices in R Programming are used to arrange elements in the two-dimensional layout. They contain elements of the same data type. They usually contain numeric values in order to perform mathematical operations.
# Create two 2x3 matrices.
matrix1 <- matrix(c(3, 9, -1, 4, 2, 6), nrow = 2)
print(matrix1)

matrix2 <- matrix(c(5, 2, 0, 9, 3, 4), nrow = 2)
print(matrix2)

# Add the matrices.
result <- matrix1 + matrix2
cat("Result of addition","\n")
print(result)

# Subtract the matrices
result <- matrix1 - matrix2
cat("Result of subtraction","\n")
print(result)
   [,1] [,2] [,3]
[1,]    3   -1    2
[2,]    9    4    6
     [,1] [,2] [,3]
[1,]    5    0    3
[2,]    2    9    4
Result of addition 
     [,1] [,2] [,3]
[1,]    8   -1    5
[2,]   11   13   10
Result of subtraction 
     [,1] [,2] [,3]
[1,]   -2   -1   -1
[2,]    7   -5    2
An array is used to store data in more than just 2 dimensions. It is used to store multi-dimensional data in the required format. It can be created with the help of an array() function.
# Create two vectors of different lengths.
vector1 <- c(5,9,3)
vector2 <- c(10,11,12,13,14,15)

# Take these vectors as input to the array.
array1 <- array(c(vector1,vector2),dim = c(3,3,2))

# Create two vectors of different lengths.
vector3 <- c(9,1,0)
vector4 <- c(6,0,11,3,14,1,2,6,9)
array2 <- array(c(vector1,vector2),dim = c(3,3,2))

# create matrices from these arrays.
matrix1 <- array1[,,2]
matrix2 <- array2[,,2]

# Add the matrices.
result <- matrix1+matrix2
print(result)
   [,1] [,2] [,3]
[1,]   10   20   26
[2,]   18   22   28
[3,]    6   24   30


Factorsare data objects that are used in order to categorize and store data as levels. They can be strings or integers. They are extremely useful in data analytics for statistical modeling. They can be created using factor() function.
# Create the vectors for data frame.
height <- c(132,151,162,139,166,147,122)
weight <- c(48,49,66,53,67,52,40)
gender <- c("male","male","female","female","male","female","male")

# Create the data frame.
input_data <- data.frame(height,weight,gender)
print(input_data)

# Test if the gender column is a factor.
print(is.factor(input_data$gender))

# Print the gender column so see the levels.
print(input_data$gender)
  height weight gender
1    132     48   male
2    151     49   male
3    162     66 female
4    139     53 female
5    166     67   male
6    147     52 female
7    122     40   male
[1] TRUE
[1] male   male   female female male   female male  
Levels: female male

Dataframeis a 2-dimensional data structure wherein each column consists of the value of one variable and each row consists of a value set from each column.
# Create the data frame.
emp.data <- data.frame(
   emp_id = c (1:5), 
   emp_name = c("Rick","Dan","Michelle","Ryan","Gary"),
   salary = c(623.3,515.2,611.0,729.0,843.25), 
   
   start_date = as.Date(c("2012-01-01", "2013-09-23", "2014-11-15", "2014-05-11",
      "2015-03-27")),
   stringsAsFactors = FALSE
)
# Print the data frame.                 
print(emp.data) 
emp_id    emp_name     salary     start_date
1     1     Rick        623.30     2012-01-01
2     2     Dan         515.20     2013-09-23
3     3     Michelle    611.00     2014-11-15
4     4     Ryan        729.00     2014-05-11
5     5     Gary        843.25     2015-03-27

3.Create Data frame with 3 columns and 5 rows and write a code to fetch and delete row and a column using index and add new column and row to the existed data frame 
Data_Frame <- data.frame (
  Training = c("Strength", "Stamina", "Other","Power","Degree"),
  Pulse = c(100, 150, 120, 100, 150),
  Duration = c(60, 30, 45, 50, 55)
)

Data_Frame

summary(Data_Frame)


> Data_Frame
  Training Pulse Duration
1 Strength   100       60
2  Stamina   150       30
3    Other   120       45
4    Power   100       50
5   Degree   150       55
> 
> summary(Data_Frame)
   Training             Pulse        Duration 
 Length:5           Min.   :100   Min.   :30  
 Class :character   1st Qu.:100   1st Qu.:45  
 Mode  :character   Median :120   Median :50  
                    Mean   :124   Mean   :48  
                    3rd Qu.:150   3rd Qu.:55  
                    Max.   :150   Max.   :60  


 Data_Frame <- data.frame (
 Training = c("Strength", "Stamina", "Other","Power","Degree"),
 Pulse = c(100, 150, 120, 100, 150),
 Duration = c(60, 30, 45, 50, 55)
)

# Remove the first row and column
Data_Frame_New <- Data_Frame[-c(1), -c(1)]

# Print the new data frame
Data_Frame_New

 Pulse Duration
2   150       30
3   120       45
4   100       50
5   150       55

Data_Frame <- data.frame (
        Training = c("Strength", "Stamina", "Other","Power","Degree"),
         Pulse = c(100, 150, 120, 100, 150),
         Duration = c(60, 30, 45, 50, 55)      )

# Add a new column
New_col_DF <- cbind(Data_Frame, Steps = c(1000, 6000, 2000, 5000, 7000))

# Print the new column
New_col_DF

Data_Frame <- data.frame (
        Training = c("Strength", "Stamina", "Other","Power","Degree"),
         Pulse = c(100, 150, 120, 100, 150),
         Duration = c(60, 30, 45, 50, 55)      
)

# Add a new row
New_row_DF <- rbind(Data_Frame, c("Strength", 110, 110))

# Print the new row
New_row_D

4.Write nested if else statements to print whether the given number is negative, positive or Zero 
x <- 0
if (x < 0) {
print("Negative number")
} else if (x > 0) {
print("Positive number")
} else
print("Zero")

5.write a program to input any value and check whether it is character, numeric or special character 
For Digit
x <-5
is.numeric(x)
For Character
x 1 ← c( “akshada”,100)#
is.character(x1)
For Special Character
m ← “/” #
grepl('[^[:alnum:]]', m)
which will check for any value that is not a letter or a number. 

6.write difference between break and next also write examples for both
Break Statement
The break keyword is a jump statement that is used to terminate the loop at a particular iteration.
Syntax 
if (test_expression) {
break
}
Eg.
# 

no <- 1:10

for (val in no)
{
	if (val == 5)
	{
		print(paste("Coming out from for loop Where i = ", val))
		break
	}
	print(paste("Values are: ", val))
}
[1] "Values are:  1"
[1] "Values are:  2"
[1] "Values are:  3"
[1] "Values are:  4"
[1] "Coming out from for loop Where i =  5"
Next Statement
The next statement is used to skip the current iteration in the loop and move to the next iteration without exiting from the loop itself.
Syntax:
if (test_condition) 
{
    next
}
[1] "Values are:  1"
[1] "Values are:  2"
[1] "Values are:  3"
[1] "Values are:  4"
[1] "Values are:  5"
[1] "Skipping for loop Where i =  6"
[1] "Values are:  7"
[1] "Values are:  8"
[1] "Values are:  9"
[1] "Values are:  10

7.write a program to print a given vector in reverse format
x= c(1,5.6,3,10,3.5,5)
print(x)
rx = rev(x)
print(rx)
[1]  5.0  3.5 10.0  3.0  5.6  1.0
8.write a program to get the mode value of the given vector (‘a’,’b’,’c’,’t’,’a’,’c’,’r’,’a’,’c’,’t’,’z’,’r’,’v’,’t’,’u’,’e’,’t’) 
> # Create the function.
> getmode <- function(v) {
+     uniqv <- unique(v)
+     uniqv[which.max(tabulate(match(v, uniqv)))]
+ }
> # Create the vector with characters.
> charv <- c("a","b","c","t","a","c","r","a","c","t","z","r","v","t","u","e","t")
> # Calculate the mode using the user function.
> result <- getmode(charv)
> print(result)
[1] "t"

9.Write a function to filter only data belongs to ‘setosa’ in species of Iris dataset.( using dplyr package)

> install.packages("dplyr")
# The datasets package needs to be loaded to access our data 
# For a full list of these datasets, type library(help = "datasets")
library(datasets)
data(iris)
summary(iris)
names(iris) <- tolower(names(iris))
library(dplyr)
## 
## Attaching package: 'dplyr'
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
# filter() the data for species virginica
setosa <- filter(iris, species == "setosa")
head(setosa) # This dispalys the first six rows
10.Create a new column for iris dataset with the name of Means_of_obs, which contains mean value of each row.( using dplyr package) 
#remove column 5
iris_subset <- iris[,-5]
 
#one less column
dim(iris_subset)
#[1] 150   4
 
#now let's perform some simple statistics
#calculate the mean of each row
#and add an extra column called mean
iris_subset$mean_of_obs <- apply(iris_subset, 1, mean)
head(iris_subset)


11.Filter data for the “versicolor” and get only ‘sepel_length’ and Sepel _width’ columns.( using dplyr package) 

rm(list = ls(all = TRUE))
# install.packages('dplyr', dependencies = TRUE) # install it if you don't have
library(dplyr, quietly = TRUE)
## 
## Attaching package: 'dplyr'
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
data(iris) # load the iris data
iris2 <- tbl_df(iris)
print(iris2)
iris2 <- tbl_df(iris)
filter(iris2, Species == 'versicolor') # Species == 'versicolor' is the criteria
select(iris2, Petal.Length, Sepal.Width)


12.create below plots for the mtcars also write your inferences for each and every plot (use ggplot package) Use Different ( Size , Colour ) 
> library(ggplot2)
> str(mtcars)
'data.frame':	32 obs. of  11 variables:
 $ mpg : num  21 21 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 ...
 $ cyl : num  6 6 4 6 8 6 8 4 4 6 ...
 $ disp: num  160 160 108 258 360 ...
 $ hp  : num  110 110 93 110 175 105 245 62 95 123 ...
 $ drat: num  3.9 3.9 3.85 3.08 3.15 2.76 3.21 3.69 3.92 3.92 ...
 $ wt  : num  2.62 2.88 2.32 3.21 3.44 ...
 $ qsec: num  16.5 17 18.6 19.4 17 ...
 $ vs  : num  0 0 1 1 0 1 0 1 1 1 ...
 $ am  : num  1 1 1 0 0 0 0 0 0 0 ...
 $ gear: num  4 4 4 3 3 3 3 4 4 4 ...
 $ carb: num  4 4 1 1 2 1 4 2 2 4 ...
> 
> library(ggplot2)
> ggplot(mtcars, aes(x = cyl, y = mpg)) 
+     geom_point()
> library(ggplot2)
> ggplot(mtcars, aes(x = wt, y = mpg, color = disp)) 
geom_point()
