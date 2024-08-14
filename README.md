# 2.1-Easter

## Java Documentation
[Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

## Java Tutorials
[Variables](https://runestone.academy/ns/books/published/apcsareview/VariableBasics/toctree.html)

[Math Operators](https://runestone.academy/ns/books/published/apcsareview/VariableBasics/operators.html)

## Background:
The naming of variables is very important. The names should be
descriptive and to the point. However, when working with any type of algorithm or formula that may
be presented to you, it is always better to use the variable names used by the client. This reduces
potential confusion that may arise if the client named something “a” and you renamed it “netIncome”.
This becomes quite clear in this assignment because if you try to change the names that are given,
you would have to remember to translate from one variable name to the other.
A convenient algorithm for determining the date of Easter in a given year was devised in 1876 and
first appeared in Butcher’s Ecclesiastical Handbook. This algorithm holds for any year in the Gregorian
calendar, which means years including and after 1583. Subject to minor adaptations, the algorithm is
as follows:
1. Let y be the year (such as 1583 or 2003).
2. Divide y by 19 and call the remainder a. Ignore the quotient.
3. Divide y by 100 and get a quotient b and a remainder c.
4. Divide b by 4 and get a quotient d and a remainder e.
5. Divide b + 8 by 25 and get a quotient f. Ignore the remainder.
6. Divide b - f + 1 by 3 and get a quotient g. Ignore the remainder.
7. Divide 19 * a + b - d - g + 15 by 30 and get a remainder h. Ignore the quotient.
8. Divide c by 4 and get a quotient i and a remainder k.
9. Divide 32 + 2 * e + 2 * i - h - k by 7 and get a remainder r. Ignore the quotient.
10. Divide a + 11 * h + 22 * r by 451 and get a quotient m. Ignore the remainder.
11. Divide h + r - 7 * m + 114 by 31 and get a quotient n and a remainder p.

The value of n gives the month (3 for March and 4 for April) and the value of p + 1 gives the day of
the month. For example, if y is 2003:
```java
    a = 8
    b = 20
    c = 3
    d = 5
    e = 0
    f = 1
    g = 6
    h = 26
    i = 0
    k = 3
    r = 3
    m = 0
    n = 4
    p = 19
```

Therefore, in 2003, Easter fell on April 20 (month = n = 4 and day = p + 1 = 20).

## Assignment:
1. Write a program to solve for the day that Easter falls on for a given year.
2. The program should display the values for all of the variables and the date for Easter. 

A Sample run output for the year 2003 would be:

```java
    a = 8
    b = 20
    c = 3
    d = 5
    e = 0
    f = 1
    g = 6
    h = 26
    i = 0
    k = 3
    r = 3
    m = 0
    n = 4
    p = 19
```

    Easter in 2003 falls on 4/20

3. Verify that the program gives the correct date of Easter for the current year.
Instructions:
1. After completing the program, print your source code and a run output to the printer.
2. Make sure your name is documented near the top of your source code.

This program has been started for you:
```
public class Easter{
    private int y;

    public Easter(int year){
        y = year;
    }

    public void calculate(){
        int a = y % 19;
        System.out.println(“a = “ + a);
        int b = y / 100;
        System.out.println(“b = “ + b);
        ...

    }
}
```