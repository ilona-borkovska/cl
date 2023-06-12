1. Make names descriptive, so they explain the purpose of variables and functions.
2. Don't use literals in expressions (HARDCODE). Instead use constants explaining this values
    - BAD EXAMPLE:
    ```js
    if (numberOfDays >= 7) {
      return basePrice - 50;
    }
    ```
    - GOOD EXAMPLE: 
    ```js
    const LONG_TERM = 7;
    const LONG_TERM_DISCOUNT = 50;

    if (numberOfDays >= LONG_TERM) {
      return basePrice - LONG_TERM_DISCOUNT;
    }
    ```
3. Prefer `const` over `let` where possible, to avoid unintentional changes.
4. Prefer `if` with `return` over `if else` to simplify later conditions. 
5. DON'T add `else` after `if` with `return` - the code after it won't be executed anyway.
    - BAD EXAMPLE:
    ```js
    if (condition) {
      return x;
    } else {
      return y;
    }
    ```
    - GOOD EXAMPLE: 
    ```js
    if (condition) {
      return x;
    }

    return y;
    ```

1. [VARIABLES] - use variables for the main values so that you'll be able to reuse them.
2. [CODE STYLE] - use correct check for property presence in object. Some properties can be present, but still contain falsy value.

GOOD EXAMPLE: 
```
if (key in robot) {
```

EVEN BETTER EXAMPLE:

```
if (robot.hasOwnProperty(key)) {
```

BAD EXAMPLE:
```
if (robot[key] === undefined) {

if (robot[key]) {
```

3. [NAMING] - use proper names for variables - if you want to name variable `result`, pick a better one :)
---
1. [CODE STYLE]: don't use `for in` loop for iterating over array
2. [CODE STYLE]: Use `switch` statement if you have limited amount of conditions.
3. [NAMING]: use proper variable names in `for of` loop

BAD EXAMPLE:
```
for (let item of actions) {

```

GOOD EXAMPLE: 
```
for (const action of actions) {
```
4. [CODE STYLE]: switch/case should always have default case for error handling.
5. [CODE STYLE]: Nested loops === EVIL
6. [CODE KNOWLEDGE]: Remember, if property key is a variable - use brackets `object[key]`. If it's called key - use dot access `object.key`.
---
1. [CODE STYLE] - don't mutate object or arrays - it will cause unexpected results later on. You should make copy using `Object.assign` or `spread` operator
2. [CODE STYLE]: switch/case should always have default case for error handling.
3. [DONT REPEAT YOURSELF] - If you perform same action in all `switch` cases - do it just once afterwards.
4. [NAMING] - use proper names for object copy 


BAD EXAMPLE:
```
const copy = { ...state }

```

GOOD EXAMPLE: 
```
const stateCopy = { ...state }
```
---
1.  [CODE STYLE] - don't mutate original array elements - it will cause unexpected results later on. 
2.  [CODE STYLE] - avoid creating needless copies of arrays, you can iterate existing array
3.  [CODE STYLE] - use `plus` operator with assignment operator `=` if you want to add something to existing value

BAD EXAMPLE:
```
let a = 1;

a = a + 2;
```

GOOD EXAMPLE: 
```
let a = 1;

a += 2;
```

4. [CODE STYLE] - avoid using nested `if` statements, we are sure that you can do it without them :)
5. [CODE STYLE] - don't write loops inside `if` statement. It's making your code too complicated. Remember that loop with `false` condition simply will iterate 0 times.
---
1.  [NAMING] - Use proper names for variables. If function was called `makeFruit`, it should return `fruit`
2.  [CODE STYLE] - use arithmetic operators with assignment operator `=` if you want to add something to existing value

BAD EXAMPLE:
```
let a = 1;

a = a + 2;
```

GOOD EXAMPLE: 
```
let a = 1;

a += 2;
```
3. [CODE KNOWLEDGE] - if you creating a method in the object, you don't need to use function keyword, use shortcut instead.


BAD EXAMPLE: 
```
 methodName: function() {
 // your code
},
```

GOOD EXAMPLE:
```
 methodName() {
 // your code
},
```
