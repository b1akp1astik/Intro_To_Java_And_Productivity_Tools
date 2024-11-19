---
title: "Lab 1 - Spring 2023"
author: "Harley Gribble (49089358)"
output: html_document
---

# Part 1: Syntax Errors

When attempting to compile `FirstProgram.java`, I received the following error message:

```shell
PS C:\Users\13045\cs1341> javac FirstProgram.java
FirstProgram.java:7: error: ';' expected
  Scanner input = new Scanner(System.in)
                                    ^
1 error
PS C:\Users\13045\cs1341>
```

This error message indicates that a semicolon was missing in the line where the `Scanner` object was declared. It was expecting a `;` after `new Scanner(System.in)`.

## Corrected Code

Here is the corrected version of the code, with the semicolon added:

```java
import java.util.Scanner;

public class FirstProgram {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);  // Missing semicolon added here

        System.out.println("This is my first Java Program!");
        System.out.print("What is your name? ");
        String name = input.next();

        System.out.printf("Hello %s, welcome to CSE 1341 at SMU! \n", name);

        System.out.println("I am pretty intelligent. I can count the numbers from 1 to 50 and find their sum!");

        int total = 0;
        for (int i = 1; i <= 50; i++) {
            System.out.print(i + " ");
            total = total + i;
        }
        System.out.printf("\nThe Sum is %d. \n", total);
    }
}
```

## Program Explanation

### Overview
This Java program accomplishes several tasks:
1. **User Interaction**:
   - The program begins by greeting the user and asking for their name.
   - It then uses the user's input to print a personalized greeting.

2. **Counting and Summing Numbers**:
   - The program counts numbers from **1 to 50**.
   - It calculates and displays the **sum of numbers from 1 to 50**.

### Key Features
- **Scanner for User Input**: 
  - The program uses `Scanner input = new Scanner(System.in);` to get input from the user.
- **Loops**:
  - A `for` loop is used to count numbers from 1 to 50 and calculate the total sum.

### Output Example

Below is an example of the expected output:

```
This is my first Java Program!
What is your name? Harley
Hello Harley, welcome to CSE 1341 at SMU!
I am pretty intelligent. I can count the numbers from 1 to 50 and find their sum!
1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 
The Sum is 1275.
```

## Summary

In this lab, I:
- Identified a **syntax error** involving a missing semicolon in the `Scanner` declaration.
- Corrected the error and successfully compiled and ran the Java program.
- Practiced using **Java loops** to count and sum numbers.
- Gained experience with **user input** using the `Scanner` class.

The corrected program provides a personalized user interaction and performs basic arithmetic, demonstrating foundational skills in Java.
