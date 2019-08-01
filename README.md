# My Codewars sold katas.

---
## The last tasks from Julia's 'Easy tasks list'
https://docs.google.com/spreadsheets/d/1bFV_GfN4Rg5HB5z_IgXgYRRiK2FD9v62jUm5eLt1-Fs/edit#gid=0


### Return the day
https://www.codewars.com/kata/59dd3ccdded72fc78b000b25
```javascript
function seatsInTheater(nCols, nRows, col, row) {
  let x =  nCols - col + 1;
  let y = nRows - row;
  return x * y;
}
```

### Remove exclamation marks
https://www.codewars.com/kata/remove-exclamation-marks
```javascript
function removeExclamationMarks(s) {
  return s.replace(/!/g, '');
}
```

### Reverse List Order
https://www.codewars.com/kata/reverse-list-order
```javascript
 function reverseList(list) {
  return list.reverse();
 }
```

### You Can't Code Under Pressure #1
https://www.codewars.com/kata/you-cant-code-under-pressure-number-1
```javascript
function doubleInteger(i) {
   return i * 2;
}
```
---

---

## Tasks from Victor's list + others )
https://github.com/bogutski/js-road-map/blob/master/tasks.md

---
##1. Initial level

### Convert a string to an array
https://www.codewars.com/kata/convert-a-string-to-an-array/train/javascript
```javascript
function stringToArray(string){
  return string.split(' ');
}
```

### Determine offspring sex based on genes XX and XY chromosomes
https://www.codewars.com/kata/determine-offspring-sex-based-on-genes-xx-and-xy-chromosomes/javascript
```javascript
function chromosomeCheck(sperm) {
  if(sperm.includes('Y') === true) return "Congratulations! You're going to have a son.";
  else return "Congratulations! You're going to have a daughter.";
}
```

### Thinkful - Logic Drills: Traffic light
https://www.codewars.com/kata/thinkful-logic-drills-traffic-light/javascript
```javascript
function updateLight(current) {
  let lights = ['green', 'yellow', 'red'];
  if(current === lights[0]) return lights[1];
  if(current === lights[1]) return lights[2];
  if(current === lights[2]) return lights[0];
}
```

### Sleigh Authentication
https://www.codewars.com/kata/52adc142b2651f25a8000643
```javascript
function Sleigh() {}

Sleigh.prototype.authenticate = function(name, password) {
  if(name === 'Santa Claus' && password === 'Ho Ho Ho!') return true;
  else return false;
}
```
---
##2. Strings

### Random case
https://www.codewars.com/kata/random-case/train/javascript

Нужна помощь

### Credit card issuer checking
https://www.codewars.com/kata/5701e43f86306a615c001868
```javascript
function getIssuer(n) {
   let str = n.toString(10);
   console.log(typeof n);
   console.log(str);
   console.log(str.length);
   if(str[0] === '3' && str.length === 15) return 'AMEX';
   if(str[0] === '6' && str[1] === '0' && str[2] === '1' && str[3] === '1' && str.length === 16) return 'Discover';
   if(str[0] === '5' && str[1] >= '1' && str[1] <= '5' && str.length === 16) return 'Mastercard';  
   if(str[0] === '4' && (str.length === 13 || str.length === 16)) return 'VISA'; 
   else return 'Unknown';
}
```
### Multiples of 3 or 5
https://www.codewars.com/kata/multiples-of-3-or-5/train/javascript
```javascript
function solution(number){
  let sum = 0;
  for (let i = 1; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
}
```

### Mumbling
https://www.codewars.com/kata/mumbling/train/javascript
```javascript
function accum(s) {
  let arr = s.split('');
  let accArr = [];
  let accStr = '';
  
  for(let i = 0; i < arr.length; i++){
    accArr.push(arr[i].toUpperCase() + arr[i].toLowerCase().repeat(i));
  }
  accStr = accArr.join('-');
 return accStr;
}
```

### Get list sum recursively
https://www.codewars.com/kata/get-list-sum-recursively/train/javascript
```javascript
function sumR(x) {

  if(x.length === 0) {
    return 0;
   }  else {
  return x.shift() + sumR(x);
  }
}
```

### Remove duplicates from list
https://www.codewars.com/kata/remove-duplicates-from-list/train/javascript
```javascript
function distinct(a) {
let newA = [];
 
    for(let i=0; i < a.length; i++){
      if(a[i] != a[i + 1]){
        newA.push(a[i]);
      }
    }
  return newA;
}
```

### Numerical Palindrome #1
https://www.codewars.com/kata/numerical-palindrome-number-1/train/javascript
```javascript
function palindrome(num) { 
  if(typeof num !== 'number' || num < 0){
      return 'Not valid';
  }
  
  let numToArr = num.toString().split('');
  const med = Math.floor(numToArr.length / 2);
  
  for(let i = 0; i <= med; i++){
      if(numToArr[i] !== numToArr[numToArr.length - 1 - i]){
          return false;
      }
  }
  return true;
  
} 
```

