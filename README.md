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
