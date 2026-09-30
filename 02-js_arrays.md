---
course: javascript
slug: arrays
title: Arrays and Array Methods
description: "Learn how arrays store lists of data, how indexing works, and how to use common array methods like forEach, map, and filter."
---

## Arrays: the OG data structure

When you build a project, you need a way to store data so it's easy to access and modify. One structure commonly used in JS is the **array**.

An array is a single variable used to store a list of multiple items — think of it like a bookshelf where each slot is numbered.

- **Index:** each item in an array has a unique position, called its index.
- **Zero-indexing:** computers start counting at `0`, not `1`. The first item is at index `0`, the second at index `1`, and so on.

```javascript
// Creating an array
const frontendTools = ["HTML", "CSS", "JavaScript"];

// Accessing items by index
console.log(frontendTools[0]); // "HTML"
console.log(frontendTools[2]); // "JavaScript"

// Updating an item
frontendTools[1] = "Tailwind CSS";
console.log(frontendTools); // ["HTML", "Tailwind CSS", "JavaScript"]
```

## Array methods: making our work easier

JS gives us built-in methods (functions) for working with arrays. Here are three of the most common.

### `.forEach()` — loops through each item

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach(function (number) {
  console.log(number * 2);
});
// Logs: 2, 4, 6, 8, 10
```

### `.map()` — creates a new array by transforming each item

Unlike `forEach`, `map` **returns a new array** instead of just looping.

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(function (number) {
  return number * 2;
});

console.log(doubled); // [2, 4, 6, 8, 10]
```

> [!NOTE]
> Use `forEach` when you just want to do something with each item (like printing it). Use `map` when you want a new array back.

### `.filter()` — creates a new array with items that pass a test

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter(function (number) {
  return number % 2 === 0;
});

console.log(evenNumbers); // [2, 4]
```

## Try it yourself

1. Use `forEach` to print every number in `[1, 2, 3, 4, 5]` multiplied by 2.
2. Use `map` to create a new array where every number in `[1, 2, 3, 4, 5]` is squared.
3. Use `filter` to get only the numbers greater than 2 from `[1, 2, 3, 4, 5]`.
