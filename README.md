# CS56-M16-DRAFT-parser-project-01
FIRST DRAFT of student facing writeup for M16 Draft Parser Project


# What you will do in this project

In this project you will implement a parser for arithmetic expressions.

The parsing technique you will use is called *recursive descent*.  The advantage of a *recursive descent* parser is that it is relatively easy to understand how to write the code.

This project will give you a taste of some topics that you'll explore in far more depth if/when you take these courses:

* CMPSC 160: Compilers
* CMPSC 162: Programming Languages

# What you'll be implemeting

A compiler or interpreter for a programming language, or any other formal language is typically divided into many subcomponents.  Two of the most important are a "tokenizer" and a "parser".  You'll be implementing both of those in this project.    

A tokenizer is typically the first thing that a compiler does with its input.  The job of the tokenizer is to simplify the input to the parser, by grouping related characters together.  Another way to say this, is that it turns a sequence of characters into a sequence of tokens.  An example will help.  Consider this line of Java code:
```Java
   for (int i=0; i<=10; i++) {
```
In this line of code, there are about 32 characters, starting with space, space, space, f, o, r, etc.   However, if we consider the sequence of tokens, there are only 14.  Note that `for` is treated as a single token, as is `<=`.  Whitespace (spaces, tabs, newlines) are discarded.

| `for`  |  `(` | `int`  |  `i` | `=`  |  `0` | `;`  |
|---|---|---|---|---|---|---|
| `i`  |  `<=` |  `;` | `i`  |  `++` |  `)` | `}`  |


There are 
You'll be implementing parser object with a method `AST parse(String input)` that can take a string as input, and then either throw produce, as output, an Abstract Syntax Tree.

We'll explain what an Abstract Syntax Tree is shortly.

Your parser will take, as input, an arithmetic expression involving integers several operators.

We will walk you, step by step, through the construction of a relatively simple parser that can handle these binary operators:

* + (addition) and - (subtraction)
* * (multiplication) and / (integer-division)

In every case, the result of applying any of these binary operators to two integer operands is, itself, an integer&mdash;except in the one special case of division by zero. For that case, you'll need to throw an exception.

What your 
