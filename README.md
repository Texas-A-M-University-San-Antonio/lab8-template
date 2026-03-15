# Lab 8: Loops and Processor Speed Analysis
**Due Date:** @ 11:59 the night *before* next lab

**Submission:** Push to GitHub repository + Submit link to Blackboard

---

## 📋 Overview
This lab introduces **sentinel-controlled loops** and applies them to a real-world computing scenario: analyzing processor benchmark performance. You'll learn how to use a `while` loop to process an unknown number of inputs, accumulate data, and calculate the geometric mean—a statistical measure commonly used in computer performance analysis.

**Learning Objectives:**
- Use sentinel values to control loop termination
- Implement a `while` loop to process variable amounts of data
- Accumulate data using multiplication and counting
- Apply `Math.pow()` to calculate the nth root
- Format output using `printf()` with decimal precision
- Avoid common pitfalls like initializing accumulators incorrectly
- Understand and prevent integer division errors
- Apply loops to solve real-world computational problems

---

## 🚀 Getting Started with GitHub Codespaces

### Initial Setup
1. **Accept the assignment** via the GitHub Classroom link provided
2. **Open your repository** in GitHub Codespaces:
   - Click the green "**Code**" button
   - Select "**Codespaces**" tab
   - Click "**Create codespace on main**"
3. **Wait for the environment to load** (this may take 1-2 minutes on first launch)
4. **Explore your workspace** - On the left side, you'll see the file explorer with:
   - `README.md` (this file)
   - `InClass8_FirstName_LastName.java` - for your in-class activity
   - Other supporting files

**Note:** You will create the `Lab8_FirstName_LastName.java` file yourself. Update all filenames and class headers with your actual first and last name.

---

## 📚 Key Concepts for This Lab

This lab builds on fundamental concepts you've learned in class. You'll need to apply your knowledge of loops, variables, and mathematical operations. **Review your lecture notes, textbook, and class examples** for detailed explanations and syntax.

### Sentinel-Controlled Loops
A **sentinel value** is a special input that signals the program to stop processing. For this lab, you'll use `-1` as the sentinel since processor speeds are always positive.

**Important Pattern:** When using a sentinel-controlled loop, you need to:
1. Read input **before** entering the loop (called a "priming read")
2. Check the condition in the loop header
3. Process the data inside the loop
4. Read the next input **at the end** of the loop body

**Why read input twice?** Review your textbook's section on while loops and sentinel values for the complete pattern.

### Accumulator Variables
Loops often require **accumulator variables** to track running calculations. Consider:
- What starting value makes sense for a variable that will hold a **sum**?
- What starting value makes sense for a variable that will hold a **product**?
- What starting value makes sense for a variable that will **count** items?

**Hint:** Think about the identity element for each operation. What number can you add without changing a value? What number can you multiply without changing a value?

### Geometric Mean Concept
The **geometric mean** differs from the arithmetic average (what you calculate when finding the mean of test scores):
- **Arithmetic mean:** Add all numbers, then divide by the count
- **Geometric mean:** Multiply all numbers, then take the nth root

**Formula:** Geometric Mean = (product)^(1/n)

The geometric mean is commonly used in computer performance analysis because it better represents data that spans different scales.

### Mathematical Operations You'll Need
**Taking Roots:** Remember from math class that the nth root of a number is the same as raising that number to the power of (1/n). For example:
- Square root of x = x^(1/2)
- Cube root of x = x^(1/3)
- nth root of x = x^(1/n)

Java provides `Math.pow(base, exponent)` to raise a base to any power.

**Integer Division Warning:** When dividing integers in Java, the result is truncated. Research how to force floating-point division when needed.

### Formatting Output
The `printf()` method allows you to control decimal precision in your output. You'll need to format your result to exactly two decimal places.

**Research:** Look up the format specifier for floating-point numbers and how to specify decimal places. Your textbook has examples of `printf()` formatting.

---

**Before starting the lab, make sure you understand:**
- How to structure a sentinel-controlled while loop
- The difference between reading input before vs. inside a loop
- How to properly initialize accumulator variables
- How to use `Math.pow()` for exponentiation
- How to avoid integer division
- How to format output with `printf()`

