This repository contains a concise and easy-to-follow pseudocode reference based on the style used in Starting Out with Programming Logic and Design.

It is designed to help students quickly understand and apply core programming concepts without worrying about syntax from specific programming languages.

Below, you’ll find sections organized in a logical learning order—from basic concepts to more advanced constructs.

---

## Variable Declarations

### Syntax

`Declare dataType variableName`

### Data Types

`Declare Integer count`
`Declare Real average`
`Declare String name`
`Declare Boolean isValid`

### Assigning Values

`Set count = 10`
`Set average = 85.5`
`Set name = "Ali"`
`Set isValid = true`

---
## Input / Output

### Input

`Input name`
`Input age`

### Output

`Display "Hello World"`
`Display name`
`Display "Your average is ", average`

Prompting the user:
`Display "Enter your age: "`
`Input age`

---
## Arithmetic Operators

| Operator | Function       |
| -------- | -------------- |
| +        | Addition       |
| -        | Subtraction    |
| *        | Multiplication |
| /        | Division       |
| ^        | Exponent       |
| Mod      | Remainder      |

Example:
`Set total = price * quantity`
`Set remainder = number MOD 2`

---
## Relational Operators

| Operator | Function                 |
| -------- | ------------------------ |
| ==       | Equal to                 |
| <>       | Not equal to             |
| >        | Greater than             |
| <        | Less than                |
| >=       | Greater than or equal to |
| <=       | Less than or equal to    |

Example: `If score >= 90 Then`

---
## Logical Operators

| Operator | Function             |
| -------- | -------------------- |
| AND      | Both conditions true |
| OR       | Atleast one is true  |
| NOT      | Reverses condition   |

Example: `If age >= 18 AND citizen = true Then`

---
## If Statements

### Basic If

```
If condition Then
	statements
End If
```

### If Else

```
If condition Then
	statements
Else
	statements
End If
```

### If Else If

```
If score >= 90 Then
	Display "A"
Else If score >= 80 Then
	Display "B"
Else
	Display "C or lower"
End If
```

### Nested If

```
If age >= 18 Then
	If citizen = true Then
		Display "Eligible"
	End If
End If
```

---
## Loops

### While Loop (Pre-Test)

```
While condition
	statements
End While
```

Example:
```
Set count = 0
While count < 5
	Display count
	Set count = count + 1
End While
```

### Do-While Loop (Post-Test)

```
Do
	statements
While condition
```

Example:
```
Do
	Input number
While number < 0
```

### For Loop (Count-Controlled)

```
For variable = start To end
	statements
End For
```

Example: 
```
For count = 1 To 10
	Display count
End For
```

With step:
```
For count = 10 To 1 Step -1
	Display count
End For
```

### Sentinel Loop

```
Set number = -1
While number <> 0
Input number
End While
```

### Accumulator Pattern

```
Set total = 0
For count = 1 To 5
	Input number
	Set total = total + number
End For
```

### Counter Pattern

```
Set count = 0
While count < 10
	Set count = count + 1
End While
```

---
## Boolean Values

`true`
`false`

Example:
`Declare Boolean isPassing`
`Set isPassing = score >= 60`

---
## Modules

```
Module name(datatype parameters)
	statements
End Module
```

Example:
``` 
Module main()
	Call displayHello("Comp-126")
End Module

Module displayHello(String name)
	Display "Hello ", name 
End Module
```

Passing by Reference:
```
Module name(Ref variable)
	statements
End Module
```
Example:
```
Module main()
	Declare Real radius, area
	Display "Enter a radius: "
	Input radius
	Call calculateArea(radius, area)
	Display "Area is: ", area
End Module

Module calculateArea(Real r, Ref a)
	Set a = r * r * 3.14
End Module
```

---
## User Defined Functions

```
Function ReturnType name(parameters)
    statements
    Return value
End Function
```

Example:
```
Function Integer addNumbers(Integer a, Integer b)
    Declare Integer result
    Set result = a + b
    Return result
End Function
```

Calling a Function:
```
Declare Integer sum
Set sum = addNumbers(5, 3)
Display "Sum is ", sum
```

---
## Library Functions

Math Functions
```
abs(x)
round(x)
pow(x,y)
sqrt(x)
random(x,y)    // inclusive of x and y
toInteger(x)
toReal(x)
```

String Functions
```
length(s)
toUpper(s)
toLower(s)
substring(s,b,e)    // returns part of string from index b to e
contains(s1,s2)
indexOf(s, sub)     // position of substring
concat(s1, s2)      // joins strings
```

---
## Basic Program Structure

Declare variables

Input data

Process data

Display results

Example: 
```
Declare Real average
Declare Real total
Declare Integer count

Set total = 0

For count = 1 To 3
Input number
Set total = total + number
End For

Set average = total / 3

Display "Average is", average
```
