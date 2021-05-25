## Lesson 00
# Basic glossary

Here is all the basic's for JavaScript language. The syntax and what it's for.

## Comments

So the first basics about code is no code. The syntax for a comment is a double forward slash in JavaScript `//`. It works like `<!-- -->` in HTML except `//` comments out the entire line. 

```ts
const test = true;
// Hello! This is a comment
```

You can comment out code with this too

```ts
// const test = true; // this is now not going to run
```

### Comment block

A comment block is a multiple line comment section. The sytax for this is started by a forward slash and double asterix `/**`. It's ended by an asterix and and forward slash `*/`. Anything between these 2 lines are considered commented

```ts
/**
* Hello I'm a comment section
* const test = true;
*
* Everything here is commented! 
*/
```

## Console

The console is a very handy tool in JavaScript to use to debug (find errors) your code! But here I'm using it as an example. When you see `console.log()` it means anything inside the brackets `()` is 'printed' (logged) to the console. 


In my code examples you'll sometimes see a comment following the console.log like so `console.log("hello"); // "hello"`. This is what would be outputted to the console of you ran the example code. 

## Variables

Variables are like little storage devices. They're used to store all sorts of data and information. Numbers, strings, calculated values and many others. Anything can be stored in a variable in JavaScipt.

### Const 

`const` or (short for) constant: Is a block scoped variable that can never be changed.

```ts
const test = true;
const value = 2 + 3; // 5
const hello = "Hello this is a hello message string";
```

What I mean by cannot be changed (redeclared)

```ts
const test = true;
test = false; // You cannot do this, it won't be allow. No really!
```

### Let

A `let` (short for "let") and is a block scoped variable that CAN be changed (the different between const).

```ts
let test = true;
test = false; // THIS IS ALLOW :O :O :O

let value = 2;

value = value + 3; // shorthand is value += 3;
```

### Var

`var` is a now outdated but still used term for declaring a variable. var is now considered "global scope" which is fancy talk for "can be used absolutely everywhere". Think of a scopes as different functions (more of this at /#scopes). 

### Scopes

```ts
var global = true;

function scope1() {
  const scoped = true;
  console.log('values', global, scoped); // 'values', true, true
}

function scope2() {
  console.log('values', global, scoped); // 'values', true, undefined
}
```

> `global` can be found anywhere, `scoped` can only be found in the top function `scope1`.

## if statements 

Have you heard the dev job "My wife asked me to by some milk, if they have eggs, get 6. So I came home with 6 pints of milk". This is a logic joke. Get milk, if they have eggs: get 6 pints of milk. It's also a bit pedantic in the sense that "it didn't specify 6 of what" but you get the idea. 

Now I'm going to show you some code and we're going to work this into the joke: this is to help go from English to JavaScript.

The below example is not correct syntax but it'll help you understand the logic.

```ts
if (condition is true) {
  // run this code here
}
```
So an if statement looks like this `if () {}`. First you specify that it's an if statement with `if`. This is a keyword in JavaScript.

The condition goes between the brackets `()`.

The code to be ran goes between the braces `{}`.

if the condition is truthful then the code block will run. That's it! 

So our joke can be written like so

```ts
shopHasEggs = true;

let milkToGet = 1;

if (shopHasEggs === true) { // true === true // this equals true
  milkToGet = 6;
}

console.log('Milk to be got', milkToGet); // 6
```

Now let's look at something that is falsy (doesn't work: not true).

```ts
const name = "Ashleigh"

if (name === "Bob") { // "Ashleigh" === "Bob" // this equals false
  console.log("Hello Cat");
}
```

In the above example "Ashleigh" does not equal "Bob" so `"Hello Cat"` will never be logged to the console.

### Else statement

An else block is what happens when the condition does not match. Let's have a look at this 

```ts
const number = 3;

if (number === 12) {
  console.log("number is 12");
} else {
  console.log("number is not 12");
}
```

## Functions

Functions are blocks of code that you can save and run when you want them to


### return values

## Types

