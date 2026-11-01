# Python Basics & Google Colab

Author: Manny Singh<br>
Contact: [<u>inbox@manny-singh.com</u>](mailto:inbox@manny-singh.com)

## 1. Introduction: What Is Python?

Before we start writing Python code, it's worth understanding what programming actually is, how computers understand our instructions, and why Python is particularly useful for data science.

### 1.1 Understanding Programming

Imagine you want a computer to calculate the average of a thousand numbers.

As humans, we can describe what we want in plain English:

"Add all the numbers together, then divide the result by how many numbers there are."

The problem is that computers don't speak English.

At their most fundamental level, computers execute instructions represented in machine code, which is made up of binary digits (0s and 1s).

These instructions tell the computer's processor to perform very specific operations, such as moving data, performing arithmetic, or comparing values.

Writing entire programs directly in machine code would be extremely difficult, which is why programming languages have been developed.

Programming languages allow us to express instructions in a form that is much easier for humans to read and write.

For example, in Python, we could calculate an average using:

```
numbers = [10, 20, 30, 40, 50]
average = sum(numbers) / len(numbers)
print(average)
```

Output:

```
30.0
```

This is an example of a high-level programming language.

High-level languages, such as Python, use concepts and instructions that are closer to human reasoning than to the internal workings of a computer.

However, the computer's processor still needs machine-level instructions to execute our program.

This is where compilers and interpreters come in.

- Compiler: Software that translates source code into another form, which may be machine code or an intermediate representation.

- Interpreter: Software that executes a program, often by processing its instructions directly or through an intermediate representation.

Different programming languages use different combinations of compilation and interpretation.

Python is commonly described as an *interpreted language*. In the standard Python implementation, our source code is first compiled into an intermediate form called bytecode, which is then executed by the Python interpreter.

Ultimately, the computer's processor carries out machine-level instructions.

Conceptually, the process looks like this:

```
Human intention
       |
       v
High-level programming language
       |
       | Compiler / Interpreter
       v
Instructions the computer can execute
       |
       v
Computer processor
       |
       v
Result
```

An important distinction is that programming languages are not simply translations of English. They have their own rules, structures, and vocabulary.

TLDR: Programming allows us to talk to a computer.

### 1.2 What Is Python?

Python is a high-level, general-purpose programming language.

Python is designed to be relatively easy to read and write, making it popular with both beginners and experienced developers.

For example, consider a program that prints a message:

```
print("Hello, world!")
```

Output:

```
Hello, world!
```

That's a complete Python program.

Python is used across a wide range of fields, including:

- Software development: Building applications, websites, and tools.

- Data science: Cleaning, analysing, and visualising data.

- Machine learning: Training models to identify patterns and make predictions.

- Automation: Performing repetitive tasks automatically.

- Scientific computing: Carrying out mathematical and scientific calculations.

- Artificial intelligence: Developing and experimenting with AI systems.

Another important feature of Python is its collection of libraries.

Libraries provide pre-written code that we can use rather than having to develop everything from scratch.

### 1.3 Why Python Is Popular in Data Science

Data science often involves working with large datasets, identifying patterns, performing calculations, and presenting findings.

Python is especially useful because it provides tools for all of these tasks.

Imagine our team is working with a dataset containing thousands of observations.

We might want to:

- Import the dataset.

- Identify missing values.

- Calculate summary statistics.

- Create graphs.

- Explore relationships between variables.

- Develop a predictive model.

Python allows us to carry out each of these steps within the same programming environment.

Its popularity in data science is largely due to its readability, flexibility, and extensive ecosystem of libraries.

Some commonly used libraries include:

| Library | Purpose |
| --- | --- |
| NumPy | Numerical calculations and arrays |
| Pandas | Data manipulation and analysis |
| Matplotlib | Creating graphs and visualisations |
| Seaborn | Statistical data visualisation |
| SciPy | Scientific and mathematical computing |
| Scikit-learn | Machine learning |

TLDR: Python can be extended with specialised tools for different tasks.

### 1.4 What Is Google Colab?

Google Colab is an online environment that allows us to write and execute Python code in a web browser.

Normally, running Python on your own computer requires installing Python and setting up an environment to execute your code.

Google Colab simplifies this process.

It provides access to a Python environment hosted on Google's infrastructure, meaning you can write Python code without having to install Python locally.

Colab is based on Jupyter notebooks.

A Jupyter notebook is an interactive document that can contain:

- Python code.

- Written explanations.

- Mathematical equations.

- Tables.

- Graphs.

- The results of executing code.

This combination makes notebooks useful for data science.

For example, we could load a dataset, display its first few rows, create a graph, and explain our findings, all within the same document.

### 1.5 How Python and Google Colab Work Together

