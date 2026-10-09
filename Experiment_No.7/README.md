# Experiment 7: Lexical Analyzer Using LEX

**Course Outcome:** CO3

## Aim
To write a lexical analyzer using Lex/Flex that reads a C-like program and classifies its lexemes into keywords, identifiers, numbers, operators and special symbols.

## Software Required
- Linux, macOS or WSL
- Flex and GCC
- Text editor

## Theory
Lexical analysis is the first phase of a compiler. It reads source code, groups characters into tokens and passes them to the parser.

| Term | Meaning | Example |
|---|---|---|
| Token | Category of lexical unit | KEYWORD |
| Lexeme | Actual character sequence | `int` |
| Pattern | Regular expression describing a token | `[0-9]+` |

## Lexical Analysis Rules
1. Longest match takes priority.
2. When matches have equal length, the first rule wins.
3. Unrecognized characters are reported as UNKNOWN.

## Algorithm
1. Read input using `yylex()`.
2. Recognize keywords.
3. Recognize numbers and identifiers.
4. Recognize operators and special symbols.
5. Ignore whitespace.
6. Report unknown characters.
7. Stop at EOF.

## Source Code
[View Lex Program](lexer.l)

## Execution
```bash
flex lexer.l
gcc lex.yy.c -o lexer
./lexer
```

## Sample Input
```c
int a = 10;
if (a > 5)
    a = a + 1;
```

## Result
The lexical analyzer classifies input lexemes into keywords, identifiers, numbers, operators and special symbols.
