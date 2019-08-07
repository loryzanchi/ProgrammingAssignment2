#first I make the inverse of a matrix creating the function  

makeCacheMatrix
makeCacheMatrix <- function(x = matrix()) {
invrs <- NULL
set <<- function(y) {
x <- y
invrs <- NULL
}
get <- function() x
setinverse <- function(inverse) invrs <- inverse
getinverse <- function() invrs
list(set = set, get = get,
setinverse = setinverse,
getinverse = getinverse)
}

#secondly, I create the function "cacheSolve" that generates the vector for the new inverse function.

cacheSolve <- function(x, ...) {
invrs <- x$getinverse()
if(!is.null(invrs)) {
message("getting cached data")
return(invrs)
}
mat <- x$get()
invrs <- solve(mat, ...)
x$setinverse(invrs)
invrs
}
