# week 3
## Variables

variables are assigned with ```=```
variables cannot start with a number, contain spaces, etc

- CamelCase
- mixedCase
- snake_case

Variables can be overwritten

### Data types

#### Numerical

##### Integers

Whole numbers

1, 2, 3, 4, 5... etc.

##### Float

Decimal numbers

1.5, 20.12, 8.3... etc.

#### Textual

##### Strings

Stores text
- single words
- whole sentences

You can grab individual parts of a string by placing the numerical position/index of the characters in brackets next to the variable name:

```one_word = "cat"```

```one_word[0]```

Returns "c".

Python is 0-indexed (starts at 0 instead of 1)

#### Slicing

Slicing is when we identify a range of characters with a colon:

```paragraph = "no knight is more"```

```paragraph[0:9]```

#### Grouping

Grouping stores a collection of strings.

```list = ["one", "two", "three"]```
```list[2]```

Find variables and their type

```type(variable_name)```

### Comparisons

#### Operators

```==```

Equal to

```!=```

Not equal to

```<```

Less than

```>```

Greater than

```<=```

Equal to or less than

```>=```

Equal to or greater than

#### Booleans

Booleans can use and & or statements

```True and False```

returns False

```True or False```

returns True

## Flow charts

Useful for thinking like a computer.

Plan out a project in advance.

## Basic structure of a Python solution

* check out Programming Historian

### Conditional statements

#### if/else statements

if _ do this

elif _ do this

else do this

```
if condition 1:
    result 1
elif condition 2:
    result 2
else:
    result 3
```

## Homework
Check out [Python documentation](www.python.org/doc/) and find one small thing to mention next class.