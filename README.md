# Day-44-Pascal-Triangle

Day 44/100 - Python Program To Print Pascal Triangle

# Print Pascal's Triangle

A program to generate and visually display Pascal's Triangle up to a user-defined number of rows using dynamic list generation.

## 📝 Description

This program calculates and prints **Pascal's Triangle**, a famous mathematical triangular array where the top row is 1, and each number in the subsequent rows is the sum of the two numbers directly above it.

The script uses a **dynamic programming** approach. It initializes a 2D list called `triangle` starting with the base case `[[1]]`. A `for` loop generates each new row by looking at the `previous_row`. It automatically starts the new row with a `1`, iterates through the previous row to add adjacent elements (`previous_row[j - 1] + previous_row[j]`), and ends the row with another `1`. After all rows are generated and stored, a second loop formats the output, adding dynamically calculated leading spaces (`" " * (n - len(row))`) to visually shape the numbers into a pyramid.

---

## 🎯 Problem Statement

### Input:

* **Input 1:** A single integer representing the total number of rows (`rows`) to generate for the triangle.

### Output:

* A visual representation of Pascal's Triangle, printed row by row, with appropriate leading spaces to create a triangular shape.

### Rules:

1. The program must accept an integer input from the user.
2. Initialize the master list with the first row: `triangle = [[1]]`.
3. Use a loop to iterate from 1 up to `n - 1`.
4. Inside the loop, construct the current row by summing the adjacent pair of elements from the previously generated row.
5. Append each newly generated row to the master `triangle` list.
6. Print each row using string formatting to join the numbers and apply left-padding spaces based on the row's length to simulate a centered triangle.

---

## 💡 Examples

### Example 1 (Standard 5 Rows)

**Input:**

```
5


```

**Output:**

```
     1
    11
   121
  1331
 14641


```

**Explanation:** The program calculates the rows: `[1]`, `[1, 1]`, `[1, 2, 1]`, `[1, 3, 3, 1]`, and `[1, 4, 6, 4, 1]`. It then prints them joined together as strings, adding decreasing amounts of blank spaces on the left to form the pyramid.

### Example 2 (Smaller Triangle)

**Input:**

```
3


```

**Output:**

```
   1
  11
 121


```

**Explanation:** The program generates the first 3 rows. The first row has 2 spaces, the second has 1 space, and the third has 0 spaces.

### Example 3 (Single Row Base Case)

**Input:**

```
1


```

**Output:**

```
 1


```

**Explanation:** The user requests only 1 row. The main calculation loop `range(1, 1)` is bypassed entirely. The program prints the initial base case `[1]` with zero leading spaces.

---

## 🚀 How to Use

1. **Clone this repository** (or save the script)

```bash
git clone https://github.com/adiaryaz/Day-44-Pascal-Triangle.git
cd pascal-triangle


```

2. **Run the program**:

```bash
python main.py


```

Enter the desired number of rows when prompted to see the corresponding Pascal's Triangle generated in the console.
