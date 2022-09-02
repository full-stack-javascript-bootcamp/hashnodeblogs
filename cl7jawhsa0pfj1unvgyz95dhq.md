## JavaScript - Array

# What is array?

An array is an object that can store multiple values at once. 

# What is the difference between non-constant array and const array variable?

Non-const array variable can initialize with whole new array
also we can change the values.

```
let myarray = new Array();
myarray.push('value'); // Allowed
myarray = new Array(); // Allowed
```

Const array variable cannot be initialize again after declaration, only initilize at the time of declaration but we can change the values;

```
const myarray = new Array();
myarray.push('value'); // Allowed
myarray = new Array(); // It will throw exception
```

# Different ways to create array 

1. Using Array literal

``` 
let students = ['Ram', 'Sham', 'Gagan']; //Array with values
let studentsEmpty = []; //Empty array

// Objects array
let objArray = [
    {
        name: 'Rohit',
        age: '27'
    },
    {
        marks: 99,
        result: 'pass'
    }
];

```
2. Using New keyword
```
let students = new Array();
```
3. Using Array constructor
```
let students = new Array('Ram', 'Sham', 'Gagan');
```
# Array Methods 

| Method | Description |
| ----------- | ----------- |
| [concat()](##concat()) | It returns a new array object that contains two or more merged arrays. |
| [copywithin()](##copywithin()) | It copies the part of the given array with its own elements and returns the modified array. |
|[entries()](##entries()) | It creates an iterator object and a loop that iterates over each key/value pair.|
|[every()](##every()) | It determines whether all the elements of an array are satisfying the provided function conditions.|
|[flat()](##flat()) | It creates a new array carrying sub-array elements concatenated recursively till the specified depth.|
|[flatMap()](##flatMap()) |It maps all array elements via mapping function, then flattens the result into a new array. |
|[fill()](##fill()) | It fills elements into an array with static values.|
|[from()](##from()) | It creates a new array carrying the exact copy of another array element.|
|[filter()](##filter()) | It returns the new array containing the elements that pass the provided function conditions.|
|[find()](##find()) |It returns the value of the first element in the given array that satisfies the specified condition. |
|[findIndex()](##findIndex()) |It returns the index value of the first element in the given array that satisfies the specified condition. |
|[forEach()](##forEach()) | It invokes the provided function once for each element of an array.|
|[includes()](##includes()) | It checks whether the given array contains the specified element.|
|[indexOf()](##indexOf()) | It searches the specified element in the given array and returns the index of the first match.|
|[isArray()](##isArray()) | It tests if the passed value ia an array.|
|[join()](##join()) |It joins the elements of an array as a string. |
|[keys()](##keys()) | It creates an iterator object that contains only the keys of the array, then loops through these keys.|
|[lastIndexOf()](##lastIndexOf()) |It searches the specified element in the given array and returns the index of the last match. |
|[map()](##map()) |It calls the specified function for every array element and returns the new array |
|[of()](##of()) | It creates a new array from a variable number of arguments, holding any type of argument.|
|[pop()](##pop()) | It removes and returns the last element of an array.|
|[push()](##push()) | It adds one or more elements to the end of an array.|
|[reverse()](##reverse()) |It reverses the elements of given array. |
|[some()](##some()) | It determines if any element of the array passes the test of the implemented function.|
|[shift()](##shift()) | It removes and returns the first element of an array.|
|[slice()](##slice()) |It returns a new array containing the copy of the part of the given array. |
|[sort()](##sort()) | It returns the element of the given array in a sorted order.|
|[splice()](##splice()) |It add/remove elements to/from the given array. |
|[toLocaleString()](##toLocaleString()) |It returns a string containing all the elements of a specified array. |
|[toString()](##toString()) |It converts the elements of a specified array into string form, without affecting the original array. |
|[unshift()](##unshift()) | It adds one or more elements in the beginning of the given array.|
|[values()](##values()) |It creates a new iterator object carrying values for each index in the array. |

<!-- |[reduce(function, initial)](##reduce(function, initial)) | It executes a provided function for each value from left to right and reduces the array to a single value.|
|[reduceRight()](##reduceRight()) |It executes a provided function for each value from right to left and reduces the array to a single value. | -->


## concat()
The concat() method is use to append the another array to current array 
```
let students1 = ['Ram', 'Sham'];
let students2 = ['Sadan', 'Mahatre'];

// contact two arrays 
let concatStudents = students1.concat(students2);

console.info(concatStudents);
//output:: [Ram,Sham,Sadan,Mahatre]

concatStudents = students2.concat(students1);

console.info(concatStudents);
//output:: [Sadan,Mahatre,Ram,Sham]

console.info(['Sham', 'Ganga'].concat(['Radha', 'Maya']));
//output:: ['Sham', 'Ganga', 'Radha', 'Maya']
```
## copywithin()
Syntax

    ```
    array.copyWithin(target, start, end)
    ```
Parameters
- target - The position where the copied element takes place.
- start - It is optional. It represents the index from where the method starts copying elements. By default, it is 0.
- end - It is optional. It represents the index at which elements stops copying. By default, it is array.length-1.

Example
```
let studentsArray = ['rohit', 'sagar', 'kamala'];
let result = studentsArray.copyWithin(0,1,2);

console.info(result);
//output: ['sagar', 'sagar', 'kamala']
```
## entries()
The entries() method creates a new iterator object of an array, holding the key/value pairs for every value in the array. A key represents the index number carrying an item as its value. It does not affect the original array.


Example 1
```
let colors = ['yellow', 'green', 'orange', 'black'];
newColors = colors.entries();

for(let color of newColors){
    console.info(color);
}
```
output 
```
[0, 'yellow']
[1, 'green']
[2, 'orange']
[3, 'black']
```
Example 2
```
let colors = ['yellow', 'green', 'orange', 'black'];

let newColors = colors.entries();

for(let color of newColors){
    color.forEach((element) => {
        console.info(element);
    });
}
```
output
```
0
yellow
1
green
2
orange
3
black

```

<!-- ## every()
## flat()
## flatMap()
## fill()
## from()
## filter()
## find()
## findIndex()
## forEach()
## includes()
## indexOf()
## isArray()
## join()
## keys()
## lastIndexOf()
## map()
## of() -->
## pop()
Get last element and remove from the array
```
let colors = ['red', 'yellow', 'green'];

console.log(colors.pop());

//output: green

console.log(colors);
//output: ['red', 'yellow']
```
## push()
Add new element at the end of the array
```
let colors = ['red', 'yellow', 'green'];

colors.push('black');

console.log(colors);
//output: ['red', 'yellow', 'green', 'black']
```
## reverse()
To reverse elements order of the array
```
let colors = ['red', 'yellow', 'green'];

colors.reverse();

console.log(colors);
//output: ['green', 'yellow', 'red']
```
<!-- ## reduce(function, initial)
## reduceRight()
## some() -->
## shift()
The JavaScript array shift() method removes the first element of the given array and returns that element. This method changes the length of the original array.
```
let colors = ['red', 'yellow', 'green'];

let color = colors.shift();

console.log(color);
//output: red

console.log(colors);
//output: ['yellow', 'green']
```
## slice()
The JavaScript array slice() method extracts the part of the given array and returns it. This method doesn't change the original array.
```
let colors = ['red', 'yellow', 'green'];

let colorsSlice = colors.slice(1,3);

console.log(colorsSlice);
//output: ['yellow', 'green']
```
## sort()
Sort method arrange elements in sorted order
```
let colors = ['red', 'yellow', 'green'];

let sortedColors = colors.sort();

console.log(sortedColors);
//output: ['green', 'red', 'yellow']

console.log(colors)
//output: ['green', 'red', 'yellow']
```
<!-- ## splice()
## toLocaleString() -->
## toString()
Converts array into command seprated string 
```
let colors = ['red', 'yellow', 'green'];

console.log(colors.toString());

//output: red,yellow,green
```
## unshift()
The JavaScript array unshift() method adds one or more elements in the beginning of the given array and returns the updated array. This method changes the length of the original array.
```
let colors = ['red', 'yellow', 'green'];

let count = colors.unshift('black')

console.log(colors);
//output: ['green', 'red', 'yellow']

console.log(count);
//output: 4
```
<!-- ## values() -->


