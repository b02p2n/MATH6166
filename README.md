java c
MATH6166 Statistical Computing for Data Scientists/MATH6173 Statistical Computing — Coursework
Instructions for Coursework
1.  This coursework assignment is worth 100% of the overall mark for the module MATH6166, and 50% of the overall mark for the module MATH6173.
2.  The deadline is 15:00 on Friday 17th November 2023, and your completed work must be submitted electronically via Blackboard.
3.  All  of your  answers  to  the  coursework  are  to  be  written  in  the  R  Markdown  file  “Coursework- template.Rmd”, which can be found under the Coursework heading in the Assessment panel on Black- board. Download this file and write all of your answers to the coursework questions in this file only.
4.  The file “Coursework-template.Rmd” is a template answer sheet that is used to write your answers to all of the coursework questions. This is the only file that you need to use to write down your answers. You must not delete any of the content from this file; for example, do not change the names or options of code chunks, or change the layout of the file.  The layout of the file has been designed specifically so that the correctness of the R functions that you write can be systematically assessed.
5. You must write all of your coding answers to each question in the corresponding empty R Markdown code chunk within the file.  Do not create any new code chunks.  Each code chunk has a name that matches the corresponding coursework question, and there are comments that signpost where to provide an answer for a specific question.  For example, for  Question 1 (a), you will see the comment Write your  code  for  Q1  (a)  in  the  code  chunk  below:  and below this comment will be a code chunk with the label Q1a. Any changes you make outside of the designated code chunks will likely result in your assessment not being able to be marked. All the coding answers must be carried out through R commands (do not use comments to give your answers).
6. Where relevant,  report  your  answers in the designated section below the R code chunks for each question in the R Markdown file.  For example, for Question 1 (a), you will see the comment Report your  answer  for  Q1  (a)  below:, below which you can write your answer in standard R Markdown formatting.
7. When writing an R function, the
•  function name,
•  argument names and data type, and
• output names and data typemust be exactly the same as those specified in the questions; otherwise a heavy penalty will be applied. Please note that uppercase and lowercase of the same alphabet are not the same character, so if the question asks to write a function/argument called, apple, but a function/argument called applE is presented in your answer, then that would be wrong.
8. Your submission must consist of exactly two files; the R Markdown file and its associated html file that is created by knitting/rendering the R Markdown file. The R Markdown file is the “Coursework- template.Rmd” file with your answers added in the appropriate places.   Using  this  file, you must generate a html output file using the knit functionality in R Markdown, and submit this along with the R Markdown file.
9. Your R Markdown file must be renamed, and have the file name .Rmd. For example, if your student ID is 12345678, then your script. must have the file name 12345678.Rmd.
10.  Similarly, the associated html file should be named .html.  For example, if your student ID is 12345678, then your html file must have the file name 12345678.html.  (This should be correctly named by default provided that you have named the R Markdown file correctly.)
11.  Missing R codes will be penalised.   Please  ensure  the submitted files have the correct file format; otherwise it cannot be marked. Note an R Markdown file is a different format to an R script. file.
12. Your entire R Markdown file must be reproducible and run without any errors.
13. You must informatively comment your R code where appropriate.
14.  Unless specifically stated otherwise, you do not have to include error handling in your code.
15.  Ensure  that  all  required  plots  are  informative,   including  the  use  of  appropriate  plotting  areas, points/lines sizes and colours, as well as including meaningful labels, titles and legends.
16. You must not load any add-on packages, i.e., using functions library or require etc.
17.  All data files required to complete the Coursework can be downloaded from Blackboard, under the Coursework panel.
18.  To help you with the completion of the Coursework, there is an example Coursework question and related files on Blackboard for reference. You can find the following files under the Coursework Example Question panel:
•  An example Coursework question, in the file Coursework-example.pdf,
•  A template R Markdown file Coursework-example-template .Rmd in which to write your answers to the example Coursework question,
•  A model solution R Markdown file Coursework-example-solutions.Rmd, which contains solu- tions to the Coursework example question and shows you the way you are expected to fill in the Coursework-example-template .Rmd file with your answers.
•  The model solution output html file Coursework-example-solutions.html, which is simply the rendered output of the Coursework-example-solutions .Rmd file.
•  all-ad-sales .txt and youtube-ad-sales .txt: the data files needed for the example question.
19. When asked to import a data file into your R workspace, you should first set the working directory to the location of the file on your local computer using the command setwd, and then read the file in using the appropriate R command  (e.g. read .csv or read.table).  You should set the working directory every time you have to import a data file. For an example of how to do this, see Question 1 (a) in the example Coursework solutions file.
20.  The standard Faculty rules on late submissions apply:  for every weekday, or part of a weekday, that the coursework is late, the mark will be reduced by a factor of 10%. No credit will be given for work which is more than one week late.
21.  All coursework must be carried out independently.  You are reminded of the University’s Academic Integrity Policy, see https://www.southampton.ac.uk/quality/assessment/academic_integrity.page.
22. In the interests of fairness,  queries which relate directly to the coursework must be made via the Coursework Discussion Forum on Blackboard.  This ensures that everybody has access to the same information.
Total marks available:  100
Question 1:  Exploratory Analysis of Tooth Growth Data Set
[22 marks]The data set in the file tooth-growth .txt contains data on an experiment from researchers at McGill University investigating the effect of vitamin C intake on tooth growth in guinea pigs.  For each of the 60 guinea pigs in the experiment, there are recordings of three variables:
1.  len: a numeric variable, giving the tooth length of the guinea pig.
2. method:  a character variable, giving the delivery method used to give the guinea pig the vitamin C, which is either "AA" (ascorbic acid), or "OJ" (orange juice).
3.  dose: a numeric variable, specifying the dose (in milligrams per day) of vitamin C that the guinea pig received.(a)  [3 marks] Import the data set from the tooth-growth .txt file into the R workspace in a variable named tooth_data.  Change the column name len to be tooth_len (this variable will henceforth be referred to as tooth_len).  Change the data type of the method column from character to factor.  How many of the observations have delivery method by orange juice?  Store this in a variable called num_OJ.
(b)  [2 marks] What is the variance of the tooth_len column for values where the delivery method is orange juice?  Store this in a variable called var_OJ. What is the mean of the tooth_len column, where the delivery method is made by ascorbic acid  and  the dose value is 2?   Store  this in a variable called mean_AA_2.
(c)  [3 marks] The variable dose takes one of three possible values:  0.5, 1, or 2.  Create a side-by-side box plot of tooth_len for the three values of dose.
(d)  [3  marks]  Cross-tabulate  the frequencies of the method and dose variables,  creating a  2 × 3 table containing the frequencies of each of the 6 combinations of method and dose in tooth_data, and store this in a variable called dose_method_counts.  Create a barplot showing the frequencies of the observations across the method and dose variables.  There should be three bars, corresponding to each dose value, and each bar should be divided into two based on the method variable.
(e)  [3 marks] Write a function, called subset_summary, that calculates the median and length of a given subset of a numeric vector x. The median and length should be calculated only for values of x whose cor- responding factor variable, x_factor, is a user-specified value chosen_factor. The subset_summary
function should have the following features: Arguments:
1. x: a numeric vector of length n.
2. x_factor: a factor vector of length n, specifying the associated factor variable of each element of x.
3.  chosen_factor: a character variable, specifying the name of the factor to use to subset the vector x.
Computation:
The subset_summary function should compute the median and length of the subset of x, where the values of x considered have corresponding x_factor value equal to chosen_factor.
Return:
subset_summary: a list object with two elements:
1.  subset_median: the median of the subset of x.
2.  subset_length: the length of the subset of x.
(f)  [2 marks] Using the subset_summary function you wrote in part (e), calculate the median and number of observations for the tooth_len variable where the delivery method was ascorbic acid.
(g)  [6 marks] In this question, you will write a function, called subset_summary2, that improves upon the function subset_summary that you wrote in part (e), by including checks to ensure that the arguments passed to the function satisfy certain requirements. First, copy and paste the code you wrote for part
(e) into your answer for part (g), and rename the function name to subset_summary2 in part (g).
The function subset_summary2 should check that the arguments satisfy the following five requirements:
1.  x should contain numeric values,
2. x_factor should be a factor object,
3. x_factor should be the same length as x,
4.  chosen_factor should be a character variable, and
5.  chosen_factor should be one of the possible values (levels) in the x_factors variable.
If invalid inputs are passed to this function, it should stop prematurely by using the appropriate R function and print out the associated relevant error message exactly as written below:
1. x  should  only  contain  numeric  values .
2. x_factor  should  be  a  factor  object .
3. x  and  x_factor  should  be  the  same  length .
4.  chosen_factor  should  be  a  character  object .
5.  chosen_factor  should  be  one  of  the  values  of  the  x_factor  variable .
For example, if requirement 2 is not satisifed, then the function should stop and print the error message 2.