### Find the calculation type
https://www.codewars.com/kata/find-the-calculation-type/train/javascript
```javascript
function calcType(a, b, res) {
  const operation = ['addition', 'subtraction', 'multiplication', 'division'];
  if(res === a + b) return operation[0];
  else if(res === a - b) return operation[1];
  else if(res === a * b) return operation[2];
  else if(res === a / b) return operation[3];
}
```

### Simple beads count
https://www.codewars.com/kata/simple-beads-count/train/javascript
```javascript
function countRedBeads(n) {
  if(n < 2) return 0;
  else return (n - 1) * 2;
}
```

### Reverse a Number
https://www.codewars.com/kata/reverse-a-number/train/javascript
```javascript
function reverseNumber(n) {
  let nRev;
  if(n >= 0){
    nRev = +(n.toString().split('').reverse().join(''));
    return nRev;
  } else 
  if(n < 0){
    n = n * (-1);
    nRev = +(n.toString().split('').reverse().join(''));
    return nRev * -1;
  }
} 
```

## !String average
https://www.codewars.com/kata/string-average/train/javascript
I could'n made it by myself and had to watch Victor' video. But I tried to do the same 2 weeks ago - and I understood nothing then.
```javascript
function averageString(str) {
   
  const d = {'zero':0, 'one':1, 'two':2, 'three':3, 'four':4, 'five':5, 'six':6, 'seven':7, 'eight':8, 'nine':9,};
  const n ={0:'zero', 1:'one', 2:'two', 3:'three', 4:'four', 5:'five', 6:'six', 7:'seven', 8:'eight', 9:'nine',};
 
  if(!str) return 'n/a';
  
  let da = str.split(' ');
  let sum = 0;
  
  for(let i = 0; i < da.length; i++){
    if(d[da[i]] !==undefined){
     sum += d[da[i]];
    } else return 'n/a';
  }
  
  const avg = Math.floor(sum / da.length);
  return n[avg];
}
```
### New solution after 400
### Sentence Smash
https://www.codewars.com/kata/sentence-smash/train/javascript
```javascript
function smash (words) {
    return words.join(' ');
};
```
### Reversing Words in a String
https://www.codewars.com/kata/reversing-words-in-a-string/train/javascript
```javascript
function reverse(string){
   return string.split(' ').reverse().join(' ');
 }
```
### Filter out the geese
!!! I have to repeat it
https://www.codewars.com/kata/filter-out-the-geese/javascript
```javascript
function gooseFilter (birds) {
  const geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  
  return birds.filter(item => !geese.includes(item)); 
}
```
### No Loops 2 - You only need one
https://www.codewars.com/kata/no-loops-2-you-only-need-one/train/javascript
```javascript
function check(a,x){
  return a.includes(x);
}
```
### Will there be enough space?
https://www.codewars.com/kata/will-there-be-enough-space/javascript
```javascript
function enough(cap, on, wait) {
   let room = ((on + wait) - cap);
   return room < 0 ? 0 : room;
 }
```

### Enumerable Magic #25 - Take the First N Elements
https://www.codewars.com/kata/enumerable-magic-number-25-take-the-first-n-elements/javascript
```javascript
const take = (arr, n) => arr.slice(0, n);
```
### Sum of differences in array
https://www.codewars.com/kata/5b73fe9fb3d9776fbf00009e
```javascript
function sumOfDifferences(arr) {
  if(arr.length <= 1) return 0;
  
  const sortArr = arr.sort((a, b) => b - a);
  let sum = 0;
  
  for(let i = 1; i < sortArr.length; i++){
    sum += sortArr[i - 1] - sortArr[i];
  }
  return sum;
}
```
### Clean up after your dog
https://www.codewars.com/kata/clean-up-after-your-dog/train/javascript
```javascript
function crap(x, bags, cap){
  let str = x.toString();
  if(str.includes('D')) return 'Dog!!';
  let count = str.split('@').length - 1;
  if(bags * cap >= count) return 'Clean';
  else return 'Cr@p';
}
```

### Grasshopper - Personalized Message
https://www.codewars.com/kata/grasshopper-personalized-message
```javascript
const greet = (name, owner) => 'Hello ' + (name === owner ? 'boss' : 'guest');
```

### Lario and Muigi Pipe Problem
https://www.codewars.com/kata/lario-and-muigi-pipe-problem
```javascript
function pipeFix(numbers){
  let arr = [];
  for(let i = numbers[0]; i <= numbers[numbers.length - 1]; i++){
    arr.push(i);
  }
  return arr;
}
```
### Random case
https://www.codewars.com/kata/random-case/
```javascript
function randomCase(x) {
let xStr = '';
  for(let i = 0; i < x.length; i++){
    if(Math.round(Math.random()) > 0){
      xStr += x[i].toUpperCase();
    } else {
      xStr += x[i].toLowerCase();
    }
  }
  return xStr;
}
```

