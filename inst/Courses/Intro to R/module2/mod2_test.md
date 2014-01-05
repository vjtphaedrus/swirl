Intro to R - Module 2
========================================================

So the value of `y` is `3`, which we recognize as an integer. However, R views `3` differently. To see this, type `typeof(y)`.


```r
typeof(y)
```

```
## Error: object 'y' not found
```


---

The `typeof()` function tells us the data type of the object given to it. In this case, R recognizes `3` as being of type "double", which just means a real (decimal) number.

---

If you want to use integers in R, you must specify the `L` suffix. Otherwise, R will generally treat numeric values as real numbers.

---

Suppose we really wanted `y` to store the integer `3L` and not the real number `3`. We can correct our mistake by assigning `3L` to `y`, essentially "overwriting" the old value. Do this now.


```r
y <- 3L
```


---

Let's check the type of `y` again with `typeof(y)` to make sure we got it right this time.


```r
typeof(y)
```

```
## [1] "integer"
```


---







---

First, it's useful to distinguish data structures from data types. Data structures are like containers that hold data. Data types describe fundamental properties of that data.

---

The most basic data structure in R is the vector. Vectors are just collections of objects. Even single numbers are considered vectors of length 1.

---

There are two different flavors of vectors in R: atomic vectors and lists. The data contained in an atomic vector must all be of the same type, whereas the data contained in a list can be of many different types.

---

For now, we'll stick with atomic vectors, since they are so fundamental to everything else in R.

---

The easiest way to create an atomic vector in R is with the `c()` function, which stands for "concatenate" or "combine".

---

To create a vector containing the real numbers 2, 3, and 4, type `c(2, 3, 4)`. Try it now and store the result in a variable called `z`.


```r
z <- c(2, 3, 4)
```


---

Since `z` is an atomic vector, all of its elements must be the same data type. In this case, we might expect the data type to be "real" or "decimal". In fact, R has a special name for real numbers: "double" (synonym "numeric").

---

The 4 most common types of atomic vectors in R are "character", "double", "integer", and "logical" (TRUE/FALSE).

---

If you want to know the type of data stored in an atomic vector, use the `typeof()` function. Try `typeof(z)` to see how R views our numbers 2, 4, 6, and 8.

---

So R considers 2, 4, 6, and 8 to be of type "double", which essentially means decimal or real numbers. This is R's default data type for numeric data. If you explicitly want an integer in R, you have to specify the `L` suffix.

---

For example, let's create a new vector called intVect that contains the integers 3 and 7. To do this, type `intVect <- c(3L, 7L)`.

---

Now, check that intVect is of type integer using the `typeof()` function.

---

Create one of each of 4 most common types of atomic vector


```r
numVect <- c(4, 2.12, 88, 0.3)
intVect <- c(3L, 7L)
charVect <- c("Nick", "Carchedi")
logVect <- c(TRUE, FALSE, TRUE)
```