**Refer to:** Your lecture notes, textbook chapters on loops and mathematical operations, and in-class examples.

---

## 📝 Part 1: In-Class Activity (Participation Points)
**File to Work With:** `InClass8_FirstName_LastName.java`

### Task
Write a program that calculates the **average of course grades** using a sentinel-controlled loop. This simpler averaging exercise will prepare you for calculating the geometric mean in the main lab.

The key difference: averaging uses **addition and division**, while geometric mean uses **multiplication and roots**. Both require the same loop pattern!

**Requirements:**
1. **Update** the filename and class name with your actual first and last name
2. **Import** Scanner at the top of your file
3. **Declare and initialize variables** to store:
   - The next grade entered by the user (`int`)
   - The sum of all grades (`int`) - what value should this start at?
   - The count of grades entered (`int`) - what value should this start at?
   - The final average (`double`)
4. **Prompt** the user to enter a grade or -1 to end
5. **Read** the first grade (this is the "priming read" mentioned earlier)
6. **Write a while loop** that continues while the grade is not -1:
   - Add the grade to the sum
   - Increment the count
   - Prompt and read the next grade (this is crucial!)
7. **Calculate** the average after the loop ends
   - **Important:** How do you avoid integer division?
8. **Display** the average formatted to two decimal places
9. **Add detailed comments** explaining:
   - What the program does overall
   - Why your initialization values make sense
   - How the sentinel value controls the loop
   - Why reading input twice is necessary

### Example Output
```
Please enter a grade (-1 to end): 100
Please enter a grade (-1 to end): 64
Please enter a grade (-1 to end): 87
Please enter a grade (-1 to end): -1
The average for the course is 83.67
```

### Testing Your In-Class Program
Test with various scenarios:
- **Multiple grades:** 90, 85, 92, -1 → Average should be 89.00
- **Single grade:** 100, -1 → Average should be 100.00

---

## 🔬 Part 2: Main Lab Assignment

### Background
A computer hardware manufacturer is conducting benchmark tests to analyze processor performance across different CPUs. Rather than using a simple average, they need to calculate the **geometric mean** of processor speeds—a more accurate statistical measure for performance metrics that span different scales.

Your task is to create a program that:
- Accepts an unknown number of processor speed measurements
- Calculates the geometric mean of all measurements
- Displays the result with professional formatting

### Task
Create a file named `Lab8_FirstName_LastName.java` (replace with your actual name). Remember to include comprehensive comments summarizing the program's purpose and approach.

### Requirements

1. **Import Scanner and set up your class**
   - Import the Scanner class at the top
   - Create your class with the name matching your filename
   - Include a detailed header comment with your name, date, and program purpose

2. **Declare and initialize variables**
   
   You will need **four variables**:
   
   - `int nextSpeed` - holds the next processor speed entered by the user
   - `int count` - tracks how many processor speeds have been entered (what starting value?)
   - `int product` - stores the running product of all speeds (what starting value?)
   - `double geometricMean` - holds the final calculated result
   
   **Think carefully:** Why are the starting values for `count` and `product` different?

3. **Get the first input (priming read)**
   - Prompt the user to enter a processor speed or -1 to finish
   - Read the user's input into `nextSpeed`

4. **Implement the sentinel-controlled while loop**
   
   The loop should continue while `nextSpeed != -1`:
   - Update the product by multiplying it with the new speed
   - Increment the count of data points
   - Prompt and read the next speed (this updates the loop condition!)

5. **Calculate the geometric mean**
   
   After the loop ends, calculate the geometric mean:
   - Remember: geometric mean = (product)^(1/count)
   - Use `Math.pow()` with the appropriate base and exponent
   - **Watch out:** How do you prevent integer division in the exponent?

6. **Display the result**
   
   Use `printf()` to format the output to exactly two decimal places.
   - Research the correct format specifier for floating-point numbers
   - Include a descriptive message with the result

### Example Output
```
Enter a processor speed (-1 to finish): 2400
Enter a processor speed (-1 to finish): 3200
Enter a processor speed (-1 to finish): 2800
Enter a processor speed (-1 to finish): -1
The geometric mean of processor speeds is 2782.83
```

