### What I Learned in Week 7



Mapping - Array will be same length but change by some process. 

The problem with changing arrays is that there would be no record of the original.

`for` loops 

- all of the loop information is at the beginning which prevents infinite loops.  The loop also doesn't change the actual array.  Every time you run it, it is a new `i`.

```javascript 
for (let i =0; i < arr.length; i ++) {
    console.log(arr[i] * 2);
}
```
****

String Building Exercises

Since strings are immutable there are other techniques that allow you to alter the content for the purposes of a function.

Example:
```javascript
function crazyCase(str) {
  let newStr = '';

  for (let i = 0; i < str.length; i++) {
    if (i % 2 === 1) {
      
      newStr = newStr + str[i].toUpperCase();
    } else {
      newStr = newStr + str[i].toLowerCase();
    }
  }
    return newStr;
  }
  ```

****

**Slice**
*Never use splice*
Slice will take out a designated segment from a string. 
slice(`beginning`,`end`(exclusive) ) 
so slice(1, 6) would start at index of 1 and end at 5 (up to 6)

What `slice` is doing behind the scenes.

```javascript
function slice(str, start = 0, end = str.length) {
  let newStr = '';

  for (let i = start; i < end; i++) {
    
      newStr = newStr + str[i];
    } 
    return newStr;
  }
  ```

  **Array manipulation**
  This is an important use of functions.  We don not want to change the original data but still have the ability to change what is inside.  Through functions we can accomplish this.