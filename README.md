# r-homework-1
# This is Exercises 1. Vectors

# 1) Create vectors:

#   (a) (1, 2, 3, . . . , 19, 20)

1:20

#   (b) (20, 19, . . . , 2, 1)

20:1

#   (c) (1, 2, 3, . . . , 19, 20, 19, 18, . . . , 2, 1)

a <- c(1:20)
b <- c(19:1)
c <- c(a,b)
c

#   (d) (4, 6, 3) and assign it to the name tmp.

tmp <- c(4,6,3)

#   (e) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3) where there are 10 occurrences of 4.

rep(tmp, 10)

#***(f) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3, 4) where there are 11 occurrences of 4, 10 occurrences of 6 and 10 occurrences of 3.

#   (g) (4, 4, . . . , 4, 6, 6, . . . , 6, 3, 3, . . . , 3) where there are 10 occurrences of 4, 20 occurrences of 6 and 30 occurrences of 3.

rep(tmp, times=c(10,20,30))

# 2) Create a vector of the values of (e^x)(cos(x)) at x = 3, 3.1, 3.2, . . . , 6.

x1 <- seq(3,6,by=.1)
x2 <- exp(x)*cos(x)
head(x1,n=30)

# 3) Create vectors:

#   (a) (0.1^3 0.2^1, 0.1^6 0.2^4, ... ,0.1^{36} 0.2{34})

a1 <- seq(3, 36,by=3)
a2 <- seq(1,34,by=3)
a3 <- 0.1^(a1)*0.2^(a2)
head(a3,n=12)

#   (b) (2, \frac{2^2}{2}, \frac{2^3}{3}, ... ,\frac{2^{25}}{25})

b1 <- c(1:25)
(2^(b1))/(b1)

# 4) Calculate following:

#   (a) \sum\limits_{i = 10}^{100}(i^3 + 4i^2)

c1 <- c(10:100)
(c1)^3+4*(c1)^2

#   (b) \sum\limits_{i=1}^{25}(\frac{2^i}{i}+\frac{3^i}{i^2})