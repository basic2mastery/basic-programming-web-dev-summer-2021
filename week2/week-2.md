# Week 2

---

# Homework

https://jsfiddle.net/mreigen/mqtv0d2o/

In class execise on Wednesday:

https://jsfiddle.net/mreigen/8hjgx3by

---

`var` vs `let`
Before ECMAScript 2015, javascript doesn’t have “block statement” scope so if you declared a variable inside a block (this is a “block”{…}) it will be accessible to the function within which that block resides. For example:

```javascript
if (true) {
  var x = 3;
}
console.log(x); // x is 3 here
```

This can cause confusion if you would declare another x variable in the same function but outside of that if statement. That is why let was introduced in ECMAScript 2015

```javascript
if (true) {
  let y = 3;
}
console.log(y); // ReferenceError: y is not defined
```

# Conditional statements

## Block statement

The most basic statement is a block statement, which is used to group statements. The block is delimited by a pair of curly brackets:

```javascript
{
  statement_1;
  statement_2;
  ⋮
  statement_n;
}
```

## If / Else

```javascript
if (condition_1) {
  statement_1;
} else if (condition_2) {
  statement_2;
} else if (condition_n) {
  statement_n;
} else {
  statement_last;
}
```

## Falsy values

The following values evaluate to false (also known as Falsy values):

```javascript
false
undefined
null
0
NaN
the empty string ("")
```

## True/False table

You should know these tables by heart regardless of what computer language you are learning or will learn. This is universal. If anything, the very least thing the Martians or Venusians :alien: will agree with us are these tables.

https://docs.google.com/spreadsheets/d/1duDk-GxJAFwGhw1MPqj--QNpF63dPlUNPo6Dxv_aWxs

## == vs ===

`==` is used to compare just the values
`===` is used to compare both the values and types of the variables being compared

# Switch statement

```javascript
switch (expression) {
  case label_1:
    statements_1
    [break;]
  case label_2:
    statements_2
    [break;]
    …
  default:
    statements_def
    [break;]
}
```

# Loops

## For

```javascript
for (let step = 0; step < 5; step++) {
  // Runs 5 times, with values of step 0 through 4.
  console.log("Walking east one step");
}
```

## do while

```javascript
let i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

## For in / of

```javascript
const arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
  console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
  console.log(i); // logs 3, 5, 7
}
```

## String intepolation

```javascript
str1 = "I'm";
str2 = "human";
console.log(`${str1} ${str2}`);
console.log(str1 + " " + str2);
console.log([str1, str2].join(" "));
```

Be careful:

```javascript
str1 = "30";
console.log(str1 + 8); // 308
console.log(str1 - 8) + // 22
  "30"; // 30
parseInt(str1); // 30
```

## Functions

As you already know in our execises and homework, this is how you _typically_ define a function, using the `function` keyword:

```javascript
function printMe(str) {
  console.log(str);
}
printMe("hey!"); // hey!
```

Another way you can define a function is to create a variable and assign a function to it! The right side of the `=` sign is a function, the left side of the `=` is the variable. Note that this function on the right side doesn't have a name. It's called an annonymous function!

```javascript
const printMe = function (str) {
  console.log(str);
};
printMe("hey!"); // hey!
```

A third way to define a function is to use the "Arrow" (`=>`) function definition:

```javascript
const printMe = (str) => {
  console.log(str);
};
printMe("hey!"); // hey!
```

---

## Slack me if you have any questions!

---
