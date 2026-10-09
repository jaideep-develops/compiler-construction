# Experiment 5: Source Code Optimization

**Course Outcome:** CO5

## Aim
To demonstrate source code optimization using operator strength reduction, dead code elimination and frequency reduction.

## Theory
Code optimization improves intermediate or target code without changing the program's meaning.

## A. Operator Strength Reduction
Before:
```c
x = i * 2;
```
After:
```c
x = i + i;
```

## B. Dead Code Elimination
Before:
```c
int a = 10;
int b = 20;
int c = a + b;
int x = 100;
printf("%d", c);
```
After:
```c
int a = 10;
int b = 20;
int c = a + b;
printf("%d", c);
```
The variable x is never used, so its declaration and assignment can be removed.

## C. Frequency Reduction / Loop-Invariant Code Motion
Before:
```c
for (i = 0; i < 100; i++) {
    x = a * b;
    y = x + i;
}
```
After:
```c
x = a * b;
for (i = 0; i < 100; i++) {
    y = x + i;
}
```
The computation a * b is moved outside the loop.

## Source Code
[View C Program](Source_code_optimization.c)

## Result
The experiment demonstrates source code optimization techniques.
