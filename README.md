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

###Credit card issuer checking
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
