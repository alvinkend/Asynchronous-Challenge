# Ringkasan Materi

# ECMASCRIPT6

Sebuah standarisasi scripting language (Javascript) yang dibuat oleh European Computer Manufacturers Association (ECMA), ES6 adalah sebuah singkatan dari ECMAScript versi 6. 
ES6 diluncurkan pada tahun 2015, jadi ES6 sama dengan ES 2015. Pada ES6 ini terdapat banyak perubahan pada JavaScript yang semakin memudahkan programmer JavaScript.

### variabel

Constant pada JavaScript bisa dipakai sejak ES6 dengan menggunakan `const` dan untuk mutable variabel bisa menggunakan `let` let dan var : fungsi dari let dan var sebenarnya sama untuk mendeklarasikan variabel yang nilainya dapat diubah. Namun perbedaanya adalah var mempunyai cakupan dalam sebuah fungsi (function scope) dan let mempunyai cakupan dalam sebuah block (block scope). 

```
const a = 10
a = 11 		//Tidak bisa diassign
let b = 10
b = 11		 //Value b berubah
```

### Arrow Function

Penyederhanaan penulisan sebuah function pada JavaScript dengan menggunakan panah `=>`.
```
const a = () => console.log(“a”)
const b = (x, y) => x + y
const c = (x, y, z) => {
	return x + y * z
```

### For Loop

Perulangan pada array di JavaScript dipermudah dengan menggunakan For of.
```
const array = ['a', 'b', 'c'];
for (const element of array) {
console.log(element);
}
```

### Array.fill()

Pengisian value pada elemen JavaScript dipermudah dengan menggunakan property fill().

```
const array1 = [1, 2, 3, 4]
console.log(array1.fill(0, 2, 4)) 	 // expected output: [1, 2, 0, 0]
console.log(array1.fill(5, 1)) 		// expected output: [1, 5, 5, 5]
console.log(array1.fill(6))		// expected output: [6, 6, 6, 6]
```

### Array.find() and Array.findIndex()

Mencari elemen pertama (Array.find()) atau index pertama (Array.findIndex())  yang memenuhi kriteria yang diharapkan pada Array JavaScript.

```
const array = [5, 12, 8, 130, 44]
const found = array.find(it => it > 10) 			//`Elemen 12`
const find = array.findIndex(it => it > 10) 			//`Index ke 1
```

### Untuk lebih lengkapnya kunjungi fitur yang ada di ES6 pada link: http://es6-features.org/



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

### array.forEach(), .reduce(), .map()

Operasi untuk me-return value

```
forEach()
fruits.forEach(function (item, index, array) {
  console.log(item, index);
});
// Apple 0
// Banana 1

reduce()
const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

map()
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

# Object

Objek sebenarnya adalah sebuah variabel yang menyimpan nilai (properti) dan fungsi (method).

### Membuat Object

```
var car = {
    // properti
    type: "Fiat", 
    model: "500", 
    color: "white",
 ```
 
## Object operation
 
operasi pada object
 
### Object.assign
 
 Menyalin semua properti object ke dalam object target, jika ada key yang sama maka akan mengubah value dari key tersebut.

```
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };

const returnedTarget = Object.assign(target, source);

console.log(target);
// expected output: Object { a: 1, b: 4, c: 5 }

console.log(returnedTarget);
// expected output: Object { a: 1, b: 4, c: 5 }
 ```
 
### Object.entries
 
Mengembalikkan sebuah array yang setiap element berupa array dengan ukuran 2, dimana index pertama sebagai array dan index kedua berupa value

```
const object1 = {
  a: 'somestring',
  b: 42
};

for (let [key, value] of Object.entries(object1)) {
  console.log(`${key}: ${value}`);
}

// expected output:
// "a: somestring"
// "b: 42"
// order is not guaranteed
 ```

### Object.from.entries
 
Mengembalikkan sebuah object dari Array, dimana setiap element hanya mempunyai dua ukuran, index pertama sebagai key dan index kedua sebagai value.

```
const entries = new Map([
  ['foo', 'bar'],
  ['baz', 42]
]);

const obj = Object.fromEntries(entries);

console.log(obj);
// expected output: Object { foo: "bar", baz: 42 }
 ```
 
## Object.keys() and Object.values()
 
Mengembalikan sebuah array yang beranggotakan key/value dari sebuah object
 
```
Object.keys()
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.keys(object1));
// expected output: Array ["a", "b", "c"]

Object.values()
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.values(object1));
// expected output: Array ["somestring", 42, false]
 ```
 
## Object.freeze()
 
Membekukan nilai pada object, supaya tidak dapat diubah
 
```
const obj = {
  prop: 42
};

Object.freeze(obj);

obj.prop = 33;
// Throws an error in strict mode

console.log(obj.prop);
// expected output: 42
 ```
 
# Asynchronous

Asynchronous hasil eksekusi atau output tidak selalu berdasarkan urutan kode, tetapi berdasarkan waktu proses. Eksekusi dengan asynchronous tidak akan membloking atau menunggu suatu perintah sampai selesai. Daripada menunggu, asynchronous akan mengeksekusi perintah selanjutnya.


### callback

Callback sebenarnya adalah function bedanya dengan function pada umumnya adalah di cara eksekusinya. Jika function pada umumnya di eksekusi berurutan dari atas ke bawah maka callback di eksekusi pada point tertentu, itu sebabnya di sebut callback.

```
function main(param1,param2,callBack){ 
  console.log(param1, param2) 
  callBack()  
}

function myCallback(){ 
  console.log ('hello callback')
}

main(1,2,myCallback)

/* ===================
Output :
 1 2
 hello callback
 */
```

### Promises

Promise umumnya digunakan sebagai alternative callback. Salah satu tantangan di callback adalah callback hell. Disebut neraka ketika ada callback didalam callback didalam callback lagi dan di dalam callback lagi. Problemnya adalah kode sulit dibaca dan penanganan error nya juga menjadi sulit.

##### Promises method
1. Beberapa static method yang bisa dipakai didalam Promise.
2. Promise.all([promise1, promise2])
3. Promise.race([promise1, promise2])
4. Promise.resolve(value)
5. Promise.reject(value)

##### Promises method
1. then()
2. catch()
3. finally()


```
new Promises((resolve, reject)=> {
  const number = Math.floor((Math.random() * 10 ) + 1)
  setTimeout(() => {
      resolve(number)
  }, 1000)
})
.then(x => % 2 === 0? "Genap" : "Ganjil")
.then(x => console.log(x))
.catch(error => console.log(error))
```

##### Async/await

Async/await adalah fitur yang hadir sejak ES2017. Fitur ini mempermudah kita dalam menangani proses asynchronous. 

Keterangan :
async → mengubah function menjadi asynchronous
await → menunda eksekusi hingga proses asynchronous selesai, dari kode di atas berarti console.log(result) tidak akan di eksekusi sebelum prose doAsync( ) selesai. await juga bisa digunakan berkali-kali di dalam function


```
async function showAvatar() {

  // read our JSON
  let response = await fetch('/article/promise-chaining/user.json');
  let user = await response.json();

  // read github user
  let githubResponse = await fetch(`https://api.github.com/users/${user.name}`);
  let githubUser = await githubResponse.json();

  // show the avatar
  let img = document.createElement('img');
  img.src = githubUser.avatar_url;
  img.className = "promise-avatar-example";
  document.body.append(img);

  // wait 3 seconds
  await new Promise((resolve, reject) => setTimeout(resolve, 3000));

  img.remove();

  return githubUser;
}

showAvatar();
```
