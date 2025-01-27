---
id: 587d7b87367417b2b2512b41
title: Declare a Read-Only Variable with the const Keyword
challengeType: 1
forumTopicId: 301201
dashedName: declare-a-read-only-variable-with-the-const-keyword
---

# --description--

The keyword `let` is not the only new way to declare variables. In ES6, you can also declare variables using the `const` keyword.

`const` has all the awesome features that `let` has, with the added bonus that variables declared using `const` are read-only. They are a constant value, which means that once a variable is assigned with `const`, it cannot be reassigned:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

The console will display an error due to reassigning the value of `FAV_PET`.

You should always name variables you don't want to reassign using the `const` keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.

A common practice when naming constants is to use all uppercase letters, with words separated by an underscore.

**Note:** It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays). You will learn more about objects, arrays, and immutable and mutable values in later challenges. Also in later challenges, you will see examples of uppercase, lowercase, or camelCase variable identifiers.

# --instructions--

Change the code so that all variables are declared using `let` or `const`. Use `let` when you want the variable to change, and `const` when you want the variable to remain constant. Also, rename variables declared with `const` to conform to common practices, meaning constants should be in all caps.

# --hints--

`var` should not exist in your code.

```js
(getUserInput) => assert(!getUserInput('index').match(/var/g));
```

You should change `fCC` to all uppercase.

```js
(getUserInput) => {
  assert(getUserInput('index').match(/(FCC)/));
  assert(!getUserInput('index').match(/fCC/));
}
```

`FCC` should be a constant variable declared with `const`.

```js
assert.equal(FCC, 'freeCodeCamp');
assert.match(code, /const\s+FCC/);
```

`fact` should be declared with `let`.

```js
(getUserInput) => assert(getUserInput('index').match(/(let fact)/g));
```

`console.log` should be changed to print the `FCC` and `fact` variables.

```js
(getUserInput) =>
  assert(getUserInput('index').match(/console\.log\(\s*FCC\s*\,\s*fact\s*\)\s*;?/g));
```

# --seed--

## --seed-contents--

```js
// Only change code below this line
var fCC = "freeCodeCamp";
var fact = "is cool!";
// Only change code above this line

fact = "is awesome!";
console.log(fCC, fact);
```

# --solutions--

```js
const FCC = "freeCodeCamp";
let fact = "is cool!";

fact = "is awesome!";
console.log(FCC, fact);
```
