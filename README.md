# R-Recycling-of-elements-in-a-vector

Recycling of elements in a vector –

Recycling occurs when vector arithmetic is performed on multiple vectors of different sizes. R takes the shorter vector and repeats them until it becomes long enough to match the longer one.
For example:-
CASE I: When the length of shorter vector divides evenly into the length of longer vector
> a <- c(10,2,23,4)+c(2,10)
> a

Output is:
[1] 12 12 25 14

The output is obtained by recycling the shorter vector c(2,10) until its length is same as the longer vector c(10,2,23,4). The vector c(2,10) vector repeated itself to form c(2,10, 2,10) so that it could successfully match the previous term.
So vector a is obtained as:
a <- (10+2, 2+10, 23+2, 4+10)
CASE II: When the length of shorter vector does not divide evenly into the length of longer vector, R will still apply the recycling method, but will throw a warning.
> b<- c(1,2,3,4,5,6,7) + c(1,3)

Warning message:
In c(1, 2, 3, 4, 5, 6, 7) + c(1, 3) :
  longer object length is not a multiple of shorter object length

> print(b)

Output is:
[1] 2 5 4 7 6 9 8

So vector b is obtained as:
b <- (1+1, 2+3, 3+1, 4+3, 5+1, 6+3, 7+1)

Example of recycling of elements.
> a <- c(10,2,23,4)+c(2,10)
> print(a)
[1] 12 12 25 14
>
> b<- c(1,2,3,4,5,6,7) + c(1,3)
Warning message:
In c(1, 2, 3, 4, 5, 6, 7) + c(1, 3) :
  longer object length is not a multiple of shorter object length
> print(b)
[1] 2 5 4 7 6 9 8
> 
> x <- c(1,2,3,4,5,6)+c(2,10)
> print(x)
[1]  3 12  5 14  7 16
> 
> y<- c(1,2,3,4,5,6,7) + c(10,30)
Warning message:
In c(1, 2, 3, 4, 5, 6, 7) + c(10, 30) :
  longer object length is not a multiple of shorter object length
> print(y)
[1] 11 32 13 34 15 36 17

