## Programming Assignment 2: Lexical Scoping

### Caching the inverse of a matrix

* Please copy the file in your current working directory and source the .R file
* Initialize the matrix using the makeCacheMatrix
* Solve to get inverse matrix by calling cacheSolve


Here is a brief snapshot of the execution of my program

> source("cachematrix.R")
> mat1 <- makeCacheMatrix(matrix(1:4,2,2))
> mat1$get()
     [,1] [,2]
[1,]    1    3
[2,]    2    4
> mat1$getInverse()
NULL
> cacheSolve(mat1)
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> cacheSolve(mat1)
getting cached data
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> mat1$getInverse()
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5

#Another example

> mat2<-makeCacheMatrix(matrix(c(3,6,2,5), 2, 2))
> mat2$get()
     [,1] [,2]
[1,]    3    2
[2,]    6    5
> mat2$getInverse()
NULL
> mat2$get()
     [,1] [,2]
[1,]    3    2
[2,]    6    5
> cacheSolve(mat2)
          [,1]       [,2]
[1,]  1.666667 -0.6666667
[2,] -2.000000  1.0000000
> cacheSolve(mat2)
getting cached data
          [,1]       [,2]
[1,]  1.666667 -0.6666667
[2,] -2.000000  1.0000000
> 