### Verification
You can verify your program is working correctly by calculating by hand:
- Product: 2400 × 3200 × 2800 = 21,504,000,000
- Count: 3
- Geometric Mean: 21,504,000,000^(1/3) ≈ 2782.83

---

## ⚠️ Common Mistakes to Avoid

1. **Incorrect accumulator initialization**
   - Starting a product at 0 will make every calculation result in 0
   - Think about what value doesn't change the result when you multiply by it

2. **Integer division in calculations**
   - When both operands are integers, Java performs integer division
   - Research how to make Java use floating-point division instead
   - This is especially critical when calculating 1/count for the exponent

3. **Forgetting the loop update**
   - If you don't read new input inside the loop, it will run forever
   - Use Ctrl+C in the terminal if your program won't stop

4. **Wrong format specifier in printf()**
   - Different data types require different format specifiers
   - Review your notes on printf() format codes for floating-point numbers

5. **Processing the sentinel value**
   - Make sure your loop stops BEFORE processing -1
   - The sentinel should not be included in your calculations

---

## 🧪 Testing Your Program

Test your lab program thoroughly with these cases:

### Test Case 1: Normal Operation
```
Input: 1000, 2000, 4000, -1
Expected: Geometric mean ≈ 2000.00
```

### Test Case 2: Two Values
```
Input: 3000, 3000, -1
Expected: Geometric mean = 3000.00
```

### Test Case 3: Different Magnitudes
```
Input: 100, 1000, 10000, -1
Expected: Geometric mean = 1000.00
```

### Test Case 4: Single Value
```
Input: 5000, -1
Expected: Geometric mean = 5000.00
```

---

## � Submitting Your Lab

### Using VS Code in Codespaces

**Stage your changes:**
1. Click the **Source Control** icon in the left sidebar (looks like a branching diagram)
2. You'll see your changed files under "Changes"
3. Click the **+** button next to each file to stage it (or click the + next to "Changes" to stage all)

**Commit your changes:**
1. Type a descriptive message in the text box at the top (e.g., "Completed Lab 8")
2. Click the **✓ Commit** button (or press Ctrl+Enter)

**Push to GitHub (SYNC):**
1. Click the **•••** (three dots) menu in the Source Control panel
2. Select **Push** (or click the **Sync Changes** button)
3. Your changes are now on GitHub!

**Submit to Blackboard:**
1. Go to your GitHub repository in a web browser
2. Copy the URL from the address bar
3. Submit this URL to the Lab 8 assignment on Blackboard

### Verification
To verify your submission worked:
- Visit your GitHub repository
- You should see your Java files updated with recent commit timestamps
- Click on your files to ensure the latest code is visible

---

## 🎯 Grading Criteria

**In-Class Activity (Participation):**
- File correctly named with your name
- Program compiles without errors
- Correctly implements sentinel-controlled loop
- Calculates average accurately
- Includes meaningful comments

**Main Lab Assignment:**
- File correctly named with your name
- Program compiles and runs without errors
- Variables correctly declared and initialized
- Sentinel-controlled loop implemented properly
- Geometric mean calculated correctly using `Math.pow()`
- Output formatted to two decimal places
- Code includes comprehensive comments
- Follows good coding style and conventions

---

## 📖 Additional Resources

**Java Documentation:**
- [Math.pow() documentation](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#pow(double,double))
- [Scanner class documentation](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Scanner.html)
- [printf() formatting guide](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/PrintStream.html#printf(java.lang.String,java.lang.Object...))

**Concepts:**
- [Geometric Mean Explained](https://en.wikipedia.org/wiki/Geometric_mean)
- [Sentinel Values in Programming](https://en.wikipedia.org/wiki/Sentinel_value)

---

## ❓ Getting Help

If you encounter issues:
1. **Read error messages carefully** - they often tell you exactly what's wrong
2. **Check your initialization values** - especially for product (should be 1)
3. **Verify your loop structure** - input before loop, input at end of loop
4. **Test with simple numbers** - try 2, 8, -1 (geometric mean should be 4.0)
5. **Ask during lab time** - your instructor and TAs are here to help!

Remember: Everyone struggles with loops at first. With practice, they become second nature!

---

**Happy Coding! 🚀**