### Alphabet symmetry
https://www.codewars.com/kata/alphabet-symmetry
```javascript
function solve(arr){  
  let alp = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  let arrN = [];
  
  for(let i = 0; i < arr.length; i++){
    let count = 0;
    for(let j = 0; j< arr[i].length; j++){
      if(j === alp.indexOf(arr[i][j].toUpperCase())){
        count++;
      }
    }
    arrN.push(count)
  }
  return arrN;
};
```
### Can we divide it?
https://www.codewars.com/kata/can-we-divide-it/javascript
```javascript
function isDivideBy(number, a, b) {
  return number % a === 0 && number % b ===0;
}
```

### Count Odd Numbers below n
https://www.codewars.com/kata/59342039eb450e39970000a6
```javascript
function oddCount(n){
  return Math.floor(n / 2);
}
```
### Difference of Volumes of Cuboids
https://www.codewars.com/kata/58cb43f4256836ed95000f97
``javascript
function findDifference(a, b) {
  let vol1 =a[0] * a[1] * a[2];
  let vol2 =b[0] * b[1] * b[2];
  return Math.abs(vol1 - vol2);
}
``
### Sum Mixed Array
https://www.codewars.com/kata/sum-mixed-array/
```javascript
function sumMix(x){
  let sum = 0;
  for(let i = 0; i < x.length; i++){
    sum += +x[i];
  }
  return sum;
}
```
### Sum of all the multiples of 3 or 5
https://www.codewars.com/kata/sum-of-all-the-multiples-of-3-or-5/
```javascript
function findSum(n) {
  let sum = 0;
  for(let i = 0; i <= n; i++){
    if(i % 3 === 0 || i % 5 === 0){
      sum += i;
    }
  }
  return sum;
}
```
### Do I get a bonus?
https://www.codewars.com/kata/do-i-get-a-bonus/
```javascript
function bonusTime(salary, bonus) {
  return  bonus ? `£${salary * 10}` : `£${salary}`
}
```

### String ends with?
https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d

```javascript
function solution(str, ending){
  return str.slice((str.length - ending.length)) === ending;
}
```
### sPoNgEbOb MeMe
https://www.codewars.com/kata/spongebob-meme/
```javascript
function spongeMeme(sentence) {
  let str = '';
  for(let i = 0; i < sentence.length; i++){
    if(i % 2 === 0){
      str += sentence[i].toUpperCase();
      } else {
      str += sentence[i].toLowerCase();
      }
  }    
  return str;
}
```
### Sort the odd
https://www.codewars.com/kata/sort-the-odd
```javascript
function sortArray(array) {
  const odd = [];
  const even = [];
  const end = [];
for (let i = 0; i < array.length; i++) {
    if (array[i]%2 === 0) {
      even.push(array[i]);
    } else {
      odd.push(array[i]);
    }
  }
  
  odd.sort((a, b) => a - b);
  
  for (let i = 0; i < array.length; i++) {
    if (array[i]%2 === 0) {
      end.push(even.shift());
    } else {
      end.push(odd.shift());
    }
  }
  return end;
}
```


### Double Char
https://www.codewars.com/kata/double-char
```javascript
function doubleChar(str) {
  let resStr = '';
  for(let i = 0; i < str.length; i++){
    resStr += str[i] + str[i];
  }
  return resStr;
}
```
### Fix string case
https://www.codewars.com/kata/fix-string-case/
```javascript
ffunction solve(s) {
   let countUC = 0; 
 	let countLC = 0; 
   
   for ( let i = 0; i < s.length; i++) {
       let letter = s[i];
       letter === letter.toUpperCase() ? countUC +=1 : countLC +=1;
   }
    
   if ( countUC > countLC) return s.toUpperCase()
   else  if ( countUC < countLC) return s.toLowerCase()
   else return s.toLowerCase();
 }
```

### Bit Counting 
Как уйти от цикла for в этой задаче???
https://www.codewars.com/kata/bit-counting
```javascript
let countBits = function(n) {
  let arrN = n.toString(2).split('');
  let result = 0;
  
  for(let i = 0; i < arrN.length; i++){
    let num = +(arrN[i]);
    result += num;
  }
   return result;
}
```

### Fake Binary
https://www.codewars.com/kata/fake-binary
```javascript
function fakeBin(x){
  let arr = x.split('');
  let arr01 = [];
  console.log(arr);
  for(let i = 0; i < arr.length; i++){
    if(arr[i] < 5){
      arr01.push(0);
    }
    if(arr[i] >= 5){
      arr01.push(1);
    }
  }
  return arr01.join('');
}
```
### Vowel Count
https://www.codewars.com/kata/vowel-count/
```javascript
function getCount(str) {  
  let vowelsCount = 0;
  const vowels = 'aeiou';
  
  for(let i = 0; i < str.length; i++){
    if(vowels.includes(str[i])){
      vowelsCount++;
    }
  }
  return vowelsCount;
}
```

