---
title: "Introduction to Data Science - HW 2"
author: "Jaleel Rogers- `jrogers1239@floridapoly.edu`"
---



# Problem 1 (30 points)

During class you completed an activity in which you practiced `git` commands and operations (such as forking a repository, cloning it using `git clone`, and uploading changes using `git push`).

In this exercise you are asked to modify the `flpoly_student.md` file you worked during class, and format it using the **markdown** tools discussed in class. You must **create a table** that shows the courses you are currently enrolled in, using for the headers of the table: 

- Prefix: in bold letters (such as **COP**)
- Number: in bold letters (such as **2073**)
- Name: in italics (such as _Introduction to Data Science_)
- Credits (such as 3)



a. Make sure your GitHub repo (`practice-repo/`) shows the results of your updated file (remember to use the commands `git add .` , `git commit -m "YOUR MESSAGE"`, and `git push`) 

b. Include a link to your GitHub repo in this document.

c. Take a screenshot of the GitHub repo, add the screenshot file to the repo, and include it in this document (review how to insert a picture using markdown)


```{r}

knitr::opts_chunk$set(echo = TRUE) #Found a way to start making a table

Prefix=c ("<B>COP</B> " , "<B>MAC</B>") #Categorize each requirement into a column | <B> </B> is for bold and <I> </I> is for italics

Number=c("<B>2073</B>","<B>2311</B>")

Name=c("<I>Introduction to Data Science</I>", "<I>Analtyic Geometry and Calculus 1</I>")

Credits=c("3", "4")

 classes=data.frame(Prefix, Number, Name, Credits)
 classes #Print data set
 
knitr::kable(classes, "pipe", col.name=c("Prefix", "Number", "Name", "Credits"), align = c ("c", "c", "c", "c")) #knit organizes information into table and aligns it


```
GitHub repo link: https://github.com/CaptainBlast096/practice-repo.git

![Screenshot of repository is above](https://imgur.com/4WMrNyg.png)

# Problem 2 (30 points)



For this problem, you are asked to create a list of **3 concepts** you have learned about so far this semester. Include the name of the course as a sub-heading (that is, using `##`), and the concepts as an unordered list. Include a link to information about at least one of the concept you listed (for example a link to the Wikipedia page about that concept/topics).


_Edit this `.Rmd` file to include the solutions here._

  
## Introduction to Data Science
 
  * Markup Language (https://careerkarma.com/blog/markup-language/)
  * Cloning, Pushing, and Pulling from GitHub
  * Variables
  
## Analytic Geometry and Calculus 1
 
  * Limit
  * Squeeze Theorem (https://www.mathwarehouse.com/calculus/limits/what-is-the-squeeze-theorem.php)
  * Discontinuity 


# Problem 3 (40 points)

In this problem you will practice some basic R operations. Include solutions to each items by inserting a new R chunk of code (make sure you run the chunk so that the output is displayed)

(a) Create a variable called `my_name` that contains your preferred name.
```{r}

a = "My name is"
my_name = 'Jaleel Rogers'
result = paste( a, my_name)
result

```
(b) Create a variable called `name_length` that holds how many letters are in `my_name`.
```{r}

b = "The number of letters in my name is"
name_length = nchar(my_name) #problem creating variable named name_length
result = paste(b, name_length)
result

```
(c) Show which value is bigger: $e^\pi$ or $\pi^e$. 
```{r}

x = "e^pi > pi^e is"
result = paste (x , exp(1) ^ pi > pi ^ exp(1)) 
result

```

(d) Define a function called `add_tree` that takes a single argument and returns a value 3 times larger than the input.
```{r}
add_tree = readline(prompt =  "Enter in a number:")
add_tree=as.integer(add_tree)
Num1 = 3
Sum = (add_tree * Num1)
print (Sum)
```

(e) Use the colon operator `:` to create a vector `v` of numbers from 10 to 49. Find the length of this vector using the `length()` function.
```{r}
 
 v = 10:49 #vector
 v
 length(V) 
```

(f) Use the `seq()` function to produce a range of number from -5 to 10 in 0.5 increments.

```{r}
 seq(-5, 10, by =  0.5) #Sequence
```

