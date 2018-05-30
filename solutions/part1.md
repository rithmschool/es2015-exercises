## ES2015 Exercise Part I Solution

Convert the following es5 code blocks into es2015 code:

### ES5 String Concatenation

```javascript
var name = 'Michael';
var favoriteColor = 'purple';
var city = 'San Francisco';

console.log(
  name +
    ' lives in ' +
    city +
    ' and his favorite color is ' +
    favoriteColor +
    '.'
);
```

### ES6 Template Literals

```javascript
var name = 'Michael';
var favoriteColor = 'purple';
var city = 'San Francisco';

console.log(
  `${name} lives in ${city} and his favorite color is ${favoriteColor}.`
);
```

### ES5 Global Constants

```javascript
var PI = 3.14;
PI = 42; // stop me from doing this!
```

### ES6 Global Constants

```javascript
const PI = 3.14;
PI = 42; /* TypeError: Assignment to constant variable. */
```

### ES5 Assigning Variables to Object Properties

```javascript
var obj = {
  numbers: {
    a: 1,
    b: 2
  }
};

var a = obj.numbers.a;
var b = obj.numbers.b;
```

### ES6 Object Destructuring

```javascript
var obj = {
  numbers: {
    a: 1,
    b: 2
  }
};

var { a, b } = obj.numbers;
```

### ES5 Array Swap

```javascript
var arr = [1, 2];
var temp = arr[0];
arr[0] = arr[1];
arr[1] = temp;
```

### ES6 One-Line Array Swap with Destructuring

```javascript
const arr = [1, 2];
[arr[1], arr[0]] = [arr[0], arr[1]];
```

### ES5 Map Callback

```javascript
function double(arr) {
  return arr.map(function(val) {
    return val * 2;
  });
}
```

### ES6 Map Callback Shorthand

```javascript
function double(arr) {
  return arr.map(val => val * 2);
}
```

### ES5 Default Arguments

```javascript
function add(a, b) {
  if (a === 0) {
    a = 0;
  } else {
    a = a || 10;
  }
  if (b === 0) {
    b = 0;
  } else {
    b = b || 10;
  }
  return a + b;
}
```

### ES6 Default Arguments

```javascript
function add(a = 10, b = 10) {
  return a + b;
}
```

### ES5 Function that takes a variable number of arguments

```javascript
function sumMany() {
  var nums = Array.prototype.slice.call(arguments);
  return nums.reduce(function(a, b) {
    return a + b;
  }, 0);
}
```

### ES6 Function that takes a variable number of arguments

```js
function sumMany(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
```
