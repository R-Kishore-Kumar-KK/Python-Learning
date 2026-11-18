# Python -- Day 1 Notes

> **Course:** 100 Days of Code: The Complete Python Pro Bootcamp\
> **Day:** 1 -- Working with Variables in Python to Manage Data\
> **Course link:** [Udemy -- Python
> Bootcamp](https://www.udemy.com/share/103IHM3@cwMHeY3Gs9PXkml2BRW5MD_XXLa39dnCsEOuBVcn5Xm21kmMAVUAlmDMnJ0RZ5I2/)

These are my personal notes from Day 1 of the course. The explanations
are written in my own words, with examples and practice programs for
future reference.

------------------------------------------------------------------------

## 1. The `print()` Function

The `print()` function displays information in the console.

A string is a sequence of characters. In Python, strings are commonly
written inside single quotes (`'...'`) or double quotes (`"..."`). The
quotation marks indicate where the string begins and ends; they are not
included in the displayed output.

### Example

``` python
print("Content to Print")
```

**Output**

``` text
Content to Print
```

### Printing multiple lines

``` python
print("1. Mix 500g of Flour, 10g Yeast and 300ml Water in a bowl.")
print("2. Knead the dough for 10 minutes.")
print("3. Add 3g of Salt.")
print("4. Leave to rise for 2 hours.")
print("5. Bake at 200 degrees C for 30 minutes.")
```

Each `print()` call displays its content on a separate line by default.

------------------------------------------------------------------------

## 2. New Lines Using `\n`

The `\n` escape sequence moves the output to a new line.

``` python
print("Hello World!\nHello World!\nHello World!")
```

**Output**

``` text
Hello World!
Hello World!
Hello World!
```

Here, `\n` tells Python to start a new line within the same string.

------------------------------------------------------------------------

## 3. String Concatenation

String concatenation means joining two or more strings together.

In Python, the `+` operator can be used to concatenate strings.

``` python
print("Hello" + "Kishore")
print("Hello " + "Kishore")
print("Hello" + " Kishore")
print("Hello" + " " + "Kishore")
```

**Output**

``` text
HelloKishore
Hello Kishore
Hello Kishore
Hello Kishore
```

Notice that spaces must be included in the strings if you want a space
between the words.

------------------------------------------------------------------------

## 4. Indentation Error

An `IndentationError: unexpected indent` occurs when a line has an
unexpected number of spaces or tabs at the beginning.

Python uses indentation to identify code blocks. Statements belonging to
the same block must follow consistent indentation. Indentation is
normally introduced after a statement ending with a colon (`:`), such as
`if`, `for`, `while`, or `def`.

### Example of an indentation problem

``` python
print("Hello")
    print("World")
```

The second line has an unexpected indentation, so Python raises an
error.

### Corrected version

``` python
print("Hello")
print("World")
```

**Remember:** Use consistent indentation. Four spaces are the standard
indentation level for a Python code block.

------------------------------------------------------------------------

## 5. Debugging Practice

Debugging means identifying and correcting errors in a program.

The Day 1 debugging exercise involved finding issues such as: - Missing
or misplaced quotation marks. - Incorrect indentation. - Missing closing
parentheses. - Misspelled function names. - Incorrect escape-sequence
usage.

### Corrected program

``` python
print("Notes from Day 1")
print("The print statement is used to output strings")
print("Strings are strings of characters")
print("String Concatenation is done with the + sign")
print("New lines can be created with a \\n")
```

**Important:** In the last line, `\\n` displays the literal characters
`\n`. To actually create a new line, use `\n` directly inside the
string.

------------------------------------------------------------------------

## 6. Getting User Input Using `input()`

So far, we have used `print()` to display information in the console.
The `input()` function allows us to receive information from the user
through the console.

### Syntax

``` python
input("A prompt for the User")
```

The prompt is displayed in the console, and Python waits for the user to
enter a value. After the user presses Enter, the entered value is
returned as a string.

### Example 1 -- Getting a name

``` python
print("Hello " + input("What is your Name?"))
```

**Example execution**

``` text
What is your Name? Kishore
Hello Kishore
```

The `input()` function is evaluated first. Python waits for the user's
response and then concatenates that response with `"Hello "`.

### Example 2 -- Adding an exclamation mark

``` python
print("Hello " + input("What is Your Name?") + "!")
```

**Example output**

``` text
Hello Kishore!
```

### Commenting code

Use `Ctrl + /` in many code editors to comment or uncomment the selected
line.

A single-line comment in Python starts with `#`.

``` python
# This is a comment
print("Hello World")
```

Comments are ignored when Python executes the program.

------------------------------------------------------------------------

## 7. Variables

A variable is a name used to refer to a value stored in a program.

Variables allow us to store data and reuse it whenever needed.

### Example 1 -- Storing user input

``` python
name = input("What is your name?")
print(name)
```

Here: - `name` is the variable. - `input()` receives the user's name. -
The entered value is assigned to `name`. - `print(name)` displays the
stored value.

### Example 2 -- Assigning a value directly

``` python
name = "Jack"
print(name)
```

**Output**

``` text
Jack
```

### Example 3 -- Using variables in multiple statements

``` python
name1 = input("What is your name?")
print("Hello, " + name1)
print(len(name1))

name2 = "Kumar"
print("Hello, " + name2)
print(len(name2))
```

------------------------------------------------------------------------

## 8. The `len()` Function

The built-in `len()` function returns the number of items in an object.
When used with a string, it returns the number of characters in that
string, including spaces.

### Example 1

``` python
print(len(input("What is your name?")))
```

Python first receives the input and then calculates the length of the
entered string.

### Example 2 -- Storing the length in a variable

``` python
username = input("What is your name?")
length = len(username)
print(length)
```

**Example execution**

``` text
What is your name? Kishore
7
```

------------------------------------------------------------------------

## 9. Variable Naming Rules in Python

Follow these rules when naming variables:

1.  A variable name must start with a letter (`a-z`, `A-Z`) or an
    underscore (`_`).
2.  The remaining characters can contain letters, numbers (`0-9`), and
    underscores.
3.  Variable names are case-sensitive. For example, `myVar` and `myvar`
    are different variables.
4.  Python reserved keywords such as `if`, `for`, `while`, `class`, and
    `def` cannot be used as variable names.
5.  Use meaningful names that describe the data being stored.

### Common naming conventions

  Naming style             Example       Common usage
  ------------------------ ------------- -------------------------
  `snake_case`             `user_name`   Variables and functions
  `SCREAMING_SNAKE_CASE`   `MAX_SIZE`    Constants
  `PascalCase`             `MyClass`     Class names

### Examples

``` python
username = "Kishore"
user_age = 28
_name1 = "Vikkash"
```

------------------------------------------------------------------------

## 10. Swapping Variable Values

The uploaded `VariableTest.py` file also contains a practice example of
swapping values between two variables.

Swapping means exchanging the values stored in two variables.

### Example using a temporary variable

``` python
glass1 = "milk"
glass2 = "juice"

temp = glass1
glass1 = glass2
glass2 = temp

print(glass1)
print(glass2)
```

**Output**

``` text
juice
milk
```

The temporary variable `temp` holds the first value while the two
variables exchange their values.

------------------------------------------------------------------------

## 11. Day 1 Project -- Band Name Generator

The Band Name Generator is the Day 1 project. It uses `print()`,
`input()`, variables, and string concatenation.

### Program

``` python
print("Welcome to the Band Name Generator.")

city = input("What's the name of the City you grew up in?\n")
petname = input("What's your pet's name?\n")

print("Your Band Name could be " + city + " " + petname)
```

### Example execution

``` text
Welcome to the Band Name Generator.
What's the name of the City you grew up in?
Cuddalore
What's your pet's name?
Tommy
Your Band Name could be Cuddalore Tommy
```

### Concepts used in this project

-   `print()` -- Displays messages in the console.
-   `input()` -- Receives information from the user.
-   Variables -- Stores the city and pet name.
-   String concatenation (`+`) -- Combines the input values into one
    output.

------------------------------------------------------------------------

## 12. Day 1 Practice Files

The following Python files were created while practising the concepts
covered on Day 1.

  -----------------------------------------------------------------------
  File name                           What it covers
  ----------------------------------- -----------------------------------
  `task.py`                           Basic printing, multiple print
                                      statements, new lines, and string
                                      concatenation

  `DebuggingTest.py`                  Debugging and correcting Python
                                      syntax issues

  `InputTest.py`                      Getting user input and combining it
                                      with strings

  `VariableTest.py`                   String length, variables, and
                                      swapping values

  `BandNameGenerator.py`              Day 1 project using input,
                                      variables, and concatenation
  -----------------------------------------------------------------------

Keep these `.py` files in the same GitHub repository as this notes
document so the examples can be run and revisited.

------------------------------------------------------------------------

## 13. Day 1 Learning Summary

By the end of Day 1, I learned:

-   How to display text using `print()`.
-   How to use `\n` to create new lines.
-   How to concatenate strings using `+`.
-   What indentation errors are and why indentation matters.
-   How to identify and correct basic errors through debugging.
-   How to receive user input using `input()`.
-   How to store and reuse values using variables.
-   How to calculate string length using `len()`.
-   The basic rules and conventions for naming variables.
-   How to swap values between two variables.
-   How to build a simple Band Name Generator project.

**Day 1 completed -- Python fundamentals and the Band Name Generator.**

------------------------------------------------------------------------

*Personal learning notes. Examples and explanations are based on my Day
1 course lessons and practice files.*
