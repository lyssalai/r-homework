# r-homework-1
# This is Exercises 1. Vectors

# 1) Create vectors:
#   (a) (1, 2, 3, . . . , 19, 20)

1:20

#   (b) (20, 19, . . . , 2, 1)

20:1

#   (c) (1, 2, 3, . . . , 19, 20, 19, 18, . . . , 2, 1)

x <- c(1:20)
y <- c(19:1)
z <- c(x,y)
z

#   (d) (4, 6, 3) and assign it to the name tmp.

tmp <- c(4,6,3)

#   (e) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3) where there are 10 occurrences of 4.

rep(tmp, 10)

#***(f) (4, 6, 3, 4, 6, 3, . . . , 4, 6, 3, 4) where there are 11 occurrences of 4, 10 occurrences of 6 and 10 occurrences of 3.

#   (g) (4, 4, . . . , 4, 6, 6, . . . , 6, 3, 3, . . . , 3) where there are 10 occurrences of 4, 20 occurrences of 6 and 30 occurrences of 3.

rep(tmp, times=c(10,20,30))

# 2) Create a vector of the values of (e^x)(cos(x)) at x = 3, 3.1, 3.2, . . . , 6.

