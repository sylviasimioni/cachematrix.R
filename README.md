
This Assignment is going to caching the inverse of a matrix

Matrix inversion is usually a costly computation and there may be some benefit to caching the inverse of a matrix rather than compute it repeatedly .

The code will write the following functions:

   1. makeCacheMatrix: This function will creates a special "matrix" object that can cache its inverse.
   
   2. cacheSolve: This function will computes the inverse of the special "matrix" returned by makeCacheMatrix above. If the inverse has already been calculated (and the matrix has not changed), then the cachesolve should retrieve the inverse from the cache.