### Vowel one
https://www.codewars.com/kata/vowel-one/
```javascript
function vowelOne(str){
  str = str.toLowerCase();
  const vowels = 'aeiou';
  let digStr = '';
  for(let i = 0; i < str.length; i++){
    vowels.includes(str[i]) ? digStr += '1': digStr += '0';
  }
  return digStr;
}
```
### Simple Pig Latin
https://www.codewars.com/kata/simple-pig-latin
```javascript
 function pigIt(str){
   let tagArr = [];
   let arr = str.split(' ');
   
   for(let i = 0; i < arr.length; i++){
      if(arr[i] !== '?' && arr[i] !== '!'){ 
         let item = arr[i].split('');
         item.splice(item.length, 0, item[0]);
         item.shift(0);
         item.push('a', 'y');
         let word = item.join('');
         tagArr.push(word);
       } else tagArr.push(arr[i]);
    }
    return tagArr.join(' ');
 }
```

### Rock Paper Scissors!
https://www.codewars.com/kata/rock-paper-scissors/
```javascript
const rps = (p1, p2) => {
  const getMsg = n => `Player ${n} won!`;
  
  if(p1 === 'scissors' && p2 === 'paper') return getMsg(1);
  if(p1 === 'paper' && p2 === 'scissors') return getMsg(2);
  
  if(p1 === 'paper' && p2 === 'rock') return getMsg(1);
  if(p1 === 'rock' && p2 === 'paper') return getMsg(2);
  
  if(p1 === 'rock' && p2 === 'scissors') return getMsg(1);
  if(p1 === 'scissors' && p2 === 'rock') return getMsg(2);
  
  if(p1 === p2) return 'Draw!';
};
```
### Find Maximum and Minimum Values of a List
https://www.codewars.com/kata/find-maximum-and-minimum-values-of-a-list/
```javascript
//var1
const min = list =>  Math.min(...list);
const max = list =>  Math.max(...list);
```
```javascript
//var2
const min = list =>  {
  let mn = list[0];
  for(let i = 1; i < list.length; i++){
    if(list[i] < mn) mn = list[i];
  }
  return mn;
}
const max = list =>  {
  let mx = list[0];
  for(let i = 1; i < list.length; i++){
    if(list[i] > mx) mx = list[i];
  }
  return mx;
}
```

### Sum without highest and lowest number
https://www.codewars.com/kata/sum-without-highest-and-lowest-number
```javascript
//var1
function sumArray(array) {
  if(!array || array.length < 2 ) return 0;
  let min = array[0], max = array[0], sum = 0 ;
  
  array.forEach(el => {
    if(el < min) min = el;
    if(el > max) max = el;
    sum += el;
  });
  return sum - min -max;
}
```
```javascript
//var2 - we safe 1 tact in the loop
unction sumArray(array) {
  if(!array || array.length < 2 ) return 0;
  let min = array[0], max = array[0], sum = array[0] ;
    
  for(let i = 1; i < array.length; i++){
    if(array[i] < min) min = array[i];
    if(array[i] > max) max = array[i];
    sum += array[i];
  }
  return sum - min -max;
}
```
### Is the string uppercase?
https://www.codewars.com/kata/is-the-string-uppercase/javascript
```javascript
/// Ask the questions here????
//define the string prototype here
String.prototype.isUpperCase = function(){
  return this.toUpperCase() === this.toString();
}
```

### Flatten and sort an array
https://www.codewars.com/kata/flatten-and-sort-an-array/
```Javascript
\\ repeat it !!!

function flattenAndSort(array) {
  let arRes = [];
  array.forEach(el =>{
    if(Number.isInteger(el)){
      arRes.push(el);
    } else if(Array.isArray(el) && el.length){
      arRes = [...arRes, ...el];
    }
  });
  return arRes.sort((a, b) => a - b);
  }
```

