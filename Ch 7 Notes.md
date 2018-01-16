# Functions and Vectors

## **Functions**
A named sequence of instructions (lines of code) we **call** a function to do those steps.

Example:
```
upcase <- toupper("Hello World")
```
- **Writing Functions**

By writing functions we can:
  - Easily reuse algorithms
  - Debug one piece of your program at a time
  - Abstract an algorithm to focus on the bigger picture.

Example:
```
FunctionName <- function(name) {
  # body: instructions (code)
}
```

**Function Arguments**:
- Arguments are **variables** (labels) that are assigned values when the function is called.

**Scope**:
- Variables created inside a function (including the arguments) are called **local variables**, and so are only available **inside** the function.

**Return Values**
- Functions can **return** a single value as a result. This is different than printing an output.

Example:
```
MakeFullName <- function(first.name, last.name) {
  full.name <- paste(first.name, last.name)

  return(full.name)
}

my.full.name <- MakeFullName("Muhammad, Hussain") #Will print Muhammad Hussain
```

## **Vectors**

- **Vectors** are _one dimensional collections_ of values that are all stored in a single variable. For example, a "set" of words (strings) or numbers. **Elements must all be of the same type.**

- **Vectorized Operations** we can use mathematical (+. -, * , /) or relational (<, >, ==) operators on vectors. These operations are applied **member-wise**

Example:
```
v1 <- c(3, 1, 4, 1, 5)
v2 <- c(2, 4, 1, 5, 1)

v3 <- v1 + v2
v4 <- v2 * v1
```

- **Recycling** if one vector is shorter than the other, then the elements of the shorter vector are **recycled**.
