# Project Challenge 01

## Junior Front-End Developer Interview Question.

### Monday, Aug 15th 2016 - Denver, CO U.S.A. 80210

#### Tags
* JavaScript
* Algorithms
* Programming

## Challenge

<strong>Diff a list of results...</strong>

* Write a function that takes two arrays full of objects and outputs a list of their changes, as seen below.

* You can assume that the `ID` of each object will be persistent and unique, but other values won't be. Don't assume that `name` and `quantity` are the only values to diff.

## Data

```javascript
const list = [
  {
    id       : 1,
    name     : 'Barbara',
    quantity : 3,
  },
  {
    id       : 2,
    name     : 'Tom',
    quantity : 0,
  },
  {
    id       : 3,
    name     : 'Sam',
    quantity : 1,
  },
];

const updatedList = [
  // barb's name is changing
  {
    id       : 1,
    name     : 'Barb',
    quantity : 3,
  },

  // sam's quantity is changing
  {
    id       : 3,
    name     : 'Sam',
    quantity : 8,
  },

  // tom has been deleted

  // nelson is being added
  {
    id       : 4,
    name     : 'Nelson',
    quantity : 6,
  },
];

getDiffBetween(list, updatedList);
```

> Calling `getDiffBetween()` with `list` as first parameter and `updatedList` as second parameter should equal the following...

```javascript
[
  {
    type     : 'CHANGE',
    id       : 1,
    name     : 'Barb',
  },
  {
    type     : 'REMOVE',
    id       : 2,
  },
  {
    type     : 'CHANGE',
    id       : 3,
    quantity : 8,
  },
  {
    type     : 'ADD',
    id       : 4,
    name     : 'Nelson',
    quantity : 6,
  },
]
```