### Who likes it?
https://www.codewars.com/kata/who-likes-it/
```javascript
function likes(n) {
  const l = n.length;
  if(!l) return 'no one likes this';
  if(l === 1) return `${n[0]} likes this`;
  if(l === 2) return `${n[0]} and ${n[1]} like this`;
  if(l === 3) return `${n[0]}, ${n[1]} and ${n[2]} like this`;
  if(l > 3) return `${n[0]}, ${n[1]} and ${l - 2} others like this`;
}
```
### Sum of the first nth term of Series
https://www.codewars.com/kata/sum-of-the-first-nth-term-of-series/
```javascript
function SeriesSum(n){
  let sum = 0;
  for(let i = 0; i < n; i++){
    sum += 1/(i * 3 + 1);
  }
  return sum.toFixed(2);
}
```
### The Office III - Broken Photocopier
https://www.codewars.com/kata/the-office-iii-broken-photocopier/
```javascript
// v1
function broken(x){
    return x.replace(/[01]/g, (a) =>  a === '0' ? '1' : '0');
}
```
```javascript
//2 I like it moore! ;-)
function broken(x){
    let res = '';
    for(let i = 0; i < x.length; i++){
      res += x[i] === '0' ? '1' : '0';
    }
    return res;
}
```
### The Office IV - Find a Meeting Room
https://www.codewars.com/kata/the-office-iv-find-a-meeting-room/
```javascript
function meeting(x){
  return x.indexOf('O') > -1 ? x.indexOf('O') : 'None available!';
}
```
### The Office V - Find a Chair
ps://www.codewars.com/kata/the-office-v-find-a-chair/
```javascript
// repeat it again
function meeting(x, need){
if(!need) return 'Game On';
const r = [];
let rest = need;
for(let i = 0; i < x.length; i++){
  if(rest > 0){
    let c = x[i][1] - x[i][0].length;
    r.push(c > 0 ? (c > rest ? rest : c) : 0);
    if(c > 0) rest -= c;
  } else {
    return r;
  }
 }
 return rest <= 0 ? r : 'Not enough!';
}
```

### Merge two sorted arrays into one
https://www.codewars.com/kata/merge-two-sorted-arrays-into-one
```javascript
// NEED to optimise it
function mergeArrays(arr1, arr2) {
  
  const arr = [...arr1, ...arr2].sort((a,b) => a - b);
  const res = [];
  for (let i = 0; i < arr.length; i++){
    if(arr[i] !== arr[i + 1]) res.push(arr[i]);
  }
  return res;
}
```
### Remove duplicate words
https://www.codewars.com/kata/remove-duplicate-words/
```javascript
function removeDuplicateWords (s) {
 let arr = s.split(' ')
 arr = arr.filter((elem,index) => arr.indexOf(elem) == index);
return arr.join(' ')
}
```
### Get the mean of an array
https://www.codewars.com/kata/get-the-mean-of-an-array
```javascript
function getAverage(marks){
  let sum = marks.reduce((a, b) => a + b, 0);
  let avg = Math.floor(sum / marks.length);
  return avg; 
}
```
### Find the missing element between two arrays 
https://www.codewars.com/kata/5a5915b8d39ec5aa18000030
```javastring
function findMissing(arr1, arr2) {
  let a1 = arr1.sort((a,b) => a - b);
  let a2 = arr2.sort((a,b) => a - b);
  for(let i = 0; i < a1.length; i++){
    if(a1[i] !== a2[i]) return a1[i];
  }
}
```


### Are the numbers in order?
https://www.codewars.com/kata/are-the-numbers-in-order/
```javascript
function inAscOrder(arr) {
  let str = arr.join('')
  let sortStr = arr.sort((a,b) => a - b).join('');
  if(str === sortStr){
    return true
  } else return false ;
}
```

### Sort and Star
https://www.codewars.com/kata/sort-and-star/
```javascript
function twoSort(s) {
  s.sort();
  return word = s[0].split('').join('***');
```
### A Needle in the Haystack
https://www.codewars.com/kata/a-needle-in-the-haystack/
```javascript
function findNeedle(haystack) {
let ind = haystack.indexOf('needle');
return `found the needle at position ${ind}`
}
```
### Numerical Palindrome #5
https://www.codewars.com/kata/58e26b5d92d04c7a4f00020a/

```javascript
function palindrome(num) {
  if (typeof num !== 'number' || num < 0) return 'Not valid';
  let cnt = 0;
  let str = num.toString().split('').sort();
  if (str.length <= 1) return false;
  for (let i = 0; i < str.length - 1 ; i++) {
   if (str[i] === str[i + 1]) {
     cnt+=2;
     i++;
     }  
  }
  return (str.length - cnt) <= 1 ? true : false; 
}
```
### Minimize Sum Of Array (Array Series #1)
https://www.codewars.com/kata/5a523566b3bfa84c2e00010b
```javascript
function minSum(arr) {
  let cnt = 0;
  arr = arr.sort((a,b) => a - b);
  for(let i = 0; i < arr.length / 2; i++){
    cnt += arr[i] * arr[arr.length - 1 - i];
  }
  return cnt;
}
```
### Difference Of Squares
https://www.codewars.com/kata/difference-of-squares
```javascript
function differenceOfSquares(n){
  let sqrSum = 0;
  let sumSqr = 0;
  for(let i = 1; i <= n; i++){
    sqrSum += i;
    sumSqr += i * i;
  }
  return (sqrSum * sqrSum) - sumSqr;
}
```
### Century From Year
https://www.codewars.com/kata/century-from-year/
```javascript
unction century(year) {
    return Math.ceil(year/100);
}
```

