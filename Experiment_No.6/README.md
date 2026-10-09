# Experiment 6: Design of a Simple High-Level Language (MiniLang)

**Course Outcome:** CO6

## Aim
To design a simple high-level language containing arithmetic and logical operations, pointers, branch instructions and loop instructions.

## Software Required
- GCC / Turbo C / Code::Blocks / VS Code
- C compiler

## Theory
A programming language is defined using lexical rules, syntax rules, statements and expressions. MiniLang is implemented using C and performs lexical analysis and basic syntax validation.

## Language Features

| Feature | Supported Constructs |
|---|---|
| Variable Declaration | `int a;`, `int b;` |
| Arithmetic | `+`, `-`, `*`, `/`, `%` |
| Relational | `<`, `>`, `<=`, `>=`, `==`, `!=` |
| Logical | `&&`, `\|\|`, `!` |
| Pointer | `*`, `&` |
| Branching | `if`, `else` |
| Loop | `while` |
| Assignment | `=` |

## Compiler Front-End Architecture
```text
MiniLang Source Program
        ↓
Lexical Analyzer
        ↓
Tokens
        ↓
Syntax Parser
        ↓
Syntax Validation
        ↓
Semantic Analysis
        ↓
Intermediate Code
```

## Algorithm
1. Start and read the MiniLang source program.
2. Scan input character by character.
3. Identify keywords, identifiers and constants.
4. Identify arithmetic, relational and logical operators.
5. Identify delimiters and special symbols.
6. Display generated tokens.
7. Check basic syntax and report errors.
8. Stop.

## Source Code
[View MiniLang C Program](minLanguage.c)

## Result
The MiniLang implementation identifies keywords, identifiers, constants, operators and delimiters and performs basic syntax validation.
