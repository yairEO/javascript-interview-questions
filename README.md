# List of Javascript fun Questions

Some are very basic programming questions that are designed to show how a person thinks.
<br><br><br>

### Remove overlapping matches in Array

Givven an array of numbers, and a size parameter, the `getNotOverlapping` is expected to return a 
new array with equal or less item, which their values do not overlap in accordance to the `size` variable.

```js
function getNotOverlapping(arr, size){  
}

console.log(
  getNotOverlapping([0,1,2,3], 1), // 0,1,2,3
  getNotOverlapping([0,1,2,3], 2)  // 0,2
)
```

<details>
<summary>See Answer</summary>
	
```js
[1, 2, 3, 4].reduce((acc, item, idx) =>  
idx === 0 || acc[acc.length-1] + size <= item ?
    [...acc, item]
    : acc, [])
```
</details>

---

### Create an array of N length and fill each item by it's index number
   https://itnext.io/heres-why-mapping-a-constructed-array-doesn-t-work-in-javascript-f1195138615a

<details>
<summary>See Answer</summary>
	
```js
[...new Array(5)].map((_, idx) => idx)
```
</details>

------

### Remove empty elements from Array

    [1,2,null,undefined,3,,"3",,NaN,0,,,true,false, {}]

<details>
<summary>See Answer</summary>
	
```js
.filter(Boolean)
```
</details>

------
### Make `Array.indexOf()` case insensitive

<details>
<summary>See Answer</summary>
	
```js
["Foo", "foO", "foo"].findIndex(item => item.toLowerCase() == 'foo')
```
</details>

------
### Find second largest number in an unsorted Array of numbers

<details>
<summary>See Answer</summary>
	
https://stackoverflow.com/a/17040125/104380
</details>

------
### Limit a number to be between 0 & 100 

<details>
<summary>See Answer</summary>
	
```js
Math.max(0, Math.min(100, num))
```
</details>

------
### Get the avarage of a number's digits

<details>
<summary>See Answer</summary>
	
https://stackoverflow.com/a/18234568/104380
	
```js
'1234'.split('').reduce((result, digit, idx, arr) => 
    idx == arr.length-1 
      ? (result+ +digit)/arr.length 
      : +result + +digit
, 0)
```
Or:

```js
let num = '12345';
let sum = 0

for( let d of num )
  sum += +d

console.log(sum/num.length) // 3
```
</details>


------
### Check if an array contains only numbers

<details>
<summary>See Answer</summary>
	
```js
![1,2,"3"].some(item => typeof item !== "number")
```
</details>

------
### Flip an integer (123 -> 321). suggest more than one solution.

https://stackoverflow.com/a/52366332/104380

------
### Sum two binary numbers (using as low-level code as possible)

    1011 + 11 // => 1110

https://stackoverflow.com/a/52372514/104380

------
### Split a paragraph into segments of max N characters, without word-breaking

------
### Check if a variable is an Object {}

------
### Create a function which executes once

------
### State different ways to define a function and their differences

------
### How to convert a DOM node list (HTMLCollection) into an array?

------
### Add only unique objects to an array

------
### Determine if two Objects are equal (identical to previous question, but more explicit)

------
### Remove DOM event listener which was added with callback which used ".bind()"

    function Example(name){
      this.name = name;
      window.addEventListener("click", this.clicked.bind(this))
    }
   
    Example.prototype.clicked = function(){
      console.log(this.name)
    }

    Example.prototype.destroy = function(){
      ...
    }
    
    const example = new Example('foo')

------
### Flatten multidimensional (2D) Array
 
    var arr = [[1,2],[3,4],[5,6]]
    console.log( [].concat(...arr) )

    // ES2015 "flat":
    arr.flat(); 

------
### Check how many times each digit in a number repeats itself

    1201977 => [[1,2],[2,1],[0,1],[9,1],[7,2]]

------
### Check number for duplicate digits

    [1, 10, 11, 1010, 1981] => [false, false, true, true, true]

------
### What would be the output of this?

    [1,2] + [3,4]
	
### Repeat a String N times

------
### Arguments vs Parameters, which term means what

------
### Check if character is number
https://stackoverflow.com/questions/8935632/check-if-character-is-number/32572539#32572539

------
### Enhance console.log function to print your name before, and as part of, the rest of the log

------
### What would these print:

        var foo = (...a) => console.log(a);
        foo([1,2,3], 4)

        var foo = (...[a]) => console.log(a);
        foo([1,2,3], 4)

------		
### For N arrays of varrying length in a 2D array, get the longest array's index
https://stackoverflow.com/a/57491707/104380
    

------		
### Write a function which finds a DOM node's index within its parent node

------		
### Deep-clone the Array & remove the 2nd item

	[{a:1}, {b:2}, {c:3}].reduce((newArr, item, idx) => {
	    if( idx != 1 )
		newArr.push({...item})
	    return newArr
	}, [])
