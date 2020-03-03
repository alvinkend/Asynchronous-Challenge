# Ringkasan Materi

# Function

Function merupakan sebuah code block yang digunakan untuk melakukan tugas tertentu, pada JavaScript mendeklarasikan function bisa dengan menggunakan keyword ‘function’, parentheses ‘( )’ dan curly bracket ‘{ do magic here }’.

### Function Declarations
Function declarations atau yang dikenal juga sebagai function statements adalah fungsi yang telah dideklarasikan sebelumnya dan akan dieksekusi jika dipanggil (call).

```
foo(); //akan mengeluarkan alert "hello".
function foo() {
  alert("hello");
}
```

### Function Expressions
Function expressions adalah fungsi yang disimpan ke dalam suatu variable. Setelah disimpan, maka variabel tersebut dapat digunakan sebagai fungsi.

```
var baz = function() {
  alert("hello");
}
```

### Arrow Function
Mendeklarasikan sebuah expression function dengan menggunakan panah ( => ) hal ini untuk mempersingkat dalam membuat function.

```
const func2 = (a, b) => {
  return a + b;
}
```


# Array

Array adalah tipe data yang berisi kumpulan dari nilai atau tipe data lain. Nilai di dalam array disebut dengan elemen, dan setiap elemen memiliki ‘nomor urut’ yang dikenal dengan istilah index.e

### Spread Operator

Spread operator adalah operator yang digunakan menyebarkan array baik ke dalam function ataupun ke dalam object atau array.

```
const array = [1, 2, 3]
const list = [4, 5, 6]
console.log([...array, ...list]) // [1, 2, 3, 4, 5, 6]
console.log([...list, ...array]) // [4, 5, 6, 1, 2, 3]
```

### Spread Operator in Parameter

Spread operator bisa dilakukan ke dalam sebuah function yang memiliki parameter

```
const array = [1, 2, 3, 4]
const fun = (a, b, c) => console.log(a*b*c)

fun(...array) // Element 4 igored
fun(...[1, 2]) // Output NaN
```

## Array Operation

Operasi yang bisa dilakukan terhadap array

### array.sort

mengurutkan isi array

```
const months = ['March', 'Jan', 'Feb', 'Dec'];
months.sort();
console.log(months);
// expected output: Array ["Dec", "Feb", "Jan", "March"]
```

### array.push, .pop(), .shift, .unshift, .indexOf, .splice()

```
push()
var newLength = fruits.push("Orange");
// ["Apple", "Banana", "Orange"]

pop()
var last = fruits.pop(); // remove Orange (from the end)
// ["Apple", "Banana"];

shift()
var first = fruits.shift(); // remove Apple from the front
// ["Banana"];

unshift()
var newLength = fruits.unshift("Strawberry") // add to the front
// ["Strawberry", "Banana"];

indexOf()
fruits.push("Mango");
// ["Strawberry", "Banana", "Mango"]

var pos = fruits.indexOf("Banana");
// 1

splice()
var removedItem = fruits.splice(pos, 1); // this is how to remove an item
// ["Strawberry", "Mango"]
```

### array.find(), array.filter()

Operasi untuk menyaring sebuah array.

```
find()
const array1 = [5, 12, 8, 130, 44];

const found = array1.find(element => element > 10);

console.log(found);
// expected output: 12

filter()
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