Question 2:  The Multivariate t-Distribution
[16 marks]
If X  is a p-dimensional random vector distributed according to the multivariate t-distribution, then the probability density function (pdf) of X evaluated at x, denoted fX (x), is given by

where Γ(·) is the gamma function,  det is the matrix determinant,  Σ  is  a p × p  scaling matrix,  μ  is a p-dimensional vector, and ν > 0 is a positive scalar known as the degrees of freedom.
(a)  [7 marks] Write a function, called calc_mvt_pdf, that calculates the pdf, or natural logarithm of the pdf, at a single value x, for user-specified values of Σ , μ, and ν .  The function calc_mvt_pdf should
have the following features: Arguments:
1. x: a numeric vector of length p, representing the p-dimensional x.
2.  Sigma: a numeric p × p ma代 写MATH6166 Statistical Computing for Data Scientists/MATH6173 Statistical Computing — CourseworkC/C++
代做程序编程语言trix, representing Σ in Equation (1).  The default value should be the p × p identity matrix Ip.
3. mu: a numeric vector of length p, representing μ in Equation (1).  The default value should be the p-dimensional zero vector 0 = [0, . . . , 0]T .
4.  df:  a positive numeric scalar, representing the degrees of freedom ν given in Equation (1).  The default value should be 1.
5.  calc_log: a logical variable. If set to TRUE, the natural logarithm of fX (x), given by log(fX (x)), is calculated. If set to FALSE, the pdf fX (x) is calculated.  The default value should be TRUE.
Computation:If calc_log  =  FALSE, the calc_mvt_pdf function should compute the pdf fX (x) given in Equation (1), and if calc_log  =  TRUE, the natural logarithm of Equation  (1) is computed. You must not use any existing functions in R that already calculate the multivariate t-distribution density.When computing the pdf, numerical errors can occur due to the calculation of very small or very large numbers, which is why we might calculate the log pdf instead.  If the log pdf is to be computed, you should not just apply the log function to the calculation you use to compute the pdf.  Instead, you should take advantage of properties of the log function to rewrite the logarithm of Equation (1) to produce a more numerically stable result when computing the log pdf.
Return:
1. x_pdf:  if  calc_log  =  FALSE, the pdf fX (x) is returned.   If  calc_log  =  TRUE,  the  log  pdf,
log(fX (x)), is returned. Hints:
1. You may use the R functions gamma and det.
2.  To check the numerical accuracy of your calculations, note that the expected output of the cal- culation calc_mvt_pdf(rep(3,200)) should be (approximately) the value —506.967.Suppose that  x1 , . . . , xn   are  a  set  of  n  observed  values  that  are  all  generated  independently  from  the multivariate t-distribution with parameters Σ , μ and ν .  Then, their joint probability density is given by Ⅱ fX (xi ), with fX (x) as in Equation (1), whilst the logarithm of the joint probability density is given by Σ log(fX (xi )).