### Check the exam
https://www.codewars.com/kata/check-the-exam/
```javascript
//var1
function checkExam(array1, array2) {
  console.log(array1, array2);
  let score = 0;
  for(let i = 0; i < array1.length; i++){
    if(array2[i] === '') score += 0;
    else if(array1[i] === array2[i]) score += 4;
    else  score -=1;
  }
   if(score < 0) return 0;
   return score
}
```
### Discover The Original Price
https://www.codewars.com/kata/discover-the-original-price/
```javascript
function discoverOriginalPrice(discountedPrice, salePercentage){
   let orPr = discountedPrice * 100 / (100 - salePercentage);
   return +orPr.toFixed(2);
}
```
### Find the divisors!
https://www.codewars.com/kata/find-the-divisors
```javascript
function divisors(integer) {
  let div = [];
  for(let i = 2; i < integer; i++){
    if(integer%i === 0) div.push(i);
  }
  if(div.length === 0) return `${integer} is prime`;
  return div;
};
```
### Sum of Odd Cubed Numbers
https://www.codewars.com/kata/sum-of-odd-cubed-numbers
```javascript
function cubeOdd(arr) {
let result = 0;
let cube = arr.map(item => Math.pow(item, 3));
if(cube.includes(NaN)) return undefined;
for(let i = 0; i < cube.length; i++){
  if(cube[i]%2) result += cube[i];
}
return result;
}
```
### Filter Coffee
https://www.codewars.com/kata/filter-coffee/
```javascript
function search(budget, prices) {
return prices.filter((el) => el <= budget).sort((a,b) => a - b).join(',');
}
```
### A Gift Well Spent
https://www.codewars.com/kata/a-gift-well-spent
```javascript
var buy = function(x, arr){
   for(let i = 0; i < arr.length - 1; i++){
    for(let j = i + 1; j < arr.length; j++){
      if(arr[i] + arr[j] === x) {
         return [i, j];
     } 
    } 
  }
 return null;
};
```

