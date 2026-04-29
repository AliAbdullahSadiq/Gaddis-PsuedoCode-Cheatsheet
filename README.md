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

```clike
If condition Then
	statements
End If
```

### If Else

```clike
If condition Then
	statements
Else
	statements
End If
```

### If Else If

```clike
If score >= 90 Then
	Display "A"
Else If score >= 80 Then
	Display "B"
Else
	Display "C or lower"
End If
```

### Nested If

```clike
If age >= 18 Then
	If citizen = true Then
		Display "Eligible"
	End If
End If
```

---
## Loops

### While Loop (Pre-Test)

```clike
While condition
	statements
End While
```

Example:
```clike
Set count = 0
While count < 5
	Display count
	Set count = count + 1
End While
```

### Do-While Loop (Post-Test)

```clike
Do
	statements
While condition
```

Example:
```clike
Do
	Input number
While number < 0
```

### For Loop (Count-Controlled)

```clike
For variable = start To end
	statements
End For
```

Example: 
```clike
For count = 1 To 10
	Display count
End For
```

With step:
```clike
For count = 10 To 1 Step -1
	Display count
End For
```

### Sentinel Loop

```clike
Set number = -1
While number <> 0
Input number
End While
```

### Accumulator Pattern

```clike
Set total = 0
For count = 1 To 5
	Input number
	Set total = total + number
End For
```

### Counter Pattern

```clike
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

```clike
Module name(datatype parameters)
	statements
End Module
```

Example:
``` clike
Module main()
	Call displayHello("Comp-126")
End Module

Module displayHello(String name)
	Display "Hello ", name 
End Module
```

Passing by Reference:
```clike
Module name(Ref variable)
	statements
End Module
```
Example:
```clike
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

```clike
Function ReturnType name(parameters)
    statements
    Return value
End Function
```

Example:
```clike
Function Integer addNumbers(Integer a, Integer b)
    Declare Integer result
    Set result = a + b
    Return result
End Function
```

Calling a Function:
```clike
Declare Integer sum
Set sum = addNumbers(5, 3)
Display "Sum is ", sum
```

---
## Data Validation

Range Check
```clike
If age >= 0 AND age <= 120 Then
    Display "Valid age"
Else
    Display "Invalid age"
End If
```

Type Check
```clike
Input value
If isInteger(value) Then
    Display "Valid integer"
Else
    Display "Invalid input"
End If
```

Presence Check
```clike
Input name
If name <> "" Then
    Display "Valid name"
Else
    Display "Name cannot be empty"
End If
```

Sentinel Validation
```clike
Set number = -1
While number <> 0
    Input number
    If number <> 0 Then
        Display "Processing ", number
    End If
End While
```

Post-Test Loop Validation (Re-prompt)
(will not give an error message)
```clike
Do
    Display "Enter a positive number: "
    Input number
While number <= 0
```

---
## Library Functions

Math Functions
```clike
abs(x)
round(x)
pow(x,y)
sqrt(x)
random(x,y)    // inclusive of x and y
toInteger(x)
toReal(x)
```

String Functions
```clike
length(s)
toUpper(s)
toLower(s)
substring(s,b,e)    // returns part of string from index b to e
contains(s1,s2)
indexOf(s, sub)     // position of substring
concat(s1, s2)      // joins strings
```
---
## Arrays

Declaration
```Declare DataType name[size]```

Example
```clike
Declare Real temps[5] = 12.4, 18.7, 21.3, 24.8, 16.9
Set temps[0] = 12.8
Display temps[3]
```

Printing array
```clike
Declare Integer values[4] = 12. 68, 34, 38
Declare Intger i = 0

For i = 0 To 3 // 0 To arrayLength - 1
	Display values[i]
End For
```

Passing Arrays to Functions
```clike
Declare Integer values[4] = 12. 68, 34, 38
Declare SIZE = 4

Declare Real avg = CalcAverage(values, SIZE)
// DO NOT USE [] BRACKETS WHEN PASSING ARRAY TO FUNCTION

Functon Real CalcAverage(vals[], SIZE)
	// Return Average
End Function
```

---
## Finding min/max

```clike
Function Integer findLargest(Integer list[], Integer size)
	Declare largest, i
	Set largest = list[i]
	
	For i = 1 To (size-1)
		If list[i] > largest Then    // for smallest: use <
			Set largest = list[i]
		End If
	End For
	
	Return largest
End Function
```

---
## Searching
### Linear Search (Sequential Search)

```clike
Function Integer linearSearch(Integer list[], Integer size, Integer target)  
    Declare Integer i  
      
    For i = 0 To size - 1  
        If list[i] == target Then  
            Return i    // position where found  
        End If  
    End For  
      
    Return -1   // not found  
End Function
```

If you need to search in main (can't use Functions):
```clike
Declare Boolean found = false

While i < size AND NOT found 
	If values[i] == target Then  
		Set found = true  
	Else  
		Set i = i + 1  
	End If  
End While  
  
If found == true Then  
	Display "Found at index ", i  
Else  
	Display "Not found"  
End If
```

### Binary Search

**IMPORTANT:** Array must be sorted.

```clike
Function Integer binarySearch(Integer list[], Integer size, Integer target)  
    Declare Integer low, high, mid  
      
    Set low = 0  
    Set high = size - 1  
      
    While low <= high  
        Set mid = (low + high) / 2  
          
        If list[mid] == target Then  
            Return mid  
        Else If list[mid] < target Then  
            Set low = mid + 1  
        Else  
            Set high = mid - 1  
        End If  
    End While  
      
    Return -1  
End Function
```
---
## Classes

```clike
myCar = new Car

myCar.Color = "white"

myCar.start()
```

Example:
```clike
Class Employee
	// attributes (fields)
	Private Integer id    // notice no Declare
	Private String name
	Private Real payRate
	
	// methods
	// constructor
	Public Module Employee(Integer newId, String newName, Real NewPayRate)
		Set id = newId
		Set name = newName
		Set payRate = newPayRate
	End Module
	
	// Mutators (Setters)
	Public Module setId(Integer newId)
		Set id = newId
	End Module
	Public Module setName(String newName)
		Set name = newName
	End Module
	Public Module setPayRate(Real newPayRate)
		Set payRate = newPayRate
	End Module
	
	// Accessors (Getters)
	Public Function getId()
		return id
	End Function
	Public Function getName()
		return name
	End Function
	Public Function getPayRate()
		return payRate
	End Function
	
	// Other methods
	Public Module giveRaise(Real raise)
		payrate = payRate + raise
	End Module
	
End Class

Module main()
	Set emp1 = new Employee(10, "Sally", 20.35)
	
	Display "Id: ", emp1.getId()
	Display "Name: ", emp1getName()
	Display "Pay Rate: ", emp1.getPayRate()
End Module
```

UML Diagram:

| Employee                                                                                                                                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| -id:int<br>-name:string<br>-payRate:Real                                                                                                                                                                                                                       |
| +Employee(id:int, name:string, payRate:real)<br><br>+setId(newId:int):void  <br>+setName(newName:string):void  <br>+setPayRate(newPayRate:real):void  <br>  <br>+getId():int  <br>+getName():string  <br>+getPayRate():real<br><br>+giveRaise(raise:real):void |
`-` means Private
`+` means Public

---
## Basic Program Structure

Declare variables

Input data

Process data

Display results

Example: 
```clike
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