Python is the programming language. Google Colab is an environment where we can write and execute Python code.

When we write Python code in Colab, that code is executed by a Python runtime connected to our notebook.

The process looks like this:

```
Google Colab Notebook
         |
         | Write Python code
         v
      Code Cell
         |
         | Run
         v
   Python Runtime
         |
         | Executes code
         v
       Output
```

For example:

```
x = 10
y = 20
print(x + y)
```

Output:

```
30
```

TLDR: We write Python code, and Google Colab gives us a place to run it.

## 2. Getting Started with Google Colab

### 2.1 Creating and Opening a Notebook

To get started:

1. Visit [<u>Google Colab</u>](https://colab.research.google.com/).

1. Sign in with your Google account.

1. Select the option to create a new notebook.

1. A new notebook will open in your browser.

A new notebook is usually given a default name such as:

```
Untitled0.ipynb
```

The `.ipynb` extension indicates that the file is a Jupyter notebook.

You can rename the notebook by clicking its name near the top of the page.

For example:

```
project_labs_analysis.ipynb
```

Unlike a traditional Python script (`.py`), a notebook can contain several separate blocks of code and written explanations.

This allows us to build and explain an analysis progressively.

### 2.2 Understanding the Colab Interface

When you open a notebook, you'll see several important components.

1. Notebook title

Displays the name of your notebook.

2. Code cells

Where you write and execute Python code.

3. Text cells

Where you write explanations, headings, and documentation.

4. Runtime controls

Allow you to connect to, restart, or change the computing environment running your code.

5. Files panel

Allows you to view files available within the current runtime.

6. Menu and toolbar

Provide options for adding cells, saving notebooks, managing the runtime, and accessing other features.

### 2.3 Code Cells vs Text Cells

Google Colab notebooks are made up of two types of cells.

Code cells

Code cells contain executable Python instructions.

For example:

```
name = "Rayan"
print("Hello", name)
```

Output:

```
Hello Rayan
```

When you run the cell, Colab executes the code and displays its output underneath.

Text cells

Text cells allow you to write explanations without executing code.

They use a formatting language called Markdown.

For example:

```
# Data Analysis
## Introduction
This notebook explores the relationship between
different variables in our dataset.
```

When rendered, Markdown creates formatted headings and paragraphs.

Text cells are useful for explaining what your code does and interpreting results.

For example:

```
Text Cell:
    Introduction to the dataset
Code Cell:
    Import the dataset
Text Cell:
    Explaining the variables
Code Cell:
    Calculate summary statistics
Text Cell:
    Interpret the findings
Code Cell:
    Create visualisations
```

This makes notebooks easier for other people to understand.

### 2.4 Writing and Running Your First Python Code

To execute Python code in Colab:

1. Create or select a code cell.

1. Type your Python code.

1. Click the play button beside the cell, or press `Shift + Enter`.

For example:

```
message = "Welcome to Project Labs!"
print(message)
```

Output:

```
Welcome to Project Labs!
```

### 2.5 Understanding Runtimes and Execution Order

A runtime is the computing environment responsible for executing the code in your notebook.

It stores variables, imported libraries, and other information created while your code runs.

For example, imagine the first cell contains:

```
x = 10
```

The second cell contains:

```
print(x)
```

As long as both cells are executed in that order, the second cell prints:

```
10
```

However, if you restart the runtime and execute only the second cell, Python will produce an error.

This happens because `x` has not yet been defined in the new runtime.

The order in which cells are executed matters.

A notebook might visually appear to be organised from top to bottom, but Python only knows about the code that has actually been executed in the current session.

For example:

```
x = 10
```

Later, you execute:

```
x = 50
```

If you now run:

```
print(x)
```

The result will be:

```
50
```

The current value depends on the most recently executed assignment, not where the cell appears in the notebook.

Colab runtimes are temporary. When a runtime disconnects or restarts, variables stored in memory are lost. Files stored only in the runtime may also disappear when its virtual machine is deleted.

Your saved notebook, however, remains available in Google Drive.

### 2.6 Saving and Sharing Notebooks

Google Colab notebooks can be stored in Google Drive.

You can also download notebooks as `.ipynb` files.

To share a notebook, use the Share button near the top of the page.

As with Google Docs, you can manage whether other people have viewing or editing access.

Sharing a notebook does not mean sharing your current runtime.

For example, suppose you've uploaded a dataset into your Colab session and written code that reads it.

If someone opens the shared notebook, thery may be able to see the code but not access the dataset you uploaded into your own runtime.

They will generally need access to the same data source.

## 3. Python Fundamentals

### 3.1 Understanding Python Syntax and Indentation

Every programming language has a set of rules describing how code must be written.

These rules are called syntax.

For example, Python understands:

```
print("Hello, world!")
```

But not:

```
print("Hello, world!"
```

The second example is missing a closing bracket, so Python raises a syntax error.

An important feature of Python is indentation.

Indentation refers to the spaces at the beginning of a line.

In many programming languages, indentation is primarily used to make code easier to read.

In Python, indentation also determines which instructions belong together.

For example:

```
age = 20
if age >= 18:
    print("You are an adult")
```

The indented line belongs to the `if` statement.

Without the required indentation:

```
if age >= 18:
print("You are an adult")
```

Python raises an error.

### 3.2 Variables and Assignment

A variable is a name that refers to a value stored in a program.

For example:

```
age = 24
```

Here:

- `age` is the variable name.

- `=` is the assignment operator.

- `24` is the assigned value.

We can now use that variable elsewhere:

```
print(age)
```

Output:

```
24
```

Variables can also be reassigned:

```
age = 24
age = 25
print(age)
```

Output:

```
25
```

The second assignment changes the value associated with `age`.

`=` does not mean mathematical equality in Python. It means assignment.

For example:

```
x = x + 1
```

This would be impossible as an ordinary mathematical equation.

In Python, however, it means:

1. Evaluate the expression `x + 1`.

1. Assign the result back to `x`.

Provided `x` has already been defined, this is perfectly valid.

For example:

```
x = 5
x = x + 1
print(x)
```

Output:

```
6
```

### 3.3 Basic Data Types

Python supports different kinds of data.

These are called data types.

Some of the most common are:

| Data type | Python name | Example |
| --- | --- | --- |
| Integer | int | 42 |
| Decimal number | float | 3.14 |
| Text | str | "Hello" |
| Boolean | bool | True |
| No value | NoneType | None |

Python automatically determines the type of each value.

You can check a value's type using `type()`:

```
print(type(age))
```

Output:

```
<class 'int'>
```

This becomes important because different data types support different operations.

For example, you can add two integers:

```
10 + 20
```

But attempting to add an integer to a string directly will cause an error:

```
10 + "20"
```

Python needs to know whether you intend to perform arithmetic or combine text.

### 3.4 Arithmetic Operators

Python supports the usual mathematical operations.

| Operator | Meaning | Example | Result |
| --- | --- | --- | --- |
| + | Addition | 10 + 5 | 15 |
| - | Subtraction | 10 - 5 | 5 |
| * | Multiplication | 10 * 5 | 50 |
| / | Division | 10 / 5 | 2.0 |
| // | Floor division | 11 // 5 | 2 |
| % | Modulo (remainder) | 11 % 5 | 1 |
| ** | Exponentiation | 2 ** 3 | 8 |

Normal division using `/` produces a floating-point result.

### 3.5 Comparison and Logical Operators

Sometimes we want our program to compare values rather than calculate something.

Python provides comparison operators.

| Operator | Meaning |
| --- | --- |
| == | Equal to |
| != | Not equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |

Comparisons produce Boolean values: either `True` or `False`.

We can combine comparisons using logical operators:

- `and`: Both conditions must be true.

- `or`: At least one condition must be true.

- `not`: Reverses a Boolean value.

These operators are particularly useful when we want our programs to make decisions.

### 3.6 Printing and Displaying Output

The `print()` function displays information.

We can print variables:

```
name = "manny"
age = 24
print(name)
print(age)
```

Or multiple values together:

```
print(name, age)
```

Output:

```
manny 24
```

Another useful feature is an f-string.

An f-string allows us to insert variables directly into text.

For example:

```
name = "manny"
age = 24
print(f"{name} is {age} years old.")
```

Output:

```
manny is 24 years old.
```

The `f` before the quotation marks tells Python to evaluate expressions enclosed in curly brackets.

This is useful when displaying results from calculations or data analysis.

### 3.7 Comments and Code Readability

A comment is text written inside your code that Python ignores when executing the program. They help explain what your code is doing.

In Python, comments begin with `#`.

Comments are particularly useful when collaborating with other people. However, comments shouldn't simply repeat what the code obviously does. The aim is to make code easier to understand, not to explain every individual character.

### 3.8 Type Conversion

Sometimes we need to convert a value from one data type to another. This is called type conversion. Python provides several built-in functions for this.

For example:

```
age = "24"
```

Here, `age` is a string, not an integer.

If we want to perform arithmetic, we can convert it:

```
age = int(age)
print(age + 1)
```

Output:

```
25
```

Other common conversion functions include:

```
int("10")       # String to integer
float("3.14")   # String to float
str(100)        # Integer to string
bool(1)         # Integer to Boolean
```

Not every conversion is possible.

For example:

```
int("hello")
```

Will produce an error because `"hello"` cannot be interpreted as an integer.

Type conversion is important in data science, where imported datasets may contain values stored in unexpected formats.

## 4. Working with Data in Python

So far, we've mostly worked with individual values.

However, programming often involves storing and manipulating collections of data.

Python provides several built-in data structures for this purpose.

### 4.1 Strings and String Operations

A string is a sequence of characters used to represent text.

Strings are written using quotation marks. Python supports both single and double quotation marks:

We can combine strings using `+`:

```
first_name = "Project"
last_name = "Labs"
print(first_name + " " + last_name)
```

Output:

```
Project Labs
```

We can also perform operations on strings.

For example:

```
message = "Hello World"
print(message.lower())
print(message.upper())
print(len(message))
```

Output:

```
hello world
HELLO WORLD
11
```

Here:

- `.lower()` converts text to lowercase.

- `.upper()` converts text to uppercase.

- `len()` returns the number of characters.

Strings are immutable, meaning their individual characters cannot be changed in place. If we want modified text, we create a new string.

### 4.2 Lists

A list is an ordered collection of values. They are written using square brackets.

For example:

```
scores = [65, 72, 81, 90]
```

A list can contain several values, and those values don't all need to have the same data type. However, lists containing similar types of data are often easier to work with.

We can access individual elements using their position, known as an index.

```
scores = [65, 72, 81, 90]
print(scores[0])
```

Output:

```
65
```

Python starts counting from zero, not one.

We can modify a list:

```
scores[0] = 70
```

We can also add elements:

```
scores.append(95)
```

And remove elements:

```
scores.remove(72)
```

Lists are mutable, meaning their contents can be changed after creation. They are useful whenever we need an ordered collection of values.

### 4.3 Tuples

A tuple is another ordered collection of values. They are commonly written using parentheses:

```
coordinates = (51.5, -0.1)
```

Like lists, tuples support indexing:

```
print(coordinates[0])
```

Output:

```
51.5
```

The main difference is that tuples are immutable. Once a tuple has been created, its individual elements cannot be reassigned.

For example:

```
coordinates[0] = 52.0
```

Will produce an error.

### 4.4 Dictionaries

A dictionary stores information as key-value pairs.

Rather than accessing values by their numerical position, we access them using a key.

For example:

```
student = {
    "name": "manny",
    "age": 24,
    "course": "mathematics and statistical science"
}
```

Here:

- `"name"` is a key.

- `"manny"` is its corresponding value.

We can retrieve information using the key:

```
print(student["name"])
```

Output:

```
manny
```

Dictionaries are particularly useful when storing information that has clear labels.

For example, we could represent a dataset observation as:

```
observation = {
    "patient_id": 101,
    "age": 35,
    "measurement": 12.5
}
```

We can also add or change dictionary values:

```
student["age"] = 22
student["university"] = "UCL"
```

Dictionaries are mutable, and each key must be unique within the dictionary.

### 4.5 Sets

A set is an unordered collection of unique values.

For example:

```
numbers = {1, 2, 3, 3, 4}
```

Although `3` appears twice, the set will contain it only once.

```
print(numbers)
```

The set contains:

```
{1, 2, 3, 4}
```

The display order of sets is not guaranteed. Sets are useful when we want to remove duplicate values or compare collections.

For example:

```
group_a = {"Rayan", "Nicole", "Em"}
group_b = {"Nicole", "Angela"}
print(group_a & group_b)
```

Output:

```
{'Nicole'}
```

The `&` operator returns the intersection of two sets: the values they have in common.

Sets also support operations such as union and difference.

Unlike lists and tuples, sets don't support indexing by position.

### 4.6 Indexing and Slicing

We've already seen that Python uses indexing to access individual elements.

For example:

```
scores = [10, 20, 30, 40, 50]
print(scores[0])
```

Output:

```
10
```

Python also supports negative indexing.

```
print(scores[-1])
```

Output:

```
50
```

Here, `-1` refers to the last element.

We can retrieve a range of elements using slicing.

For example:

```
scores[1:4]
```

Produces:

```
[20, 30, 40]
```

The general form is:

```
sequence[start:stop:step]
```

The starting index is included, while the stopping index is excluded.

For example:

```
scores[:3]     # First three elements
scores[2:]     # From index 2 onwards
scores[::2]    # Every second element
```

Slicing works with lists, strings, and tuples.

### 4.7 Choosing the Right Data Structure

Python provides several ways to store collections of data because different situations require different behaviour.

| Data structure | Ordered | Mutable | Allows duplicates |
| --- | --- | --- | --- |
| List | Yes | Yes | Yes |
| Tuple | Yes | No | Yes |
| Dictionary | Yes (insertion order) | Yes | Keys must be unique |
| Set | No guaranteed order | Yes | No |

In general:

- Use a list when you need an ordered collection that can change.

- Use a tuple when you want an ordered collection whose elements shouldn't be reassigned.

- Use a dictionary when values should be associated with descriptive keys.

- Use a set when you need unique values or set operations.

There isn't always one correct choice. The appropriate data structure depends on what you're trying to achieve.

## 5. Conditional Statements and Loops

Until now, our programs have mostly executed instructions in sequence.

However, we often want programs to make decisions or repeat actions.

Python provides conditional statements and loops for this purpose.

### 5.1 Boolean Logic

A Boolean is a value that can be either:

```
True
False
```

Boolean values are often produced by comparisons.

Boolean logic allows us to combine conditions.

For example:

```
has_data = True
has_permission = False
print(has_data and has_permission)
```

Output:

```
False
```

Because both conditions must be true for `and` to return `True`.

A useful summary:

| A | B | A and B | A or B |
| --- | --- | --- | --- |
| True | True | True | True |
| True | False | False | True |
| False | True | False | True |
| False | False | False | False |

Boolean logic forms the basis of many decisions made by programs.

### 5.2 `if`, `elif` and `else` Statements

An if statement allows Python to execute code only when a condition is satisfied.

For example:

```
score = 75
if score >= 70:
    print("First")
```

The indented code only executes if the condition is true.

We can introduce alternatives using `else`:

```
score = 65
if score >= 70:
    print("First ")
else:
    print("Below first threshold")
```

We can also check multiple conditions using `elif`, short for *else if*.

For example:

```
score = 65
if score >= 70:
    print("First")
elif score >= 60:
    print("Upper Second")
elif score >= 50:
    print("Lower Second")
else:
    print("Below Lower Second")
```

Output:

```
Upper Second
```

Python checks the conditions in order.

Once a condition is satisfied, its corresponding block executes and the remaining branches are skipped.

### 5.3 `for` Loops

A loop allows us to repeat instructions.

A `for` loop is commonly used to iterate through the elements of a collection.

For example:

```
scores = [65, 72, 81, 90]
for score in scores:
    print(score)
```

Output:

```
65
72
81
90
```

Here:

- `scores` is the list we're iterating through.

- `score` is a variable representing the current element.

- The indented code executes once for each element.

We can also use loops to perform calculations.

For example:

```
scores = [65, 72, 81, 90]
for score in scores:
    print(score * 2)
```

A commonly used function with `for` loops is `range()`.

For example:

```
for i in range(5):
    print(i)
```

Output:

```
0
1
2
3
4
```

We can also specify a starting value and step:

```
for i in range(2, 11, 2):
    print(i)
```

Output:

```
2
4
6
8
10
```

### 5.4 `while` Loops

A `while` loop repeatedly executes code for as long as a condition remains true.

For example:

```
count = 1
while count <= 5:
    print(count)
    count = count + 1
```

Output:

```
1
2
3
4
5
```

The loop continues until `count` becomes greater than five.

Unlike a `for` loop, a `while` loop doesn't necessarily iterate over a collection. Instead, it depends on a condition.

One important thing to remember is that the condition must eventually become false if we want the loop to finish normally.

For example:

```
while True:
    print("Hello")
```

This loop continues indefinitely unless interrupted or terminated. These loops are called infinite loops.

```
5.5 break and continue
```

Python provides two useful statements for controlling loops.

```
break
```

Immediately exits the innermost loop.

For example:

```
for number in range(10):
    if number == 5:
        break
    print(number)
```

Output:

```
0
1
2
3
4
```

The loop stops when `number` reaches five.

```
continue
```

Skips the remaining instructions in the current iteration and moves to the next one.

For example:

```
for number in range(5):
    if number == 2:
        continue
    print(number)
```

Output:

```
0
1
3
4
```

The value `2` is skipped, but the loop continues.

### 5.6 Iterating Through Lists and Dictionaries

We've covered how to iterate through lists, we can also iterate through dictionaries.

To iterate through the keys and values together, we can use `.items()`:

```
for name, score in scores.items():
    print(name, score)
```

This is useful when we want to process labelled information.

For example, we might iterate through a collection of observations and perform a calculation for each one.

## 6. Functions and Reusable Code

As programs become larger, we may find ourselves repeating the same instructions. Functions allow us to organise repeated tasks into reusable blocks of code.

### 6.1 What Is a Function?

A function is a named block of code that performs a particular task. Rather than writing the same calculation ourselves every time, we can use the existing function.

Python also allows us to create our own functions.

### 6.2 Defining Functions with `def`

We define a function using the `def` keyword.

For example:

```
def greet():
    print("Hello!")
```

This creates a function called `greet`.

However, defining a function doesn't automatically execute its contents.

To execute it, we need to call it:

```
greet()
```

Output:

```
Hello!
```

We can call the same function multiple times:

```
greet()
greet()
greet()
```

This allows us to reuse instructions without rewriting them.

### 6.3 Parameters and Arguments

Functions become more useful when they can accept information. A parameter is a variable defined in the function's declaration. An argument is the value supplied when calling the function.

For example:

```
def greet(name):
    print(f"Hello, {name}")
```

Here, `name` is a parameter.

When we call:

```
greet("Nicole")
```

The string `"Nicole"` is the argument.

Output:

```
Hello, Nicole
```

We can pass different arguments:

```
greet("Rayan")
greet("Em")
greet("Angela")
```

The function performs the same task using different input values.

Functions can also accept multiple parameters.

For example:

```
def add_numbers(a, b):
    print(a + b)
```

Calling:

```
add_numbers(10, 20)
```

Produces:

```
30
```

### 6.4 Returning Values

So far, our functions have displayed results using `print()`.

However, sometimes we want a function to produce a result that can be used elsewhere in our program.

This is where `return` comes in.

For example:

```
def add_numbers(a, b):
    return a + b
```

We can call the function and store its result:

```
result = add_numbers(10, 20)
print(result)
```

Output:

```
30
```

The distinction between `print()` and `return` is important.

- `print()` displays information.

- `return` sends a value back to the code that called the function.

Because the function returns a value, we can use it in another calculation. A function that finishes without an explicit return value returns `None`.

### 6.5 Built-in Python Functions

Python includes many built-in functions.

Some of the most common are:

| Function | Purpose |
| --- | --- |
| print() | Display information |
| len() | Find the length of a collection |
| sum() | Calculate the sum of values |
| min() | Find the minimum |
| max() | Find the maximum |
| abs() | Calculate absolute value |
| round() | Round a number |
| type() | Identify a value's type |
| int() | Convert to integer |
| float() | Convert to floating-point |
| str() | Convert to string |
| range() | Generate a sequence of integers for iteration |
| sorted() | Return a sorted list |

These functions allow us to perform common operations without writing all the underlying logic ourselves.

## 7. Using Python for Data Science in Google Colab

Now that we've covered the fundamentals of Python, we can look at how these concepts are used when working with real datasets.

### 7.1 Understanding Libraries and Packages

Python provides many built-in features, but it doesn't include every possible tool we might need.

For example, suppose we want to perform complex numerical calculations or create graphs. We could write all the necessary code ourselves, but this would be time-consuming. Instead, we can use libraries.

A library is a collection of reusable code designed to perform particular tasks.

In Python, code is organised into modules, and related modules can be grouped into packages.

The terms *library* and *package* are often used interchangeably in everyday discussion, although they aren't exactly the same thing.

Some commonly used data science libraries include:

- NumPy: Numerical calculations.

- Pandas: Working with datasets and tables.

- Matplotlib: Data visualisation.

- Scikit-learn: Machine learning.

These libraries allow us to build on existing software rather than starting from scratch.

### 7.2 Importing Libraries

Before using a library, we generally need to import it.

For example:

```
import math
```

We can now access functions provided by Python's `math` module.

We can also import a library using an alias.

For example:

```
import pandas as pd
```

Here, `pd` is a shorter name for Pandas.

We can then access Pandas functions through that alias.

Similarly, you'll often see:

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

These aliases are widely used conventions in Python data science.

### 7.3 An Introduction to NumPy, Pandas and Matplotlib

Three of the most important libraries in introductory Python data science are NumPy, Pandas, and Matplotlib.

NumPy

NumPy is primarily used for numerical computing.

One of its main features is the array, which allows us to efficiently store and manipulate numerical data.

For example:

```
import numpy as np
numbers = np.array([10, 20, 30, 40])
print(np.mean(numbers))
```

Output:

```
25.0
```

Here, `np.mean()` calculates the arithmetic mean of the array.

Pandas

Pandas is used for manipulating and analysing structured data.

Its most important data structure is the DataFrame, which resembles a spreadsheet or database table.

For example:

```
import pandas as pd
data = {
    "name": ["x", "y", "z", "s"],
    "score": [75, 82, 68, 91]
}
df = pd.DataFrame(data)
print(df)
```

This creates a table containing two columns: `name` and `score`.

We can then perform operations on those columns.

For example:

```
print(df["score"].mean())
```

Output:

```
79.0
```

Matplotlib

Matplotlib is used to create graphs and visualisations.

For example:

```
import matplotlib.pyplot as plt
names = ["x", "y", "z", "s"]
scores = [75, 82, 68, 91]
plt.bar(names, scores)
plt.xlabel("Student")
plt.ylabel("Score")
plt.title("Student Scores")
plt.show()
```

This creates a bar chart displaying each student's score.

These examples are only introductions.

### 7.4 Installing Packages in Colab

Google Colab comes with many commonly used Python libraries pre-installed.

However, sometimes we need a package that isn't available in the current runtime.

Python packages are commonly installed using pip.

For example, in Colab:

```
%pip install seaborn
```

This installs Seaborn into the current Python environment.

The `%pip` command is a notebook feature that runs the package installer in the active Python environment.

Once the package has been installed, we can import it:

```
import seaborn as sns
```

Remember that Colab runtimes are temporary. If you install a package into one runtime, it may need to be installed again when you start a new runtime. For this reason, notebooks that depend on additional packages should include the installation instructions needed to reproduce their environment.

### 7.5 Uploading and Accessing Datasets

In data science, we'll often work with data stored in external files.

Common formats include:

- CSV (`.csv`)

- Excel (`.xlsx`)

- JSON (`.json`)

- Text files (`.txt`)

A CSV, or comma-separated values file, stores tabular data as text.

Each line represents a row, with commas separating the values.

To upload a file into Colab, you can use the Files panel.

Alternatively, you can use Python:

```
from google.colab import files
uploaded = files.upload()
```

Colab will open a file-selection interface.

After uploading a file, it can be accessed from the runtime's filesystem. However, files uploaded directly into the runtime are temporary. If you need a dataset to remain available across sessions, you can store it in Google Drive or another persistent location and access it from your notebook.

### 7.6 Reading CSV Files with Pandas

Once we've uploaded a dataset, we can load it using Pandas.

For example, suppose we've uploaded a file called:

```
scores.csv
```

We can read it using:

```
import pandas as pd
df = pd.read_csv("scores.csv")
```

Here:

- `pd` is our alias for Pandas.

- `read_csv()` reads a CSV file.

- `"scores.csv"` is the file we want to open.

- `df` is the variable containing the resulting DataFrame.

We can display the dataset:

```
print(df)
```

Or, in Colab, simply enter:

```
df
```

Colab will display the DataFrame as a formatted table.

If the dataset is large, we might only want to see its first few rows:

```
df.head()
```

By default, this displays the first five rows.

We can specify a different number:

```
df.head(10)
```

This displays the first ten rows.

### 7.7 Inspecting and Exploring a Dataset

Once we've loaded a dataset, we usually want to understand its structure before performing more detailed analysis.

Pandas provides several useful methods for this.

Viewing the first few rows

```
df.head()
```

Viewing the last few rows

```
df.tail()
```

Checking the dataset's dimensions

```
df.shape
```

This returns a tuple containing the number of rows and columns.

For example:

```
(1000, 5)
```

Means the dataset contains 1,000 rows and 5 columns.

Viewing the column names

```
df.columns
```

Checking the data types and missing-value information

```
df.info()
```

Generating descriptive statistics

```
df.describe()
```

By default, this summarises the numerical columns and includes statistics such as the count, mean, standard deviation, minimum, and maximum.

Checking for missing values

```
df.isnull().sum()
```

This returns the number of missing values in each column.

For example:

```
age             0
measurement    12
category        3
```

This tells us that the `measurement` column contains 12 missing values and the `category` column contains 3.

TLDR: Pandas allows us to load datasets into DataFrames, inspect their structure, and begin understanding the information they contain.

## 8. Common Errors and Troubleshooting

Python provides error messages that help us understand what went wrong.

### 8.1 Understanding Python Error Messages

When Python encounters a problem, it may stop executing the current operation and display an error.

For example:

```
print(unknown_variable)
```

Produces something similar to:

```
NameError: name 'unknown_variable' is not defined
```

This error tells us that Python doesn't recognise the variable name.

Python error messages often include:

- The type of error.

- A description of what went wrong.

- The line where the problem occurred.

- A traceback showing how execution reached the error.

The traceback is useful for identifying the source of a problem.

When debugging, start by reading the error type and message carefully.

### 8.2 Syntax and Indentation Errors

Two common errors for beginners are `SyntaxError` and `IndentationError`.

SyntaxError

Occurs when Python cannot interpret the structure of your code.

For example:

```
print("Hello"
```

The closing bracket is missing.

IndentationError

Occurs when Python's indentation rules are not followed.

For example:

```
if True:
print("Hello")
```

The `print()` statement should be indented:

```
if True:
    print("Hello")
```

These errors are usually fixed by checking the punctuation and structure of the relevant lines.

### 8.3 Name, Type and Index Errors

NameError

Occurs when we refer to a name that hasn't been defined.

```
print(score)
```

If `score` hasn't been assigned a value, Python raises a `NameError`.

TypeError

Occurs when we attempt an operation that isn't supported for the given data types.

For example:

```
10 + "20"
```

Python cannot directly add an integer and a string.

IndexError

Occurs when we try to access a position that doesn't exist in a sequence.

For example:

```
numbers = [10, 20, 30]
print(numbers[5])
```

The list only contains three elements, with indices `0`, `1`, and `2`.

Attempting to access index `5` produces an error.

These errors become easier to recognise with experience.

### 8.4 Writing Readable and Reproducible Notebooks

To make notebooks easier to understand and reproduce:

- Organise code cells in a logical order.

- Explain important steps using text cells.

- Include the necessary imports.

- Make required datasets accessible to the team.

- Document additional package requirements.

- Avoid relying on temporary files without explaining how to recreate them.

- Avoid including passwords, API keys, or confidential information.

## 9. Python & Google Colab Quick Reference

### 9.1 Essential Python Terminology

| Term | Meaning |
| --- | --- |
| Programming | Writing instructions for computers to execute |
| High-level language | Programming language designed to be relatively readable by humans |
| Machine code | Instructions directly executable by a processor |
| Python | High-level, general-purpose programming language |
| Interpreter | Software that executes program instructions |
| Syntax | Rules governing how code must be written |
| Variable | Name referring to a value |
| Data type | Classification of a value |
| String | Sequence of characters representing text |
| Integer | Whole-number data type |
| Float | Floating-point numerical data type |
| Boolean | True or False value |
| List | Ordered, mutable collection |
| Tuple | Ordered, immutable collection |
| Dictionary | Collection of key-value pairs |
| Set | Unordered collection of unique values |
| Index | Position of an element in a sequence |
| Loop | Structure that repeats instructions |
| Function | Reusable block of code |
| Parameter | Named input defined by a function |
| Argument | Value passed to a function |
| Return value | Result sent back by a function |
| Library | Collection of reusable code |
| DataFrame | Two-dimensional labelled data structure provided by Pandas |
| Notebook | Interactive document containing code, text, and output |
| Runtime | Environment in which notebook code executes |

### 9.2 Python Syntax Cheat Sheet

Variables

```
x = 10
name = "manny"
```

Arithmetic

```
a + b
a - b
a * b
a / b
a // b
a % b
a ** b
```

Comparisons

```
a == b
a != b
a > b
a < b
a >= b
a <= b
```

Logical operators

```
and
or
not
```

Lists

```
numbers = [1, 2, 3]
numbers[0]
numbers.append(4)
```

Dictionaries

```
student = {"name": "manny", "age": 24}
student["name"]
```

Conditional statements

```
if condition:
    # Code
    pass
elif another_condition:
    # Code
    pass
else:
    # Code
    pass
```

Here, `pass` is a statement that does nothing. It is useful as a placeholder when Python requires a statement inside a block.

For loops

```
for item in collection:
    print(item)
```

While loops

```
while condition:
    # Code
    pass
```

Functions

```
def function_name(parameter):
    return parameter * 2
```

Importing libraries

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

### 9.3 Common Built-in Functions

| Function | Example | Purpose |
| --- | --- | --- |
| print() | print("Hello") | Display output |
| len() | len([1, 2, 3]) | Count elements |
| sum() | sum([1, 2, 3]) | Sum values |
| min() | min([1, 2, 3]) | Minimum value |
| max() | max([1, 2, 3]) | Maximum value |
| abs() | abs(-5) | Absolute value |
| round() | round(3.14159, 2) | Round a number |
| type() | type(10) | Identify data type |
| int() | int("10") | Convert to integer |
| float() | float("3.5") | Convert to float |
| str() | str(100) | Convert to string |
| range() | range(5) | Generate values for iteration |
| sorted() | sorted([3, 1, 2]) | Return sorted values |

### 9.4 Useful Google Colab Shortcuts

| Shortcut | Action |
| --- | --- |
| Shift + Enter | Run the current cell and select the next |
| Ctrl/Cmd + Enter | Run the current cell without advancing |
| Ctrl/Cmd + M, then B | Insert a code cell below |
| Ctrl/Cmd + M, then A | Insert a code cell above |
| Ctrl/Cmd + M, then M | Convert the cell to a text cell |
| Ctrl/Cmd + M, then Y | Convert the cell to a code cell |

### 9.5 Overview of a Typical Data Science Notebook

The following diagram brings together the concepts covered in this guide.

```
              GOOGLE COLAB
                   |
                   v
             Python Notebook
                   |
                   v
           Import Libraries
                   |
                   v
              Load Dataset
                   |
                   v
            Inspect the Data
                   |
                   v
             Clean the Data
                   |
                   v
           Analyse the Data
                   |
                   v
             Visualisations
                   |
                   v
          Interpret the Results
                   |
                   v
          Save / Share Notebook
```