### Maximum Triplet Sum (Array Series #7)
https://www.codewars.com/kata/maximum-triplet-sum-array-series-number-7/
```javascript
function maxTriSum(numbers){
   let res = [];
  let arr = numbers.sort((a,b) => b - a);
  for(let i = 0; i < arr.length; i++){
    if(arr[i] !== arr[i+1]) res.push(arr[i]);
  }
  return res[0] + res[1] + res[2];
}
```
### Find The Parity Outlier
https://www.codewars.com/kata/find-the-parity-outlier/
```javascript
function findOutlier(integers){
  let oddInEven;
  let oddArr = integers.filter((el) => el%2);
  if(oddArr.length === 1) return oddArr[0]
  else {
   integers.forEach((el) => {if(el%2 === 0) oddInEven = el})
  } 
  return oddInEven;
}
```
### Love vs friendship
https://www.codewars.com/kata/love-vs-friendship/
```javascript
function wordsToMarks(string){
  let alph = ("abcdefghijklmnopqrstuvwxyz").split('');
  let strArr = string.split('');
  let count = 0;
  for(let i = 0; i < strArr.length; i++){
   for(let j = 0; j < alph.length; j++){
     if(strArr[i] === alph[j]) count += j+1;
   }
  }
    return count;
}
```
### Number of People in the Bus
https://www.codewars.com/kata/number-of-people-in-the-bus/
```javascript
llet number = busStops => busStops.reduce((acc,cur) => acc + cur[0] - cur[1],0)
```
### Two Sum
https://www.codewars.com/kata/two-sum/train/javascript
```javascript
unction twoSum(numbers, target) {
  for(let i = 0; i < numbers.length - 1; i++){
    for(let j = 1; j < numbers.length; j++){
      if(numbers[i] + numbers[j] === target) return [i, j];
    }
  }
}
```
### Sum of positive
https://www.codewars.com/kata/sum-of-positive/
```javascript
function positiveSum(arr) {
 return arr.filter((el) => el > 0).reduce((acc, cur) => acc + cur, 0);
}
```
### Disemvowel Trolls
https://www.codewars.com/kata/disemvowel-trolls/
```javascript
return str.replace(/[aeiou]/gi, '');
```
### For Twins: 2. Math operations
https://www.codewars.com/kata/for-twins-2-math-operations
```javascript
function iceBrickVolume(radius, bottleLength, rimLength) {
  let a = radius * (2 ** 0.5);
  let c = bottleLength - rimLength;
  return Math.floor(a * a * c);
}
```
### Converting Measures
https://www.codewars.com/kata/converting-measures
```javascript
function convertRecipe(recipe){
  let arr = recipe.split(' ');

  for(let i = 0; i < arr.length; i++){
    if(typeof +arr[i] === 'number' && arr[i+1] === 'tbsp'){
       arr[i + 1] = arr[i + 1] + ' (' + Math.ceil(eval(arr[i]) * 15) + 'g)';
       i++;
    }
    if(typeof +arr[i] === 'number' && arr[i+1] === 'tsp'){
       arr[i + 1] = arr[i + 1] + ' (' + Math.ceil(eval(arr[i]) * 5) + 'g)';
        i++;
     }
  }
  return arr.join(' ');
}
```
### Convert string to camel case
https://www.codewars.com/kata/convert-string-to-camel-case
```javascript
function toCamelCase(str){
  let clearArr = str.replace(/-|_/g, ' ').split(' ');
  let resArr = [clearArr[0]]

  for(let i = 1; i < clearArr.length; i++){
    resArr.push(clearArr[i].substring(0, 1).toUpperCase() + clearArr[i].substring(1).toLowerCase());
  }
  return resArr.join('');
}
```
```javascript
function toCamelCase(str){
   return str.split(/-|_/g).map((el, i) => (i > 0 ? el.substring(0,1).toUpperCase() + el.slice(1) : el)).join('');
}
```
### Welcome! OBJECTS
https://www.codewars.com/kata/welcome
```javascript
function greet(language) {
	let greet = {
    english: 'Welcome',
    czech: 'Vitejte',
    danish: 'Velkomst',
    dutch: 'Welkom',
    estonian: 'Tere tulemast',
    finnish: 'Tervetuloa',
    flemish: 'Welgekomen',
    french: 'Bienvenue',
    german: 'Willkommen',
    irish: 'Failte',
    italian: 'Benvenuto',
    latvian: 'Gaidits',
    lithuanian: 'Laukiamas',
    polish: 'Witamy',
    spanish: 'Bienvenido',
    swedish: 'Valkommen',
    welsh: 'Croeso',
    };
    if(greet[language]){
      return greet[language];
    } else return 'Welcome';
  }
```
### The Office I - Outed OBJECTS
https://www.codewars.com/kata/the-office-i-outed
```javascript
function outed(meet, boss){
  let sum = 0;
  let empl = 0;
  for(let key in meet){
    if(key === boss){
      sum = sum + meet[key] * 2;
    } else {
      sum = sum + meet[key];
    }
    empl++
  }
  if(sum / empl <=5){
    return 'Get Out Now!';
  } else return 'Nice Work Champ!'
}
```
### The Office II - Boredom Score
https://www.codewars.com/kata/the-office-ii-boredom-score
```javascript
function boredom(staff){
  let dep = {
    'accounts': 1,
    'finance' : 2, 
    'canteen' : 10, 
    'regulation' : 3, 
    'trading' : 6, 
    'change' : 6,
    'IS' : 8,
    'retail' : 5,
    'cleaning' : 4,
    'pissing about': 25,
  };
  let sum = 0;
  for (let key in staff){
    sum += dep[staff[key]];
  }
    if(sum <= 80) return 'kill me now';
  if(sum > 80 && sum < 100) return 'i can handle this';
  if(sum >= 100) return 'party time!!';
}
```
### Who's Online?
https://www.codewars.com/kata/whos-online/
```javascript
const whosOnline = (friends) => {
  
  let obj = {};
  for(let i = 0; i < friends.length; i++){
    if(friends[i].status === 'online' && friends[i].lastActivity <= 10){
      if(!obj.online) obj.online = [];
      obj.online.push(friends[i].username);
    }
   if(friends[i].status === 'offline'){
      if(!obj.offline) obj.offline = [];
      obj.offline.push(friends[i].username);
    }
    if(friends[i].status === 'online' && friends[i].lastActivity > 10){
      if(!obj.away) obj.away = [];
      obj.away.push(friends[i].username);
    }
  }
  return obj;
}
```
### Simple validation of a username with regex
https://www.codewars.com/kata/simple-validation-of-a-username-with-regex/
```javascript
function validateUsr(username) {
  return /^[a-z0-9_]{4,16}$/g.test(username);
}
```
### Reverse Vowels In A String
https://www.codewars.com/kata/reverse-vowels-in-a-string/
```javascript
function reverseVowels(str) {
  let vowels = /[AEIOU]/ig;
  let strVow = [];
  let res = str.split('');
  for(let i = 0; i < str.length; i++){
    if(vowels.includes(str[i])){
      strVow.push(str[i]);
    }  
  }

  for(let i = 0; i < res.length; i++){
    if(vowels.includes(res[i])){
      res[i] = strVow[strVow.length-1];
      strVow.pop();
    } 
  }
  return res.join('');
}
```
### Bumps in the Road
https://www.codewars.com/kata/bumps-in-the-road/
```javascript
function bump(x){

  return  x.split('n').length > 16 ? 'Car Dead' : 'Woohoo!';
}
```
### Balanced Number (Special Numbers Series #1 )
https://www.codewars.com/kata/balanced-number-special-numbers-series-number-1
```javascript
function balancedNum(number){
  
  let numArr = number.toString().split('').map((d) => +d);
  let sumF = 0, sumB = 0;
  if(numArr.length <= 2) return 'Balanced';
  
  if(numArr.length%2 === 0){
    for(let i = 0; i < Math.floor(numArr.length / 2) - 1; i++){
      sumF += numArr[i];
      sumB += numArr[numArr.length-1-i];
      console.log(sumF, sumB);
    }
  } else {
    for(let i = 0; i < Math.floor(numArr.length / 2); i++){
      sumF += numArr[i];
      sumB += numArr[numArr.length-1-i];
      console.log(sumF, sumB);
    }
  }
  
  return (sumF === sumB) ? 'Balanced' : 'Not Balanced';
}
```
### Player Contact Manager
https://www.codewars.com/kata/player-contact-manager
```javascript
function playerManager(players) {
  if(players === null || players.length === 0) return [];
  let arr = players.split(', ');
  let list = [];
  
  for(let i = 0; i < arr.length; i+=2){
    let obj = {player : arr[i], contact : +arr[i+1]};
    list.push(obj);
  }
  return list;
}
```
### Minimum Steps (Array Series #6)
https://www.codewars.com/kata/minimum-steps-array-series-number-6
```javascript
function minimumSteps(numbers, value){
 numbers.sort((a,b) => a - b);
 let count = 0;
 let sum = numbers[0];
 for(let i = 1; i < numbers.length; i++){
   if(sum < value){
     sum += numbers[i];
     count++;
   }
 }
 return count;
}
```

