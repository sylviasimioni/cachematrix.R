
~ Explanation:

    The function starts requesting the matrix
    The code will get and set the inverse of the matrix

cachematrix.R
makeCacheMatrix <- function(x = matrix()) {
inv <- NULL
set <- function(y) {
x <<- y
inv <<- NULL
}
get <- function() x
setinverse <- function(inverse) inv <<- inverse
getinverse <- function() inv
list(set=set, get=get, setinverse=setinverse, getinverse=getinverse)
}

~ Explanation:

    The cacheSolve verify if the matrix inverse is cached
    If the matrix is not null it will pop up a message "getting caching data" and return the inverse of the matrix

cacheSolve <- function(x, ...) {
inv <- x$getinverse()
if(!is.null(inv)) {
message("getting cached data.")
return(inv)
}
data <- x$get()
inv <- solve(data)
x$setinverse(inv)
inv
}

~ Explanation:

    Matrix used for the problem

x = rbind(c(1,0,0), c(0,1,0), c(0,0,1))
m = makeCacheMatrix(x)
cacheSolve(m)
