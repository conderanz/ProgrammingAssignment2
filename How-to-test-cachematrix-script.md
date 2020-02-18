## Set working directory
setwd("C:/Users/L05652/Desktop/Data Science/Training/Coursera/Module 2")
getwd()

## Set your working directory
setwd("C:/Users/L05652/GitRepos/ProgrammingAssignment2")

## Load the functions script
source("cachematrix.R")

## Create your square invertible matrix
c <- rbind(c(2, -3), c(4, -7))

## Call makeCacheMatrix()
f <- makeCacheMatrix()

## Check nothing is yet assigned
cacheSolve(f)

## Call the set method to assign your matrix
f$set(c)

## Check it was correctly assigned
f$get()

## Call the solve method (at this point the inverse matrix is calculated)
cacheSolve(f)

## Call the solve method again (the inverse matrix value is getting from memory)
cacheSolve(f)

## Call method getinv
f$getinv()

## Create another square invertible matrix
c2 <- rbind(c(4, 7), c(2, 6))

## Call the set method to assign your new matrix
f$set(c2)

## Every time you call "set", m turns NULL then "getinv" returns NULL
f$getinv()

## Call the solve method (at this point the inverse matrix is calculated)
cacheSolve(f)

## Call the solve method again (the inverse matrix value is getting from memory)
cacheSolve(f)

## Call method getinv
f$getinv()