(b)  [4 marks] Using a loop structure and the function calc_mvt_pdf that you wrote in part (a), write a function,  calc_joint_mvt_pdf,  that calculates the joint probability density for observed values x1 , . . . , xn that are all generated independently from the same multivariate t-distribution. The function should have the following features:
Arguments:
1. x_matrix: a numeric n × p matrix of length p, with the i-th row representing an observed value xi  .
2.  Sigma: a numeric p × p matrix, representing Σ in Equation (1).  The default value should the p × p identity matrix Ip.
3. mu: a numeric vector of length p, representing μ in Equation (1).  The default value should be the p-dimensional zero vector 0 = [0, . . . , 0]T .
4.  df:  a positive numeric scalar, representing the degrees of freedom ν given in Equation (1).  The default value should be 1.
5.  calc_log:  a logical variable.  If set to TRUE, the natural logarithm of the joint pdf is calculated. If set to FALSE, the joint pdf is calculated.  The default value should be TRUE.
Computation:
If calc_log  =  FALSE, the calc_joint_mvt_pdf function should compute the joint pdf Π fX (xi ), and  if  calc_log  =  TRUE,  the  function  should  compute  the  natural  logarithm  of  the  joint  pdf, Σ log(fX (xi )). This value should be computed using a loop structure, by looping over the n values
x1 , . . . , xn. Return:
1.  joint_pdf:  if calc_log  =  FALSE, the joint pdf Π fX (xi ) is returned.  If calc_log  =  TRUE, the logarithm of the joint pdf, Σ log(fX (xi )) is returned.
(c)  [3 marks] Using the function calc_joint_mvt_pdf you wrote in part (b), compute both the joint pdf and log joint pdf for the observed values x1  = [1.2, 3]T , x2  = [1.1, 3.1]T , x3  = [3.4, 2.6]T , coming from the multivariate t-distribution with