### Form The Largest
https://www.codewars.com/kata/form-the-largest
```javascript
function maxNumber(n){
  let mod = n.toString().split('').map((el)=>+el).sort((a,b) => b - a).join('');
  return +mod;
}
```
### Get the Middle Character
https://www.codewars.com/kata/get-the-middle-character/
```javascript
function getMiddle(s){
  let cl = Math.floor(s.length/2);
  return (s.length%2 !== 0) ? s.charAt(cl) : s.slice(cl-1, cl+1)
}
```
### 1/n- Cycle // for discussing !!!
https://www.codewars.com/kata/1-slash-n-cycle/
```javascript
function cycle(n) {
 if (n % 2 == 0 || n % 5 == 0) return -1;
 
  let i = 0, j = 1;
  while (++i) {
    j = j * 10 % n;
     if (j == 1) return i;
  }
}
```
### Javascript Mathematician // for discussing !!!
https://www.codewars.com/kata/javascript-mathematician/
```javascript

```
### Find the odd int
https://www.codewars.com/kata/find-the-odd-int/
```javascript
function findOdd(A) {
  let countN = 0;
  for(let i = 0; i < A.length; i++) {
    for(let j = 0; j < A.length; j++) {  
      if(A[i] === A[j]) countN++;
    }
    if (countN % 2 !== 0) return A[i];
    }
    countN = 0;
}
```
### Highest and Lowest
https://www.codewars.com/kata/highest-and-lowest/
```javascript
function highAndLow(numbers){
  let numArr = numbers.split(' ');
  let min = Math.min(...numArr),  max = Math.max(...numArr);
  return `${max} ${min}`;
 }; 
```
### Descending Order
https://www.codewars.com/kata/descending-order
```javascript
function descendingOrder(n){
  return Number(n.toString().split('').sort((a, b) => b-a).join(''));
}
```

### Playing with cubes I
https://www.codewars.com/kata/playing-with-cubes-i/train/java
```java
public class Cube{
 int side;
 public class EncapsulationDemo {
   private int number;
   private String stringValue;
   private Object anObject;
   
   public int getNumber() {
     return number;
   }
   
   public void setNumber(int number) {
     this.number = number;
   }
   
   public String getStringValue() {
     return stringValue;
   }
   
   public void setStringValue(String stringValue) {
     this.stringValue = stringValue;
   }
   
   public Object getAnObject() {
     return anObject;
   }
   
   public void setAnObject(Object anObject) {
     this.anObject = anObject;
   }
   
   public EncapsulationDemo() {
   }
   
   public EncapsulationDemo(int number, String stringValue, Object anObject) {
     this.number = number;
     this.stringValue = stringValue;
     this.anObject = anObject;
   }
 }
 int getSide(){
   return side;
 }
 
 void setSide(int side){
   this.side = side;
 }
}
```

### Lombok Encapsulation
https://www.codewars.com/kata/lombok-encapsulation/
```java

```

### Building blocks
https://www.codewars.com/kata/building-blocks/
```java
public class Block {
    private int width;
    private int length;
    private int height;

    public int getWidth() {
        return width;
    }

    public int getLength() {
        return length;
    }

    public int getHeight() {
        return height;
    }

    public Block(int[] arr) {
        this.width = arr[0];
        this.length = arr[1];
        this.height = arr[2];
    }

    public int getVolume(){
        return width * length * height;
    }

    public int getSurfaceArea(){
        return 2 * (width * length + width * height + length * height);
    }
}
```