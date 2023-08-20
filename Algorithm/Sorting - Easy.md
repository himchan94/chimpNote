# Sorting


# Bubble

```js
function bubbleSort(arr) {

for (let i \= 0; i < arr.length; i++) {

for (let j \= i + 1; j < arr.length; j++) {

if (arr\[i\] \> arr\[j\]) \[arr\[i\], arr\[j\]\] \= \[arr\[j\], arr\[i\]\];

else if (arr\[i\] < arr\[j\]) \[arr\[i\], arr\[j\]\] \= \[arr\[i\], arr\[j\]\];

else continue;

}

}

console.log("sortedArr", arr);

return arr;

}

  

bubbleSort(\[5, 3, 100, 4, 23, 300, \-3, 0, 9\]);

  

solution \- 1

function bubbleSort(arr) {

for (let i \= 0; i < arr.length; i++) {

for (let j \= 0; j < arr.length; j++) {

if (arr\[j\] \> arr\[j + 1\]) {

let temp \= arr\[j\];

arr\[j\] \= arr\[j + 1\];

arr\[j + 1\] \= temp;

}

}

}

  

return arr;

}

  

solution - 2

function bubbleSort(arr) {

for (let i = arr.length; i > 0; i--) {

for (let j = 0; j < i - 1; j++) {

if (arr\[j\] > arr\[j + 1\]) {

let temp = arr\[j\];

arr\[j\] = arr\[j + 1\];

arr\[j + 1\] = temp;

}

}

}

  

return arr;

}

  

soultion - 3

function bubbleSort(arr) {

const swap = (arr, idx1, idx2) => {

\[arr\[idx1\], arr\[idx2\]\] = \[arr\[idx2\], arr\[idx1\]\];

};

  

for (let i = arr.length; i > 0; i--) {

for (let j = 0; j < i - 1; j++) {

if (arr\[j\] > arr\[j + 1\]) swap(arr, j, j + 1);

}

}

  

return arr;

}

  

bubbleSort(\[37, 45, 29, 8\]);

```

### Insertion
```js

function insertionSort(arr) {

for (let i \= 1; i < arr.length; i++) {

let currentVal \= arr\[i\];

for (var j \= i \- 1; j \>= 0 && arr\[j\] \> currentVal; j\--) {

arr\[j + 1\] \= arr\[j\];

}

arr\[j + 1\] \= currentVal;

}

return arr;

}

  

insertionSort(\[2, 1, 9, 76, 4\]);

```

### Selection

```js
function selectionSort(arr) {

for (let i \= 0; i < arr.length; i++) {

let lowest \= i;

for (let j \= i + 1; arr.length; j++) {

if (arr\[j\] < arr\[lowest\]) lowest \= j;

}

if (i !== lowest) {

var temp \= arr\[i\];

arr\[i\] \= arr\[lowest\];

arr\[lowest\] \= temp;

}

}

return arr;

}

  

selectionSort(\[34, 22, 10, 19, 17\]);

```