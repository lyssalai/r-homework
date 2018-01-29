# r-homework-1
# This is Exercises 1. Vectors

1) Create vectors:

    (a) (1, 2, 3, . . . , 19, 20)
1:20

    (b) (20, 19, . . . , 2, 1)
20:1

    (c) (1, 2, 3, . . . , 19, 20, 19, 18, . . . , 2, 1)
c(1:20, 19:1)

    (d) (4, 6, 3) and assign it to the name tmp.
tmp <- c(4,6,3)

    (e) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3) where there are 10 occurrences of 4.
rep(tmp, 10)

    (f) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3, 4) where there are 11 occurrences of 4, 10 occurrences of 6 and 10 occurrences of 3.
c(rep(tmp,10),4)

    (g) (4, 4, . . . , 4, 6, 6, . . . , 6, 3, 3, . . . , 3) where there are 10 occurrences of 4, 20 occurrences of 6 and 30 occurrences of 3.
   rep(tmp, times=c(10,20,30))

2) Create a vector of the values of (e^x)(cos(x)) at x = 3, 3.1, 3.2, . . . , 6.

x1 <- seq(3,6,by=.1)
x2 <- exp(x)*cos(x)
head(x1,n=30)

3) Create vectors:

    (a) (0.1^3 0.2^1, 0.1^6 0.2^4, ... ,0.1^{36} 0.2{34})
a1 <- seq(3, 36,by=3)
a2 <- seq(1,34,by=3)
a3 <- 0.1^(a1)*0.2^(a2)
head(a3,n=12)

    (b) $(2, \frac{2^2}{2}, \frac{2^3}{3}, ... ,\frac{2^{25}}{25})$
b1 <- c(1:25)
(2^(b1))/(b1)

4) Calculate following:

    (a) \sum\limits_{i = 10}^{100}(i^3 + 4i^2)
c1 <- c(10:100)
(c1)^3+4*(c1)^2

    (b) \sum\limits_{i=1}^{25}(\frac{2^i}{i}+\frac{3^i}{i^2})
d1 <- c(1:25)
((2^(d1))/(d1))+((3^(d1))/(d1)^2)

5) Use the function paste to create vectors:

    (a) ("label 1", "label 2", ....., "label 30")
paste("label",1:30,sep=" ")

    (b) ("fn1", "fn2", ..., "fn30")
paste("fn",1:30,sep="")

6) Execute the following lines which create two vectors of random integers which are chosen with replacement from the integers 0, 1, . . . , 999. Both vectors have length 250.

set.seed(50)
xVec <- sample(0:999,250,replace=True)
yVec <- sample(0:999,250,replace=True)

    (a) (y_2 - x_1, . . . , y_n - x_{n-1})
e1 <- yVec[-1]-xVec[-length(xVec)]
head(e1,n=10)

    (b) (\frac{sin(y_1)}{cos(x_2)}, \frac{sin(y_2)}{x_3}, ...,\frac{y_{n-1}}{cos(x_n)})
f1 <- sin(yVec[-length(yVec)])/xVec[-1]
head(f1,n=10)

    (c) (x_1 + 2x_2 - x_3, x_2 + 2x_3 - x_4, ..., x_{x-2} + 2x_{n-1} - x_n)
g1 <- xVec[3:250]+2*(xVec[-length(xVec)]*xVec[-1])
head(g1,n=10)

    (d) \sum\limits_{i=1}^{n-1} \frac{e^{-x_{i+1}}}{x_i + 10}
h1 <- exp(-xVec[-1])/(xVec[-length(xVec)]+10)
head(h1,n=10)

7) This question uses the vectors xVec and yVec created in the previous question and the functions sort,
order, mean, sqrt, sum, and abs.

