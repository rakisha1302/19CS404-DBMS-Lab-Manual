# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers
```
DECLARE
    a NUMBER := 95;
    b NUMBER := 90;
BEGIN
    IF a > b THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || a);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || b);
    END IF;
END;
```

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.
  
<img width="911" height="830" alt="image" src="https://github.com/user-attachments/assets/b75b2fd4-7ac7-421d-a88d-57da85eda890" />

**Expected Output:**  
Greater number is: 95

---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

```
DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    sum NUMBER := 0;
BEGIN
    WHILE i <= n LOOP
        sum := sum + i;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n ||
    ' natural numbers is: ' || sum);
END;

```

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55

<img width="722" height="842" alt="image" src="https://github.com/user-attachments/assets/ee41dfba-1a31-4610-a1f6-29e2f26ab3b8" />

---

## 3. Write a PL/SQL program to generate Fibonacci series

```
DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
    i NUMBER := 1;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci sequence:');

    WHILE i <= n LOOP
        DBMS_OUTPUT.PUT(a || ' ');

        c := a + b;
        a := b;
        b := c;

        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.NEW_LINE;
END;

```

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

<img width="727" height="907" alt="image" src="https://github.com/user-attachments/assets/4c3796c4-641d-4e9f-8317-fc6a22885d40" />

---

## 4. Write a PL/SQL Program to display the number in Reverse Order

```
DECLARE
    n NUMBER := 1535;
    rem NUMBER;
    rev NUMBER := 0;
BEGIN
    WHILE n > 0 LOOP
        rem := MOD(n, 10);
        rev := rev * 10 + rem;
        n := TRUNC(n / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reversed number is: ' || rev);
END;

```
### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

<img width="897" height="882" alt="image" src="https://github.com/user-attachments/assets/11577884-082d-4e39-976c-538248fb44d6" />

---

## 5. Write a PL/SQL program to find the largest of three numbers
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    IF a > b AND a > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || a);

    ELSIF b > a AND b > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || b);

    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || c);
    END IF;
END;

```
### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.
  
<img width="712" height="722" alt="image" src="https://github.com/user-attachments/assets/cf5c033a-ee5b-4559-b39a-10c668314866" />

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
