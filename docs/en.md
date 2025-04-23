# EkushScript Documentation

**EkushScript** is a Bengali Romanized programming language that compiles to JavaScript, designed to make programming accessible to Bengali speakers while maintaining modern programming practices.

> নিজের ভাষায় প্রোগ্রামিং শুরু হোক আজই! 🇧🇩

## Table of Contents

1. [Getting Started](#getting-started)
   - [Installation](#installation)
   - [Quick Start](#quick-start)
   - [CLI Usage](#cli-usage)

2. [Language Fundamentals](#language-fundamentals)
   - [Basic Syntax](#basic-syntax)
   - [Comments](#comments)
   - [Data Types](#data-types)
   - [Variables](#variables)

3. [Operators and Expressions](#operators-and-expressions)
   - [Arithmetic Operators](#arithmetic-operators)
   - [Comparison Operators](#comparison-operators)
   - [Assignment Operators](#assignment-operators)

4. [Control Flow](#control-flow)
   - [Conditional Statements](#conditional-statements)
   - [Loops](#loops)
   - [Loop Control Statements](#loop-control-statements)

5. [Functions](#functions)
   - [Function Declaration](#function-declaration)
   - [Return Values](#return-values)

6. [Data Structures](#data-structures)
   - [Arrays](#arrays)
   - [Array Methods](#array-methods)
   - [Array Properties](#array-properties)

7. [Built-in Functions](#built-in-functions)
   - [Console Output](#console-output)
   - [Input Functions](#input-functions)

8. [Development Tools](#development-tools)
   - [REPL Usage](#repl-usage)
   - [Compilation](#compilation)
   - [Debugging](#debugging)

## Getting Started

### Installation

```bash
npm install -g ekushscript
```

### Quick Start

Create your first EkushScript program:

```ekush
// hello.ekush
rakho nam = "EkushScript";
bolo("Hello," nam "!");
```

Run it:

```bash
ekush run hello.ekush
```

### CLI Usage

```bash
ekush run <file>      # Run an EkushScript file
ekush repl            # Start interactive REPL
ekush compile <file>  # Compile to JavaScript
ekush -v              # Show version
ekush --version       # Show version
```

## Language Fundamentals

### Basic Syntax

- Statements can end with optional semicolons (;)
- Blocks are enclosed in curly braces {}
- Keywords are in Bengali Romanized form
- Case-sensitive identifiers

### Comments

```ekush
// Single line comment

/* 
   Multi-line
   comment
*/
```

### Data Types

1. **Numbers**

   ```ekush
   rakho purnoSongkha = 42;      // Integer
   rakho vognangso = 3.14;       // Float
   ```

2. **Strings**

   ```ekush
   rakho text = "Hello World";   // Double quotes
   ```

3. **Booleans**

   ```ekush
   rakho sotti = thik;           // true
   rakho mittha = bhul;          // false
   ```

4. **Null**

   ```ekush
   rakho khali = faka;           // null
   ```

5. **Arrays**

   ```ekush
   rakho list = [1, 2, 3];       // Number array
   rakho mixed = [1, "two", thik]; // Mixed types
   ```

### Variables

Declaration and assignment:

```ekush
rakho boyosh = 21;         // Declaration with initialization
```

## Operators and Expressions

### Arithmetic Operators

```ekush
rakho a = 10;
rakho b = 3;

rakho jogfol = a jog b;        // Addition (13)
rakho biyogfol = a biyog b;    // Subtraction (7)
rakho gunfol = a gun b;        // Multiplication (30)
rakho vagfol = a vag b;        // Division (3.333...)
rakho vagshesh = a vag_shesh b; // Modulus (1)
```

> Note: `jog`, `biyog`, `gun`, `vag`, `vag_shesh` are the operators for addition, subtraction, multiplication, division, and modulus respectively. All of these operators are binary operators, meaning they take two operands. You can also use the `+`, `-`, `*`, `/`, `%` operators for addition, subtraction, multiplication, division, and modulus respectively.

### Comparison Operators

```ekush
rakho x = 5;
rakho y = 10;

jodi (x == y) { }     // Equal to
jodi (x != y) { }     // Not equal to
jodi (x < y) { }      // Less than
jodi (x > y) { }      // Greater than
jodi (x <= y) { }     // Less than or equal to
jodi (x >= y) { }     // Greater than or equal to
```

### Assignment Operators

```ekush
rakho x = 5;
x jog= 3;             // x = x + 3
x biyog= 2;           // x = x - 2
x gun= 2;             // x = x * 2
x vag= 3;             // x = x / 3
x vag_shesh= 2;       // x = x % 2
```

> Note: You can also use the `+=`, `-=`, `*=`, `/=`, `%=` operators for addition, subtraction, multiplication, division, and modulus respectively.

## Control Flow

### Conditional Statements

1. **Simple If**

   ```ekush
   jodi (condition) {
       // code
   }
   ```

2. **If-Else**

   ```ekush
   jodi (condition) {
       // code
   } nahoi {
       // else code
   }
   ```

3. **If-Else If-Else**

   ```ekush
   jodi (condition1) {
       // code
   } nahoi jodi (condition2) {
       // else if code
   } nahoi {
       // else code
   }
   ```

### Loops

1. **While Loop**

   ```ekush
   jotokkhon (condition) {
       // code
   }
   ```

2. **For Loop**

   ```ekush
   ghuro (rakho i = 0; i < 5; i += 1) {
       // code
   }
   ```

### Loop Control Statements

```ekush
ghuro (rakho i = 0; i < 10; i += 1) {
    jodi (i == 5) {
        thamo;        // Break
    }
    jodi (i == 3) {
        cholo;        // Continue
    }
    bolo(i);
}
```

## Functions

### Function Declaration

```ekush
kaj nameBolo(nam) {
    bolo("Hello,", nam);
}

// With default parameters
kaj jogKoro(a, b = 0) {
    ferot a jog b;
}
```

### Return Values

```ekush
kaj gunKoro(a, b) {
    ferot a gun b;    // Return value
}

kaj boloAndFerot(text) {
    bolo(text);
    ferot thik;       // Return boolean
}
```

## Data Structures

### Arrays

Creation and access:

```ekush
rakho numbers = [1, 2, 3, 4, 5];
bolo(numbers); // [1, 2, 3, 4, 5]

rakho first = numbers[0];     // Array access
bolo(first); // 1
```

### Array Methods

```ekush
rakho list = [1, 2, 3];

list.jog_koro(4);            // Push: [1, 2, 3, 4]
list.ber_koro();             // Pop: [1, 2, 3]

// find pop element
rakho lastElement = list.ber_koro();
bolo(lastElement);
```

### Array Properties

```ekush
rakho list = [1, 2, 3, 4, 5];
rakho size = list.lomba();    // Length: 5
```

## Built-in Functions

### Console Output

```ekush
bolo("Hello");                // Single value
bolo("X =", x);              // Multiple values
bolo("Array:", numbers);     // Array output
```

### Input Functions

```ekush
rakho input = shuno("Enter your name: ");  // Read user input
```

## Development Tools

### REPL Usage

Interactive development environment:

```bash
$ ekush repl
> rakho x = 10
> bolo(x)
10
> x gun 2
20
```

> ⚠️ Important: The `shuno()` input function is currently not supported in REPL mode. This feature will be available in a future release.

### Compilation

Convert EkushScript to JavaScript:

```bash
ekush compile source.ekush
# Creates source.js with equivalent JavaScript code
```

### Debugging

1. Use `bolo()` for debugging output
2. Check compilation output with `ekush compile`
3. Use REPL for testing expressions

## Best Practices

1. Use meaningful variable names
2. Add comments for complex logic
3. Use proper indentation
4. Break down complex operations into functions
5. Handle errors appropriately
6. Use consistent naming conventions

## Common Pitfalls

1. Case sensitivity in identifiers
2. Forgetting to declare variables with `rakho`
3. Missing parentheses in conditions
4. Missing curly-braces `{}` in if-else, loop, and function statements