Store the results in variables joint_mvt_pdf and log_joint_mvt_pdf respectively.
(d)  [2 marks] Suppose that X  has a bivariate t-distribution with parameters µ = [0, 0]T , Σ is the 2 × 2 identity matrix I2 , and ν = 1.  Suppose that Y has a bivariate standard normal distribution (i.e. the bivariate normal distribution with mean vector and covariance matrix the same as X above).  Cal- culate the absolute value of the difference between these two densities, evaluated at the value  [0, 1]T , i.e. calculate
IfX ([0, 1]T ) — fY ([0, 1]T ) I ,
where fX (·) and fY (·) are the pdfs of X and Y respectively.  Store the result in a variable named density_diff.




Question 3:  Nonparametric Kernel Density Estimation
[32 marks]Density estimation is the problem of estimating the probability density function (pdf) from a set of given data points.   Concretely,  suppose we observe n  (1-dimensional) data points X1, . . . , Xn , and we wish to estimate the underlying unknown pdf, denoted f(x), of the data.
The Kernel Density Estimator (KDE) is one of the most well-known methods for solving this problem.  The

where f(ˆ)n,h (x) is the estimator of the true pdf f(x), K(·) is called the kernel function, and h > 0 is calledthe bandwidth. The kernel function is generally a smooth, symmetric function, and the bandwidth controls the amount of smoothing in the estimation.
(a)  [3 marks] The Gaussian kernel functionis  one  of  the  most  common  choices  for  the  kernel  function  K.      Write   a  function,   called width h, the KDE f(ˆ)n,h (x) given in Equation (2) with K given by the Gaussian kernel in Equation
(3). The function should have the following features: Arguments:
1.  data: a numeric vector of length n containing the data set X1, . . . , Xn  that we want to estimate the pdf of,
2. x: a numeric object, the value x for which we want to estimate the pdf f(x),
3. n: a positive integer object specifying the number of data points n,
4. h: a numeric object specifying the bandwidth h of the kernel function.
Computation:
Calculate f(ˆ)n,h (x) for a given (single) value of x using the Gaussian kernel.
Return:
• kde_est: a numeric object containing the KDE estimator f(ˆ)n,h (x).
(b)  [2 marks] Another possible kernel is the triangular kernel:for n data points X1, . . . , Xn , given value x, and bandwidth h, the KDE f(ˆ)n,h (x) given in Equation (2)with K given by the triangular kernel in Equation (4).  The function should have exactly the same
features as your answer to part (a), except that the function uses the triangular kernel.
(c)  [2 marks] The bandwidth parameter h can be set using the “rule-of-thumb” choice:



