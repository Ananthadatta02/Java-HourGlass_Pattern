
s
# Hourglass Pattern in Java

## Overview
This Java program generates an **hourglass (sandglass) star pattern** based on the user’s input. The pattern consists of an inverted pyramid followed by an upright pyramid, creating a symmetrical hourglass shape.

## Code Explanation

### 1. Scanner Class
The **Scanner** class in Java is used to take user input. In this program:
```java
Scanner s = new Scanner(System.in);
```
- `Scanner s` creates an instance of the Scanner class.
- `new Scanner(System.in)` allows us to read input from the console.
- `int n = s.nextInt();` reads an integer value entered by the user.

### 2. Variables
- `n`: Stores the size of the pattern (number of rows in the upper half).
- `i, j`: Loop control variables for iterating through rows and columns.

### 3. Outer For Loop (Upper Half - Inverted Pyramid)
```java
for(int i=0; i<=n; i++)
```
- Controls the number of rows in the upper half.
- Runs from `0` to `n`, generating each row.

#### Inner Loops (Upper Half)
1. **Leading Spaces**
   ```java
   for(int j=1; j<=i; j++)
   ```
   - Prints spaces to shift stars to the right, forming the upper half of the hourglass.

2. **Printing Stars**
   ```java
   for(int j=i; j<n; j++)
   ```
   - Prints `*` characters to form the left side of the pattern.
   ```java
   for(int j=i; j<=n; j++)
   ```
   - Prints `*` characters to form the right side, completing the row.

3. **New Line Statement**
   ```java
   System.out.println();
   ```
   - Moves to the next line after printing one row.

### 4. Outer For Loop (Lower Half - Upright Pyramid)
```java
for(int i=2; i<=n+1; i++)
```
- Starts from `2` to `n+1`, forming the lower half.

#### Inner Loops (Lower Half)
1. **Leading Spaces**
   ```java
   for(int j=i; j<=n; j++)
   ```
   - Prints spaces to align the lower half.

2. **Printing Stars**
   ```java
   for(int j=1; j<=i; j++)
   ```
   - Prints the first half of `*`.
   ```java
   for(int j=1; j<i; j++)
   ```
   - Prints the second half of `*`, completing the row.

3. **New Line Statement**
   ```java
   System.out.println();
   ```
   - Moves to the next row.

## Example Output
For `n = 5`, the output is:
```
***********
 *********
  *******
   *****
    ***
     *
    ***
   *****
  *******
 *********
***********
```

## Summary
- **Takes user input** using `Scanner`.
- **Uses nested loops** to print spaces and stars.
- **Creates an hourglass pattern** by printing an inverted pyramid followed by an upright pyramid.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-HourGlass_Pattern.git
```
