# Chapter 2: Intro to Coding
[Back to Introduction](https://github.com/jawolfe97/How_To_Write_Mediorcre_Lab_Code/tree/main)

### Topics
- [Disclaimer](#disclaimer)
- [What is code?](#what-is-code)
- [Hello World](#hello-world)
- [Data Types](#data-types)
- [Functions](#write-code)
- [Data Structures](#data-structures)
- [Libraries](#libraries)

## Disclaimer
Hi, to all of the Comp Sci people reading this: don't. This is not a course or an expert explanation, this is a quick and dirty explanation of the improtant stuff for using the programs described at the beginning. You're not going to like this and probably have many complaints. This is not a professional way to show anyone anything or help anyone acutally code anything effective. This is solely a crash course in how to search the important terms for scientific coding. My goal here is to set up someone to convince themselves that they have set up the environment for running someone else's code and be able to search the keywords to troubleshoot their own. I won't be explaining the difference between recursion and iteration. I don't understand it myself and haven't needed it to get this far.

[Back to TOC](#topics)

## What is Code?
Code is a list of instructions. There's a misconception that coding is all math -math can certainly help sometimes. A piece of code is the minimum list of instructions needed to get a computer to achieve a task. Thats why a coding diagram looks like this: 

<p><a href="https://commons.wikimedia.org/wiki/File:LampFlowchart.svg#/media/File:LampFlowchart.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/9/91/LampFlowchart.svg" alt="LampFlowchart.svg" height="442" width="324"></a><br>By svg by <a href="//commons.wikimedia.org/wiki/User:Booyabazooka" class="mw-redirect" title="User:Booyabazooka">Booyabazooka</a>original png by <a href="https://en.wikipedia.org/wiki/User:Wapcaplet" class="extiw" title="w:User:Wapcaplet">Wapcaplet</a> - vector version of <a href="//commons.wikimedia.org/wiki/File:LampFlowchart.png" title="File:LampFlowchart.png">Image:LampFlowchart.png</a>, <a href="http://creativecommons.org/licenses/by-sa/3.0/" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=714537">Link</a></p>

and not like this: 

<p><a href="https://commons.wikimedia.org/wiki/File:Algebraic_equation_notation.svg#/media/File:Algebraic_equation_notation.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/b/be/Algebraic_equation_notation.svg" alt="Algebraic equation notation.svg" height="516" width="883"></a><br>By <a href="https://en.wikipedia.org/wiki/User:Iantresman" class="extiw" title="wikipedia:User:Iantresman">Iantresman</a> at <a href="https://en.wikipedia.org/wiki/" class="extiw" title="wikipedia:">English Wikipedia</a>, <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=25604857">Link</a></p>

If you were a bit math-hesitant like I was growing up, great! The computer will do it for you now. As a mater of fact, it can perform mathematical calculations at speeds unthinkable to the human brain. Beat the calculator? Only when a person is typing in the numbers. 

[Back to TOC](#topics)

## Hello World
As is tradition, I will now give your first piece of code. This is typically only a line long. It's asking the computer to say "Hello World" back to you. [It's a fun piece of comp sci history you get to be a part of!](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program)

## 🌍 Hello World in 4 Languages
Google Sheets
```excel
="Hello, World!"
```
RStudio
```R
print("Hello, World!")
```
Python
```python
print("Hello, World!")
```
C++
```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

As you can see, there's always more than just typing in the phrase "Hello, World!." The text around the words is the code, our instructions to tell the computer to "Say the following:" What I find particularly striking is how much we can actually learn from the juxtaposition of the 4. First, as you are well aware, Google Sheets was built for visualizing spreadsheets and doing calculations. As such, it starts with an "=" and the fact that we're working with text and not numbers has to be denoted. Second, both Python and RStudio are so-called "Interpretable Languages." You can tell the computer to print out a word and the function that does it is "print." Excellent. This is intuitive. C++ wasn't designed to be intuitive or user-friendly. It was designed for speed. We talked about this before, but this is the key to picking your programming language. It has to be familiar to you and the code user to make sure your instructions are correct, but there may be lists of instructions that are so long and complex that making the computer translate out the "print" function back into computer speak and binary will preclude your ability to complete the list in a reasonable amount of time. 
[Back to TOC](#topics)

## Data Types

I didn't tell you this, but the languages here operate on "Objects." An object can be anything, a date, a number, a word, etc. Because programming languages need to be versatile, we need to be specific about what our objects are. The answer from a computer to "Fish" + "Fish" isn't automatically "Two Fish." Computers don't understand context, they only understand very specific directions written in the correct language. As such 1 + 1 = 2 if we abstract away the unit "Fish" and define each fish as a number. 

This is intuitive, but it differs a little betwen our 4 languages. Here is the table:
## 🧮 Data Type Comparison: Google Sheets, R, Python, and C++

| Data Type           | Google Sheets        | R (RStudio)           | Python                    | C++                        | Shared?       |
|---------------------|----------------------|------------------------|----------------------------|-----------------------------|---------------|
| **Integer**         | `Number` (no decimal) | `integer` (`int`)     | `int`                     | `int`                       | ✅ Yes        |
| **Float / Decimal** | `Number` (decimal)    | `numeric` (default)    | `float`, `double`         | `float`, `double`           | ✅ Yes        |
| **String / Text**   | `Text`                | `character`            | `str`                     | `std::string`, `char[]`     | ✅ Yes        |
| **Boolean**         | `TRUE` / `FALSE`      | `logical`              | `bool` (`True`, `False`)  | `bool` (`true`, `false`)    | ✅ Yes        |
| **Date / Time**     | `Date`, `DateTime`    | `Date`, `POSIXct`      | `datetime.datetime`       | `std::chrono` or libraries  | ✅ Yes        |
| **List / Array**    | `Array` (via ranges)  | `vector`, `list`       | `list`, `tuple`           | `array`, `vector`           | ✅ Yes        |
| **Null / Missing**  | `""`, `#N/A`          | `NA`, `NULL`           | `None`, `nan`             | `nullptr`, `NULL`           | ⚠️ Partially |
| **Object / Struct** | ❌ Not supported       | `list`, `data.frame`   | `class`, `dict`           | `struct`, `class`           | ❌ No         |
| **Dictionary / Map**| ❌ Not supported       | `named list`, `env`    | `dict`                    | `map`, `unordered_map`      | ⚠️ Partially |

---

### 🔍 Notes

- **Google Sheets** uses cell formatting to infer types — no strict declarations.
- **R** treats all numbers as `numeric` by default; use `as.integer()` for integers.
- **Python** is dynamically typed, with implicit conversions and rich built-ins.
- **C++** is statically typed — all types must be declared.

That was scary, but stay with me. Most of those are a little confusing. Lets give a practical definition of each:
Integer -  A whole number
Float/Decimal - A number, like a normal decimal number from math class. You can define 3 as 3 or 3.0 and perform numeric calculations. Be careful though, if you don't specify which one then the programming language will choose a default. This can mess up code and is a common source of error.
String/Text -  So it explains itself. It's words, and single letters. But keep in mind that we can have a string "3" 3 the integer, 3.0 the float, and "3" the string could be confused if not well-defined by the computer and prevent the computer from running your instructions. 
Date/Time -  You know, don't worry about it.
Null - Okay, so what if there was no number in the object you defined? Is that 0? No, so we need a place holder for an "empty" object.
Boolean - The result of a logical operation. Why was 6 afraid of 7? Because 7<8<9. We can use code evaluate the mathematical validity of that joke. If 7 < 8 and 8 < 9 then the statement should return the value TRUE. If the joke isn't funny, then the logical operation would return FALSE. There are many logical operators we could test:

## 🔁 Boolean Logic Operators in Google Sheets, R, Python, and C++

| Operation            | Google Sheets       | R / RStudio                    | Python              | C++                    | Shared?       |
|----------------------|---------------------|--------------------------------|---------------------|------------------------|---------------|
| **AND**              | `AND(x, y)`         | `x & y` (vector), `x && y` (scalar) | `x and y`          | `x && y`               | ✅ Yes        |
| **OR**               | `OR(x, y)`          | `x | y`, `x || y`              | `x or y`            | `x || y`               | ✅ Yes        |
| **NOT**              | `NOT(x)`            | `!x`                           | `not x`             | `!x`                   | ✅ Yes        |
| **XOR**              | `XOR(x, y)`         | `xor(x, y)`                    | `x != y` or `x ^ y` (bitwise) | `x ^ y` (bitwise)     | ⚠️ Partial    |
| **Equal (`==`)**     | `x = y` or `x = x`  | `x == y`                       | `x == y`            | `x == y`               | ✅ Yes        |
| **Not Equal**        | `x <> y`            | `x != y`                       | `x != y`            | `x != y`               | ✅ Yes        |
| **Greater Than**     | `x > y`             | `x > y`                        | `x > y`             | `x > y`                | ✅ Yes        |
| **Less Than**        | `x < y`             | `x < y`                        | `x < y`             | `x < y`                | ✅ Yes        |
| **Greater or Equal** | `x >= y`            | `x >= y`                       | `x >= y`            | `x >= y`               | ✅ Yes        |
| **Less or Equal**    | `x <= y`            | `x <= y`                       | `x <= y`            | `x <= y`               | ✅ Yes        |

---

### 🧠 Notes

- **Google Sheets** uses logic **functions** like `AND()`, `OR()`, and `XOR()`, not infix operators. It uses `<>` for "not equal".
- **R** distinguishes between **element-wise** (`&`, `|`) and **scalar** (`&&`, `||`) logical operators.
- **Python** uses **keywords** (`and`, `or`, `not`) and bitwise XOR (`^`) for booleans.
- **C++** uses standard logical symbols (`&&`, `||`, `!`) and supports bitwise XOR (`^`) for `bool` and numeric types.

Below is an example of some R Code that incorporates Boolean Logic to the logic behind that joke:

RStudio
```R
#Define Objects as Integers
a = 7
b = 8
c = 9
#Test Joke Logic
if(a < b & b < c){
print("That was a funny joke")
}
```

For the rest of this, well only be talking about R and Python because there's overlap there. 



[Back to TOC](#topics)

## Functions
Functions perform actions on objects. It's intuitive from math class. Here is a non-exhaustive list of functions that you can string together in both languages.


[Back to TOC](#topics)

##Data Structures

[Back to TOC](#topics)