where  is the estimated standard deviation  with X = n −1 Σ Xi , IQR is the inter-quartile range,  and  n is the number of data points observed.   Write  a  function, rule_of_thumb_calc, that computes hROT  for a data set X1, . . . , Xn.  The function should have the following features: 
Arguments:
1.  data: a numeric vector of length n containing the data set X1, . . . , Xn ,
2. n: a positive integer object specifying the number of data points n.
Computation:
Calculate hROT  in Equation (5) for the data X1, . . . , Xn. Return:
• h_rot: a numeric object containing the rule-of-thumb choice for h. Hint: you may use the functions sd and IQR.
(d)  [5 marks] Write a function kde_estimate that computes the KDE of a data set X1, . . . , Xn , at m specified values x1 , . . . , xm .  Your function should call the functions you wrote in parts (a), (b), and
(c) when necessary. The function should have the following features: Arguments:
1.  data: a numeric vector of length n containing the data set X1, . . . , Xn  that we want to estimate the pdf of,
2. x_vals: a numeric vector of length m representing values x1 , . . . , xm  at which we want to estimate the pdf f (x),
3. kernel: a character object specifying the kernel function we want to use.  The kernel function can be set to be either "gaussian" or "triangular". The default argument of kernel is "gaussian".
4. h: a numeric object specifying the bandwidth of the kernel function.  The default value of h should be NULL.
Computation:
If no bandwidth parameter h is specified by the user, then the bandwidth h is calculated using the rule-of-thumb choice in Equation (5). Then, the function calculates fˆn,h(x) for all x = x1, . . . , xm, with respect to the chosen bandwidth and kernel function.
Return:
• kde_est:  a numeric vector of length m containing the KDE esimtator f(ˆ)n,h (x) evaluated at the points x = x1 , . . . , xm , i.e. a vector containing the values f(ˆ)n,h (x1 ), . . . , f(ˆ)n,h (xm ).
(e)  [6 marks] Generate 100 random variables with distribution N (3, 2), i.e. normally distributed with mean equal to 3 and variance equal to 2, and store them in a variable named norm_data.  Calculate the KDE with respect to norm_data, evaluating the KDE at 200 points x1 , . . . , x200  on an equi-spaced grid, beginning at -3, and ending at 9;
1.  using the Gaussian kernel, using the rule-of-thumb choice to set the bandwidth h;
2.  using the triangular kernel, using bandwidth h = 0.7.
Store the results in variables named gaussian_est and triangular_est respectively. On a single figure, plot the values x1, . . . , x200 against the KDE fˆn,h(x1), . . . , fˆn,h(x200) for both gaussian_est and triangular_est using a line plot. Add to this plot the true values of the pdf, f(x), evaluated at x1, . . . , x200. Make sure that each line is a different type and colour, and add a legend to distinguish the three lines.




In practice, we should carefully select the bandwidth h to minimise the mean squared error (MSE) of density estimation:



Minimising Equation (6) with respect to h can be shown to be approximately equivalent to minimising




where

i.e. fˆ−i(Xi) is the KDE in Equation (2) evaluated at Xi, computed using all data except Xi.
(f)  [7 marks] Write a function J_calc, that computes, for a given bandwidth h, the value of J(h) given in Equation (7).  The function J_calc should call the function kde_estimate written in part (d) when necessary, and have the following features: Arguments:
1. h: a numeric object specifying the bandwidth of the kernel function,
2.  data: a numeric vector of length n containing the data set X1, . . . , Xn ,
3. kernel: a character object specifying the kernel function we want to use. The default argument of kernel is "gaussian".
Computation:
The function calculates J(h) given in Equation (7).  To compute the first term in Equation  (7), you should use the integrate function.  Refer to the help file of the integrate function for details of its
usage.
Return:
•  J: a numeric value containing J(h).
(g)  [3 marks] Write a function find_opt_h, that computes, for a given set of possible bandwidth values H, the optimal choice of h by finding the bandwidth hopt  ∈ H that minimises Equation (8), i.e. computing
hopt  = arg minh∈H{J(h)}.                                 (9)
The function should call the function J_calc that you wrote in part (f), and have the following features: Arguments:
1. H_set: a numeric vector specifying the set of bandwidths H.
2.  data: a numeric vector of length n containing the data set X1, . . . , Xn ,
3. kernel: a character object specifying the kernel function we want to use. The default argument of kernel is "gaussian".
Computation:
The function calculates hopt  given in Equation (9). Return:
• h_opt: a numeric value containing hopt .
Hint: you may find the function which .min useful.
(h)  [4  marks] For the norm_data data set from part  (e),  compute the optimal bandwidth hopt  for the Gaussian kernel on the set H = {0.1, 0.11, 0.12, . . . , 1.19, 1.2}.  Plot the values of J(h) for all values in the set H in a line plot.   Add a vertical line indicating  hopt , and a vertical line indicating the rule-of-thumb choice for h, making sure the two lines can be distinguished.


         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
