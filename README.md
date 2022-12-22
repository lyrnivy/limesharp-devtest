# Limesharp Developer Test

Please, **don't fork this repo**, clone it or download it locally and then commit changes after each task into a new repo of your own, and send us the link. We will get back to you shortly. 

Languages accepted: Javascript or PHP. 

### Task 1: 
Make this work (repeat 3 times the contents of an array):
```javascript
repeat([1,2,3]) //[1,2,3,1,2,3,1,2,3]
```
Your solution:

```

console.log (
Array(3).fill([1,2,3]).flat()
)

Result:
https://codepen.io/lyrnivy-the-scripter/pen/poZJExG
// [object Array] (9)
[1,2,3,1,2,3,1,2,3]

```

###### If we type in our console your function and repeat([1,2,3]) then the result should be [1,2,3,1,2,3,1,2,3] 

### Task 2:
Make this work (no vowels, lowercase except the first letter):
```javascript
reformat("liMeSHArp DeveLoper TEST") //Lmshrp dvlpr tst
```
Your solution:
Html and javascript

```
//get the element Id which is task2 to show result in html
<p id="task2"></p>

<script>

let text = "liMeSHArp DeveLoper TEST";
let firstLetter = text[0].toUpperCase(); //get first letter and convert to UPPERCASE
let result = firstLetter + text.toLowerCase().slice(2); //combine UPPERCASE letter with sliced lowercase text

document.getElementById("task2").innerHTML = result.replace(/[aeiou]/gi, ''); //return result with no vowels

</script>

Result:
https://codepen.io/lyrnivy-the-scripter/pen/rNrVLYd
Lmshrp dvlpr tst

```

###### If we type in our console your function and reformat("liMeSHArp DeveLoper TEST") then the result should be Lmshrp dvlpr tst


### Task 3 (optional, for bonus points):
Make this work (without using any built in functions, only a `for` loop, return the next binary number in a string or as an array)
```javascript
next_binary_number([1,0]) // [1,1]

// possible test cases:
// [1,0] => [1,1]
// [1,1] => [1,0,0]
// [1,1,0] => [1,1,1]
// .......
// [1,0,0,0,0,0,0,0,0,1] => [1,0,0,0,0,0,0,0,1,0]
```

```
Your solution:

function nextBinaryNumber(binary) {
  // Find the first bit that is 0, starting from the least significant bit
  for (var i = 0; i < binary.length; i++) {
    if (binary[i] === 0) {
      // Set that bit to 1
      binary[i] = 1;
      break;
    }
  }
  // If no 0s were found, add a 1 at the end of the array
  if (i === binary.length) {
    binary.push(1);
  }

  // Set all the bits to the right of the changed bit to 0
  for (let j = i + 1; j < binary.length; j++) {
    binary[j] = 0;
  }
  return binary;
}

console.log(nextBinaryNumber([1, 0]));  // prints [1, 1]

Results:
https://codepen.io/lyrnivy-the-scripter/pen/rNrVMbN
// [object Array] (2)
[1,1]

```

###### If we type in our console your function and next_binary_number([1,0,0,0,0,0,0,0,0,1]) then the result should look like 1,0,0,0,0,0,0,0,1,0 (or as an array).

---

If you get invited to the first interview read the "What to expect.md" file.