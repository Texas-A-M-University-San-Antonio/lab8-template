# Programming Fundamentals I - Fall 2025

## Lab Assignment #7: City Sorter

*Due at 11:59 pm the night before the next lab session*

---

## Purpose

A delivery company is developing its own address catalog. Part of this application allows users to select locations to deliver packages. To do this efficiently, the catalog must be sorted. You will begin writing a simple algorithm to sort three cities by name. This lab focuses on the following concepts:

• Comparing Strings using methods from the String class

• Using logical operators to build more complex boolean expressions

---

## In-Class Lesson

To understand the basics of this sorting algorithm, write a program that accepts **two cities** from the user and sorts those two cities in alphabetical order. Use the `compareTo` method from the String class to make a comparison between the cities.

The `compareTo` method returns a number indicating the difference in the Unicode values of the differing characters. Make sure this number is compared to another number that can be used to determine which city comes before the other alphabetically.

**Practice Exercise:** Write a simple program that:
1. Prompts the user to enter two city names
2. Uses `compareToIgnoreCase()` to compare them
3. Prints the cities in alphabetical order using an if-else statement

This simpler two-city comparison prepares you for the main lab assignment where you'll sort three cities.

---

## Task

Create a project called `CitySorter_FirstName_LastName` or `Lab7_FirstName_LastName`. Remember to include comments summarizing the program.

### Requirements

1. **Declare a Scanner** that accepts input from the keyboard.

2. **Declare the following three variables** in your program:

   • Three variables of type `String` that will hold three different cities the user enters

   *Note: You may also consider three variables of type boolean to hold comparisons between the cities.*

3. **Prompt the user three times** to enter each of the three cities. Use the appropriate method of the Scanner class to assign each of the user's inputs to the appropriate String variable.

4. **Determine the alphabetical order** of the cities using comparisons. The order of the cities will depend on the order of the statements to print those cities to the console. To determine the order to print the cities in, you will need to compare the cities using the appropriate method of the String class. 

   **Assume that case does not matter** and that the user enters three different cities. You must do **comparisons between all pairs of cities** to determine the correct order.

   For example, to determine if the last city that the user enters comes first alphabetically, compare this city to the other two cities. If the last city entered by the user does come first alphabetically, print that city and then compare the remaining two cities. Whichever comes second alphabetically is printed next, and then whichever comes last alphabetically is printed last.


## Implementation Notes

- Use the `compareToIgnoreCase()` method or convert strings to the same case before comparing to ensure case-insensitive comparisons
- When `string1.compareTo(string2)` returns a negative number, `string1` comes before `string2` alphabetically
- When `string1.compareTo(string2)` returns a positive number, `string2` comes before `string1` alphabetically
- Use logical operators (&&, ||) to build complex boolean expressions for determining order
- Your program must handle all six possible orderings of three cities

---

## Running Your Program

### Method 1: Using the Terminal
1. Open the terminal in your codespace (Terminal → New Terminal)
2. Compile your program:
   ```bash
   javac Lab7_YourFirstName_YourLastName.java
   ```
3. Run your program:
   ```bash
   java Lab7_YourFirstName_YourLastName
   ```

Replace `Lab7_YourFirstName_YourLastName.java` with your actual file name. If you are running the in-class exercise, use the corresponding file name instead.

---

## Example Program Flow

```
Enter the first city: Dallas
Enter the second city: Austin
Enter the third city: Houston

Cities in alphabetical order:
Austin
Dallas
Houston
```

---

## Grading Criteria

- **Comment summarizing the program** (5 points)
- **Importing and declaring the Scanner class** (2 points)
- **Requests for the user's input** (9 points total)
- **Properly comparing and printing the three Strings in alphabetical order** (14 points for each of the six possible initial orderings provided by the user = 84 points total)

**Total: 100 points**

---

💡 **Fun Tip:** Consider taking a screenshot of your terminal output after running your program with different city combinations! This helps you verify that all six possible orderings work correctly.

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

**Excellent work!** You've reached Lab 7, and this assignment introduces you to string comparison and sorting algorithms. Working with the `compareTo` method and logical operators will help you understand how computers sort text data. This is a fundamental skill that applies to databases, search engines, and countless other applications. Remember to test your program with different city orderings to ensure it handles all cases correctly. Breaking down the problem into smaller comparisons and using logical thinking will lead you to success!

**Important:** Focus on completing the lab assignment. Do NOT edit or tamper with any test files, markdown files, or class files if they appear in your repository.