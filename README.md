# Programming Fundamentals I - Fall 2025

## Lab Assignment #8: Processor Speed Analysis

*Due at 11:59 pm the night before the next lab session*

---

## Purpose

A computer manufacturer is testing processor speeds using benchmark tests. Part of these tests involves calculating the geometric mean of a set of data points. A geometric mean requires multiplying the numbers together and getting the nth root of those numbers, where n is the amount of numbers. You will write a program that allows the user to enter any amount of data points and calculate the geometric mean of that entire data set. This lab focuses on the following concepts:

• Controlling a loop using a sentinel value

• Displaying formatted outputs using printf

---

## In-Class Lesson

To better understand the flow of this kind of program, consider a similar case: calculating the average of a set of grades. Write a program that will accept any amount of grades and prints the average as output. You will need to keep track of two pieces of information: the sum of the grades and the amount of grades. Use -1 as a sentinel value to finish inputting grades. 

**Practice Exercise:** Write a simple program that:
1. Prompts the user to enter grades (or -1 to end)
2. Uses a while loop to accumulate the sum and count
3. Calculates and prints the average when the user enters -1

The following is an example of the program flow:

```
Please enter a grade (-1 to end): 100
Please enter a grade (-1 to end): 64
Please enter a grade (-1 to end): 87
Please enter a grade (-1 to end): -1
The average for the course is 83.67.
```

This simpler averaging program prepares you for the main lab assignment where you'll calculate the geometric mean of processor speeds.

---

## Task

Create a project called `Processors_FirstName_LastName` or `Lab8_FirstName_LastName`. Remember to include comments summarizing the program.

### Requirements

1. **Declare a Scanner** that accepts input from the keyboard.

2. **Declare the following four variables** in your program:

   • A variable of type `int` that will hold the next processor speed to be included in the set
   
   • A variable of type `int` that will hold the amount of processor speeds (data points)
   
   • A variable of type `int` that will hold the product of all processor speeds
   
   • A variable of type `double` that will hold the final geometric mean of the data set

   **Initialize the variables for the amount and product to appropriate values** given the purpose of this program.

3. **Prompt the user** to enter a processor speed or -1 to end. Use the appropriate method of the Scanner class to assign the user's input to the int variable for the next processor speed.

4. **Write a while loop** that will check if the user's input is not -1. While the input is not -1, do the following:

   • Multiply the product by the next processor speed and assign this result back to the product.
   
   • Increment the amount of processor speeds.
   
   • Prompt the user again to enter a processor speed or -1 to end. Use the appropriate method of the Scanner class to assign the user's input to the int variable for the next processor speed.

5. **After the user has finished entering processor speeds**, calculate the geometric mean using `Math.pow` to get the nth root. Be careful about performing integer division.

6. **Display the geometric mean** to the console formatted to two decimal places.

---

## Implementation Notes

- Initialize the product variable to 1 (since multiplying by 0 would result in 0)
- Initialize the amount variable to 0 (since you start with no data points)
- The geometric mean formula is: (product)^(1/n) where n is the amount of numbers
- Use the appropriate mathematical expression to calculate the nth root, also known as "to the power of 1/n"
- Use `printf` to display the result with two decimal places
- Make sure to convert at least one value to double to avoid integer division

---

## Running Your Program

### Method 1: Using the Terminal
1. Open the terminal in your codespace (Terminal → New Terminal)
2. Compile your program:
   ```bash
   javac Lab8_YourFirstName_YourLastName.java
   ```
3. Run your program:
   ```bash
   java Lab8_YourFirstName_YourLastName
   ```

Replace `Lab8_YourFirstName_YourLastName.java` with your actual file name. If you are running the in-class exercise, use the corresponding file name instead.

---

## Example Program Flow

```
Enter a processor speed (-1 to end): 100
Enter a processor speed (-1 to end): 40
Enter a processor speed (-1 to end): 76
Enter a processor speed (-1 to end): -1
The geometric mean of the processor speeds is 67.24
```

---

## Grading Criteria

- **Comment summarizing the program** (5 points)
- **Importing and declaring the Scanner class** (2 points)
- **Appropriate variable declarations** (15 points total)
- **The first request for the user's input** (3 points)
- **Properly implementing the while loop** (45 points)
- **The final calculation of the geometric mean** (20 points)
- **The output of the program with the geometric mean formatted to two decimal places** (10 points)

**Total: 100 points**

---

💡 **Fun Tip:** Test your program with different sets of processor speeds to verify your geometric mean calculation is correct. You can use an online calculator to check your results! Don't forget to take a screenshot of terminal output and add to your directory on the left <-

---


## Commit Your Changes
### Step 1. Use VS Code's Source Control panel:
   - Click the Source Control icon in the left sidebar
   - Type a commit message describing your changes
   - Click "Commit" then "Sync Changes" to push your code

### Step 2: Verify Submission
After pushing your changes, visit your assignment repository on GitHub Classroom. Confirm that your latest code and commit message appear, and that your files are named correctly. 

### Step 3: Submit to Blackboard Assignment
Once you have verified your submission on GitHub Classroom, copy the URL of your assignment repository and submit this GitHub repository link to Blackboard as confirmation that you are DONE.

**Excellent work!** You've reached Lab 8, and this assignment introduces you to loop control with sentinel values and formatted output. Working with while loops and the `printf` method will help you understand how to process variable amounts of data and display results professionally. The geometric mean is used in many real-world applications like calculating average growth rates, investment returns, and benchmark performance. Remember to test your program with different numbers of processor speeds to ensure your loop and calculations work correctly!

**Important:** Focus on completing the lab assignment. Do NOT edit or tamper with any test files, markdown files, or class files if they appear in your repository.