# bolo() Function — Full Documentation & Usage Guide

The `bolo()` function is the standard output/print function in EkushScript. It supports advanced formatting, type safety, and robust string handling. Below are all supported features, usage patterns, and important notes.

---

## 1. Basic Output

```ekush
bolo("Hello World!")                // Output: Hello World!
bolo("Number:", 21)                  // Output: Number: 21
bolo("PI =", 3.14159)                // Output: PI = 3.14
```

- You can pass multiple arguments; they will be printed with a space between them.
- Numbers are formatted as described below.

---

## 2. Escape Characters in Strings

```ekush
bolo("line1\nline2")
bolo("tab\tseparated")               // Output: tab    separated
bolo("quote: \" and backslash: \\")   // Output: quote: " and backslash: \
```

**Supported escape sequences:**

- `\n` : New line
- `\t` : Tab
- `\"` : Double quote
- `\'` : Single quote
- `\\` : Backslash
- `\r` : Carriage return
- `\b` : Backspace
- `\v` : Vertical tab

---

## 3. String Concatenation

```ekush
bolo("Welcome" + " to")               // Output: Welcome to
bolo("Ekush" jog "Script")            // Output: EkushScript
bolo("pi = " + 3.14159)               // Output: pi = 3.14
```

- You can concatenate strings using `+` or the Bengali `jog` operator.
- Concatenation with numbers is allowed (number is converted to string).
- **Type Safety:**
  - Only `string+string` or `string+number` or `number+string` is allowed.
  - Any attempt to concatenate a string with a boolean, array, or other type will throw a clear error.

```ekush
bolo("hello" + true)                  // Error: Only string with string/number allowed
```

---

## 4. Float Formatting

```ekush
bolo(3.14159)                         // Output: 3.14
rakho pi = 3.14159
bolo("Value: " + pi)                  // Output: Value: 3.14
```

- All floating-point numbers are printed with 2 decimal places.

---

## 5. Template-like String Formatting

```ekush
rakho name = "Ekush"
bolo("Hello, ${name}!")              // Output: Hello, Ekush!
bolo("Sum: ${2 + 3}")                // Output: Sum: 5
bolo("Float: ${3.14159}")            // Output: Float: 3.14159
```

- You can embed expressions and variables inside `${...}` in double-quoted strings.
- The expressions are evaluated in the current script context.
- If the variable is not defined, the placeholder will remain unchanged.

---

## 6. Arrays and Special Values

```ekush
bolo([1, 2, 3])                       // Output: [1,2,3]
bolo(thik)                            // Output: thik
bolo(bhul)                            // Output: bhul
bolo(faka)                            // Output: faka
```

- Arrays are printed as comma-separated lists in brackets.
- Special values: `thik` (true), `bhul` (false), `faka` (null) are printed in Bengali.

---

## 7. Error Handling

- If you try to concatenate a string with a boolean, array, or other unsupported type, you will get a clear, professional error message in Romanized Bengali.
- Example:

```ekush
bolo("hello" + thik)
```

>🚨 EkushScript Error [Line 1]:  
>Ektu bhabo! Jog ba concatenation shudhu string er shathe string, ba number kora jabe.

---

## 8. Comments

- Use `//` for single-line comments and `/* ... */` for multi-line comments in your EkushScript code.
