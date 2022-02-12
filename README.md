# **Big O Notation Exercises Solution**

- [Part1](#part1)
- [Part2](#part2)

<hr>

## Part 1  <span id="part1"></span>
Simplify the following big O expressions as much as possible:

- `O(n + 10)` 
     - After simplify: O(n)
- `O(100 * n)`
     - After simplify: O(n)
- `O(25)`
     - After simplify: O(1)
- `O(n^2 + n^3)`
     - After simplify: O(n<sup>3</sup>)
- `O(n + n + n + n)`
     - After simplify: O(n)
- `O(1000 * log(n) + n)`
     - After simplify: O(n)
- `O(1000 * n * log(n) + n)`
     - After simplify: O(n * log(n))
- `O(2^n + n^2)`
     - After simplify: O(2<sup>n</sup>)
- `O(5 + 3 + 1)`
     - After simplify: O(1)
- `O(n + n^(1/2) + n^2 + n * log(n)^10)`
     - After simplify: O(n<sup>2</sup>)


<hr/>

## Part 2 <span id="part2"></span>

Determine the time and space complexities for each of the following functions. If you're not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```js
// 1.

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}

```
- Time = O(n)
- Space = O(1)

<hr>

```js
// 2.

function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```
- Time = O(1)
- Space = O(1)

<hr>

```js
// 3.

function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```
- Time = O(n)
- Space = O(1)
<hr>

```js
// 4.

function onlyElementsAtEvenIndex(array) {
  let newArray = Array(Math.ceil(array.length / 2));
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray[i / 2] = array[i];
    }
  }
  return newArray;
}
```
- Time = O(n)
- Space = O(n)
<hr>

```js
// 5.

function subtotals(array) {
  let subtotalArray = Array(array.length);
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray[i] = subtotal;
  }
  return subtotalArray;
}
```
- Time = O(n<sup>2</sup>)
- Space = O(2)

<hr>

## Done By [Nada Abuzaid](https://github.com/nada-abuzaid)
