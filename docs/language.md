Placebo Language

This document describes the current experimental Placebo language implementation.

The language is still evolving. Syntax and semantics may change between releases.

---

Variables

Variables can be created using "store".

store name = "Salem"
store age = 21

Variables can subsequently be assigned new values.

age = 22

---

Output

Use "output" or "print".

output "Hello"
print "Hello"

---

Strings

Strings are written using quotes.

store name = "world"
output name

Placebo supports interpolation using parentheses inside strings.

store name = "world"
output "Hello, (name)"

---

Numbers

Placebo supports numeric values and arithmetic operations.

store x = 10
store y = 5

output x + y
output x - y
output x * y
output x / y

---

Lists

Lists use square brackets.

store numbers = [1, 2, 3, 4]

Elements can be accessed by index.

output numbers[0]

---

Dictionaries

Dictionaries use braces.

store person = {
    name: "Salem",
    age: 21
}

Values can be accessed through keys.

output person.name

---

Conditions

if age > 18
    output "adult"
else
    output "minor"
end

Multiple conditions can be expressed using "else if".

if score > 90
    output "excellent"
else if score > 70
    output "good"
else
    output "keep going"
end

---

Boolean Logic

Placebo supports:

and
or
not

Example:

if age > 18 and score > 50
    output "accepted"
end

---

Loops

While

store x = 0

while x < 10
    output x
    x = x + 1
end

Repetition

loop 5 times
    output "hello"
end

Iteration

each item in items
    output item
end

---

Functions

Functions are declared using "function".

function greet(name)
    output "Hello, (name)"
end

Call a function by using its name:

greet("world")

---

Return Values

Functions can return values.

function add(a, b)
    return a + b
end

store result = add(2, 3)

output result

---

Lambdas

Placebo supports lambda expressions.

store double = lambda x: x * 2

---

Error Handling

Placebo supports "try" and "catch".

try
    ...
catch error
    output error
end

Programs can explicitly raise errors.

error "Something went wrong"

---

Loop Control

Loops can use:

stop

to terminate the current loop, and:

skip

to skip the current iteration.

---

Comments

Comments can use "#".

# This is a comment

output "Hello"

The "comment" keyword is also recognized by the current implementation.

---

Built-ins

The current implementation provides built-in functionality including:

length
type
random
down
up
min
max
number
text
range
input
reverse
split
remove
has
read
write
append
exists
fetch

The exact behavior of individual built-ins is part of the evolving language specification.

---

Experimental Semantics

Some aspects of the language are not yet considered final.

Current areas under active refinement include:

- Assignment
- Mutation
- Loop variable scope
- Dictionary key behavior
- Runtime error locations
- Asynchronous operations
- File loading
- Host/runtime boundaries

If behavior seems surprising, please open an issue with a minimal example.

---

Design Goal

Placebo explores a simple question:

«Can programming syntax communicate the intent of a program more directly without sacrificing the expressive power of a general-purpose language?»

The project is an experiment toward answering that question.
