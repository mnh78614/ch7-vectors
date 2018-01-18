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

## **Everything is a vector**
- **Literals** are just vectors within a single element in them.
- Using "scalars" (single values) as operands causes the **recycling** behavior so that the operand is applied to every element in the vector.
- **Vectorized functions**, most functions work with vectors.
- **Vector Indices**, we can refer to each element in a vector by its **index**. It starts at '1', unlike '0' in Java.
- **Bracket Notation**, Access individual values in a vector by using **bracket notation**, putting the **index** of the element inside brackets after the vector name.

Example:
```
vowels <- c('a', 'e', 'i', 'o', 'u')
first.vowel <- vowels[1]
print(first.vowel) # prints a
```

- **Multiple Indices**, we can make our "position vector" have multiple elements to extract a **subset** of elements.
- **Vector Filtering**, we can use **logical** values inside the brackets instead of a position vector. This will extract every element that corresponds with true.

## Lists

- **Lists**, like vectors, are _one dimensional collections_ of values, but with some additional features:
  - Lists can store elements of different types
  - List elements can be **tagged** with a variable name

Example:

```
person <- list(name = 'Ada", salary = 78000, in.union = TRUE)
```

- **Maps**
  - Tagging elements in lists cause them to act like _maps_, where one value "maps" or gives directions to another.
- Accessing Lists: we access individual values in a list by using **dollar notation**. This looks up an element by its tag.

Example:
```
person <- list(name = 'Ada", salary = 78000, in.union = TRUE)

person$first.name # person's first.name ('Ada')
person$salary # person's salary (78000)
```

- Double - Bracket Notation: we can also access list elements by using **double-bracket notation**, specifying either the numeric index of the element or the tag.

Example:
```
person <- list(name = 'Ada", salary = 78000, in.union = TRUE)

person[[first.name]] # person's first.name ('Ada')
person[[salary]] # person's salary (78000)

person[[1]] # 'Ada'
person[[4]] # 'TRUE'
```

## Vectors use single-bracket when accessing, Lists use double-brackets
