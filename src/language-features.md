# Language Features

## Strict Mode
Add this to the very top of a function or a script:
```
"use strict";
```
Strict mode makes several changes to normal JavaScript semantics:
- Prohibits some syntax likely to be defined within future versions of ECMAScript.
- Removes some of JavaScript's silent errors by changing them to throw errors.
- Modifies code that makes it difficult for JavaScript engines to optimize, with the result that strict mode sometimes runs faster than non-strict.
- In React, it's not necessary to declare strict mode.

## ES6 and Hoisting
Hoisting is the default behavior of moving all declarations (but not initializations) to the top of the scope before executing the code. It applies to functions and variables. It allows JavaScript to use the component before its declaration.
- Hoisting does not apply to scripts that run in strict mode.
- aJavaScript only hoists the variable declaration, not variable initialization.

## Variables

From [W3Schools](https://www.w3schools.com/Js/js_variables.asp).

Declare with `var`, `let`, and `const` (or nothing)

- The `var` keyword was used in all JavaScript code from 1995 to 2015.
- The `let` and `const` keywords were added to JavaScript in 2015.
- You cannot re-declare a variable declared with `let` or `const`.
- You cannot re-assign a variable declared with `const`.
- Variables defined with `let` must be declared before use.
- Variables defined with `let` have Block Scope.
```
let person = "John Doe", carName = "Volvo", price = 200;
let carName;  // Will have undefined as value
```
- $ is a valid character in a variable name.  Programmers often use it as an alias for the main function in a JavaScript library.
- "_" is a valid character in a variable name.  A convention among programmers is to prefix private/hidden variables with "_".

### Block Scope and variables
- Before ES6 (2015), JavaScript had only Global Scope and Function Scope.
- let and const provide Block Scope in JavaScript.

Variables declared inside a { } block cannot be accessed from outside the block:
{
  let x = 2;
}
// x can NOT be used here
//


## export - Exposing to Other Files
To make functions, constants, or variables available in other files, they need to be exported using the `export` keyword. Another file may then import these using the `import` keyword. This is also known as the module system.

A great example is how all the tests work. Each exercise has at least one file, for example lasagna.js, which contains the implementation. Additionally, there is at least one other file, for example lasagna.spec.js, that contains the tests.


