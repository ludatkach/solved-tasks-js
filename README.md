# solved-tasks
* Array Array Array
```javascript
function explode(x) {
    let duplArr = x;
    let score = 0;
    for ( let i = 0; i <= 1; i ++ ) {
         if ( typeof(duplArr[i]) === 'number' ) {
            score += duplArr[i];
        } 
        if ( typeof(duplArr[0]) != 'number' && typeof(duplArr[1]) != 'number') {
            return 'Void!';
        }
    }
    let newArr = [];
    for ( let i = 0; i < score; i ++ ) {
        newArr[i] = duplArr;
    }
    return newArr;
}
```
```javascript
//Sort the odd
function sortArray(array) {
  let oddEl = [];
    let newArr = array.slice();
    for (let i = 0; i < newArr.length; i++) {
        if (newArr[i] % 2 !== 0) {
            oddEl.push(newArr[i]);
        }
    }
    oddEl.sort(function (a, b) { return a - b });
    for (let i = 0, j = 0; i < newArr.length; i++) {

        if (newArr[i] % 2 != 0) {
            newArr[i] = oddEl[j];
            j++;
        }
    }
    return newArr;
}
```
```javascript
//RGB To Hex Conversion
function rgb(r, g, b){
    let arrDec = [ r, g, b];
    let hexNum = '';
    for ( let i = 0; i < arrDec.length; i++ ) {
        if ( arrDec[i] >= 0 && arrDec[i] <= 255){
            let hex = arrDec[i].toString(16);
            hexNum += hex.length == 1 ? "0" + hex : hex;
        } else if ( arrDec[i] < 0 ) {
            arrDec[i] = 0;
            let hex = arrDec[i].toString(16);
            hexNum += hex.length == 1 ? "0" + hex : hex;
        } else {
            arrDec[i] = 255;
            let hex = arrDec[i].toString(16);
            hexNum += hex.length == 1 ? "0" + hex : hex;
        }
    }
    return hexNum.toUpperCase();
}
```
```javascript
function toWeirdCase(string){
  let newStr = string.split(' ');
    let weirdStr = '';
    for (let i = 0; i < newStr.length; i++) {
        let newWord = '';
        for (let j = 0; j < newStr[i].length; j++) {
            if (j % 2 === 0) {
                newWord += newStr[i][j].toUpperCase();
            } else {
                newWord += newStr[i][j].toLowerCase();
            }
        }
        if (weirdStr.length) {
            weirdStr += ' ' + newWord;
        } else {
            weirdStr += newWord;
        }   
    }

    return weirdStr;
}
```
```javascript
//Bit Counting
var countBits = function(n) {
    let count = 0;
    let binNum = (n >>> 0).toString(2);
    for ( let i = 0; i < binNum.length; i++ ) {
        
        if ( binNum[i] === "1" ) {
            count++;
        }
    }
    return count;
}
```
```javascript
//Array.diff
function array_diff(a, b) {
    let newArr = [];
    for ( let i = 0; i < b.length; i++ ) {
        for(let indx = a.indexOf(b[i]); indx >= 0;  indx = a.indexOf(b[i])) {
            a.splice(indx, 1);
        }
    }
    return a;
}
```
```javascript
//Find the next perfect square!
function findNextSquare(sq) {
    let n = Math.sqrt(sq);
    if ( n % 1 === 0 ) {
        let x = sq + 1;
        while ( x > sq ) {
            if ( Math.sqrt(x) % 1 === 0) {
                return x;
            }
        x++;
        }
    } else {
        return -1;
    }
}
```
```javascript
//Sum of two lowest positive integers
function sumTwoSmallestNumbers(numbers) {  
  let sum = 0;
    numbers.sort((a,b) => a - b);
    sum = numbers[0] + numbers[1];
    return sum;
}

//Odd or Even?
function oddOrEven(array) {
     let sum = 0;
    if ( !array) {
        return "even";
    }
    for (  let i = 0; i < array.length; i++ ) {
        sum += Math.abs(array[i]);
    }
    if ( sum % 2 === 0 ) {
        return "even";
    } else {
        return "odd";
    }
}

//Sum of Odd Cubed Numbers
function cubeOdd(arr) {
     let sum = 0;
     let result = 0;
     for ( let i = 0; i < arr.length; i++ ){
        if (typeof(arr[i]) === 'number' ) {
            if ( arr[i] % 2 != 0 ) {
                result = Math.pow(arr[i], 3);
                sum += result;
            }
        } else {
            return undefined;
        }
     }
     return sum;
}
```
```javascript
//Squares sequence
function squares(x, n) {
    let arr = [];
    if ( n <= 0 ) {
        return [];
    }
    arr.push(x);
    for (let i = 0; i < n-1; i++ ){
        arr.push( Math.pow(x, 2));
        x = Math.pow(x, 2);
    }
    return arr;
}

//Square Every Digit
function squareDigits(num){
    let str = '';
    let newNum = '';
    str += num;
    for (let i = 0; i < str.length; i++ ){
        newNum +=Math.pow(str[i], 2);
    }
    return +newNum;
}
```
```javascript
//Filter the number
var FilterString = function(value) {
  let num='';
    for ( let i = 0; i < value.length; i++ ) {
        if ( isNaN(value[i]) === false)  {
            num +=value[i];
        }

    }
    return +num;
}

//Sum of the first nth term of Series
function SeriesSum(n)
{
  if ( n === 0 || n === 1 ) {
        return n.toFixed(2);
    }
    let sum = 0;
    for ( let i = 0; i < n; i++ ) {
        sum += 1/(1+i*3);
    }
    return sum.toFixed(2);
}
```
```javascript
//Numbers to Letters
function switcher(x) {
    let arr = " ?!abcdefghijklmnopqrstuvwxyz-".split('').reverse();
    let newArr = x.map( Number);
    let string = '';
    newArr.forEach(el => {string += arr[el]});
    return string;
 }
```
```javascript
//Numbers to Letters
function switcher(x){
    let arr = " ?!abcdefghijklmnopqrstuvwxyz-".split('').reverse();
    let newArr = x.map( Number);
    let string = '';
    newArr.forEach(el => {string += arr[el]});
    return string;
}
//Regex validate PIN code
function validatePIN (pin) {
    return pin.match(/^\d{4}$|^\d{6}$/) ? true : false;
}
```
```javascript
//Powers of 3
function largestPower(n){
    let k = 0;
    for (; Math.pow(3,k) < n; k++);
    return --k;
}

//Power of two
function isPowerOfTwo(n){
  if (Number.isInteger(Math.log2(n))) {
    return true;
  } else if (n === 1) {
    return true;
  } else if (n % 2 === 1) {
    return false;
  } else {
    return false;
  }
}

//Factorial
function factorial(n){
  return n === 1 || n === 0 ? 1 :  n * factorial(n-1);
}

//Difference Of Squares
function differenceOfSquares(n){
  let sumNum = 0;
    let sqrs = 0;
    //let difference = 0;
    for ( let i = 1; i <= n; i++ ) {
        sumNum += i;
        sqrs += Math.pow(i,2);
    }
   let sqrSum = Math.pow(sumNum,2);
   return sqrSum - sqrs;
}
```
```javascript
//Tail Swap
function tailSwap(arr) {
    let newArr = [];
    let el1= '';
    let el2 ='';
     let indx1 = arr[0].indexOf(':');
     let indx2 = arr[1].indexOf(':');
     let pos1 = indx1+1;
     let pos2 = indx2+1;
     let tail1 = arr[0].slice(pos1);     
     let tail2 = arr[1].slice(pos2);
     el1 += arr[0].slice(0,pos1) + tail2;
     el2 += arr[1].slice(0,pos2) + tail1;
    newArr.push(el1);
    newArr.push(el2);
    return newArr;
}
```
```javascript
//Every possible sum of two digits
function digits(num){
    numStr = num + '';
    let arr = numStr.split('');
    let sum = [];
    for ( let i =0; i < arr.length; i++ ) {
        for ( let j = i+1; j < arr.length; j++ ) {
            let val = +arr[i] + +arr[j];
            sum.push(val);
        }
    }
    return sum;
}

//Can Santa save Christmas?
function determineTime(durations){
    let seconds = 0;
    let arr = [];
    for (let i = 0; i < durations.length; i++ ){        
        arr = durations[i].split(':');
       seconds += arr[0] * 60 * 60 + arr[1] * 60 + arr[2]*1;
    }
    return (seconds <= 86400 ) ? true : false;
}
```
```javascript
//Check three and two
function checkThreeAndTwo(array) {
    let counters = {
        'a': 0,
        'b': 0,
        'c': 0,
    };
    array.forEach(val => counters[val]++);
    let arrVal = Object.values(counters);
    return arrVal.indexOf(2) >= 0 && arrVal.indexOf(3) >= 0;
}

//Make a function that does arithmetic!
function arithmetic(a, b, operator){
  switch ( operator) {
        case "add":  return a + b; 
                breake;
        case "subtract": return a - b;
                breake;
        case "multiply": return a * b;
                breake;
        case "divide": return a / b;
                breake;
    }
}
```
```javascript
//What is my name score? #1
function nameScore(name){
    for(key in alpha) {
        key.split('').forEach(letter => alpha[letter] = alpha[key]);
    }
    let sum = 0;
    name.toUpperCase().split('').forEach(letter => letter in alpha ? sum += alpha[letter]:0);
    return {[name]: sum};
}

//Coding Meetup #5 - Higher-Order Functions Series - Prepare the count of languages
function countLanguages(list) {
    let counts = {};
    list.map(el=>el.language in counts ? counts[el.language]++ : counts[el.language] = 1);
    return counts;
}

//Numbers to Objects
function numObj(s){
    let arrObj =[];
    for ( let i = 0; i < s.length; i++ ) {
        let num = String(s[i]);
        let x = String.fromCharCode(num);
        arrObj.push({[num]:x});
    }
    return arrObj;
}
```
```javascript
//The Office I - Outed
function outed(meet, boss){
    let score = 0;
    for (let key in meet){
        if ( key === boss ) {
            meet[key] = meet[key] * 2;
        }
        score +=meet[key];
    }
    let totalScore = score / Object.keys(meet).length;
    return  totalScore <= 5 ? 'Get Out Now!' : 'Nice Work Champ!';
}
```
```javascript
//How many days are we represented in a foreign country? 
function daysRepresented(trips){
    let count = 0;
    let tr = trips.sort((a,b)=>a[0]-b[0]);
    // merge overlaping days
    for (let i = 1; i < tr.length; ) {
        if(tr[i][0] <= tr[i-1][1]) {
            tr[i-1][1] = tr[i][1];
            tr.splice(i,1);
            continue;
        } 
        i++;
    }
    // count days
    for (let i = 0; i < tr.length; i++) {
        let num = tr[i][1] - tr[i][0] + 1;
        count += num;
    }
    return count;
}
```
```javascript
//Permute a Palindrome
function permuteAPalindrome (input) { 
    let arr = input.split('');
    let obj = {};
    arr.forEach( val => val in obj ? obj[val]++ : obj[val] = 1 );
    let numberOdds = Object.values(obj).filter(val => val % 2).length;
    if ( arr.length % 2 === 0 && numberOdds === 0  || arr.length % 2 != 0 && numberOdds === 1 ) {
        return true;
    } else {
        return false;
    }
}

//Most valuable character
function solve(st) {
    let arr = st.split('');
    let unique = [...new Set(arr)];
    let newArr = unique.map(val => { return { letter: val, difference: arr.lastIndexOf(val) - arr.indexOf(val)}; });
    let result = newArr.sort((a,b) =>  b.difference - a.difference === 0 ? a.letter.charCodeAt() - b.letter.charCodeAt(): b.difference - a.difference );
    return result[0].letter;
}
```
```javascript
//The Office II - Boredom Score
function boredom(staff){
    let count = 0; 
    let depScore = {
        accounts: 1,
        finance: 2,
        canteen: 10,
        regulation: 3,
        trading: 6,
        change: 6,
        IS: 8,
        retail: 5,
        cleaning: 4,
        "pissing about": 25,
    };

    let valuesDepartments = Object.values(staff);
    valuesDepartments.forEach(val =>  count += depScore[val]);

    if ( count < 100 && count > 80) {   
      return 'i can handle this';
    } else if ( count <= 80 ) {   
      return 'kill me now';
    } else if ( count >= 100 ) {
      return 'party time!!';
    }
}
```
```javascript
//Are the numbers in order?
function inAscOrder(arr) {
    let  sum = arr.reduce((acc, val)=>acc+val);
    if( typeof sum !== 'number') {
        return false;
    }
    for ( let i = 1; i < arr.length; i++ ) {
        if ( arr[i] < arr[i-1]) {
            return false;
        }
    }
    return true;
}

//Sort and Star
function twoSort(s) {
    s.sort();
    let word = s[0].split('').join('***');
    return word;
}
```
```javascript
//Find the missing element between two arrays
function findMissing(arr1, arr2) {
    arr2.forEach(val => {
        let elIndx = arr1.indexOf(val);
        if ( elIndx >= 0 ) {
            arr1[elIndx] = undefined;
        }
    });
    return +arr1.filter(val => val != undefined );
}
```
```javascript
//Remove duplicate words
function removeDuplicateWords (s) {
    let arr = s.split(' ');
    let str = new Set(arr);
    return Array.from(str).join(' ');
}
//Get the mean of an array
function getAverage(marks){
  return Math.floor((marks.reduce((acc,curr) => acc + curr, 0))/marks.length);
}
```
```javascript
//Check the exam
function checkExam(array1, array2) {
     let score = 0;
    for ( let i = 0; i < array1.length; i++ ) {
        if ( array1[i] === array2[i]) {
            score +=4;
        } else if ( array2[i]  === '') {
            continue;
        } else {
            score -= 1;
        }
    }
    return score > 0 ? score : 0;
}

//Merge two sorted arrays into one
JavaScript:
function mergeArrays(arr1, arr2) {
    let newArr =  arr1.concat(arr2); 
    let str = new Set(newArr);
    return [...str].sort((a, b) => a - b);
}
```
```javascript
//Check the exam
function checkExam(array1, array2) {
     let score = 0;
    for ( let i = 0; i < array1.length; i++ ) {
        if ( array1[i] === array2[i]) {
            score +=4;
        } else if ( array2[i]  === '') {
            continue;
        } else {
            score -= 1;
        }
    }
    return score > 0 ? score : 0;
}
```
```javascript
//Clocky Mc Clock-Face
var whatTimeIsIt = function(angle) {
    let hour;
    let minutes;
    if ( angle === 0  || angle === 360) {
        return "12:00";
    } else {
        hour = Math.floor(angle / 30) +'';
        if ( hour === '0' ) {
          hour = '12';
        }
        if ( hour.length === 1 ) {
            hour = '0' + hour;
        }
        minutes = (Math.floor((angle % 30) * 2)).toFixed();
        if ( minutes.length === 1) {
            minutes = '0' + minutes;
        }
        return hour + ":" + minutes;
    }
}
```
```javascript
//Number of People in the Bus
var number = function(busStops){
    let re = busStops.reduce((acc, cur) => {
        acc[0] += cur[0];
        acc[1] += cur[1];
        return acc;
    });
    return re[0]-re[1];
}

//Find Nearest square number
function nearestSq(n){
   return  Math.pow(Math.round(Math.sqrt(n)), 2);
}
```
```javascript
//Two Sum
function twoSum(numbers, target) {
    let length = numbers.length;
    for ( let i = 0; i < length-1; i++ ) {
        for ( let j = i + 1; j < length; j++ ) {
            if ( (numbers[i] + numbers[j]) === target ) {
                return [i,j];
            }
        }
    }
    return [];
}
```
```javascript
//Sum of Digits / Digital Root
//(1)
function digital_root(n) {
  return (n - 1) % 9 + 1;
}
//(2)
function digital_root(n) {
    do {
        let arr = (String(n)).split('').map(val => +val);
        n = arr.reduce((acc, curr) => acc + curr);
    } while (String(n).length > 1);
    return n;
}
```
```javascript
//Understanding closures - the basics
function buildFun(n){
    var res = [];
    for (let i = 0; i < n; i++) {
        res.push(function () {
            return i;
        });
    }
    return res;
}

//Disemvowel Trolls
function disemvowel(str) {
  return str.replace(/[aeuio]/ig,'');
}
```
```javascript
//Vasya and Book
function bookIsDay(pages,days){
    for ( var i = 0; pages > 0; i++ ){
        let iIdx = i % days.length;
        pages -= days[iIdx];
    }
    return i == 7 ? 7 : i % days.length;
}
```
```javascript
//Character Frequency
function charFreq(message) {
    let arr = message.split("");
    let obj = {};
    arr.forEach( val => val in obj ? obj[val]++ : obj[val] = 1);
    return obj;
}


//Squash the bugs (1)
  function findLongest(str) {
    var spl = str.split(" ");
    var longest = 0;
    for (let i = 0; i < spl.length; i++){
      if (spl[i].length > longest) {
        longest = spl[i].length;
      }
    }
      return longest;
  }

//Squash the bugs (2)
function findLongest(str) {
    var arr2 = str.split(" ").map(x => x.length);
    let max = Math.max(...arr2);
    return max;
}
```
```javascript
//Smallest value of an array
function min(arr, toReturn) {
    let minVal = Math.min.apply(Math, arr);
    if ( toReturn === 'value') {
        return minVal;
    }
    if ( toReturn === 'index' ) {
        return arr.indexOf(minVal);
    }
}
```
```javascript
//Find The Parity Outlier
function findOutlier(integers){
    let arr1 = integers.filter(val => val % 2);
    let arr2 = integers.filter(val => val % 2 === 0 );
    return arr1.length === 1 ? arr1[0] : arr2[0];
}
```
```javascript
//Return the first M multiples of N
function multiples(m, n){
    let arr = [];
    for ( let i = 1; i <= m; i++ ) {
        arr.push( i * n );
    }
    return arr;
}

//Return String of First Characters
function makeString(s){
    let newArr = s.split(" ");
    let newWord = [];
    for ( let i = 0; i < newArr.length; i++ ) {
        newWord.push(newArr[i][0]);
    }
    return newWord.join('');
}
```
```javascript
//Give Me a Diamond
function diamond(n){
    if ( n % 2 === 0 || n < 0 ) {
        return null;
    }
    let side = Math.floor(n / 2);
    let a1 = [];
    for (let i = 0; i < side; i++) {
        let s1 = ' '.repeat(side - i) + '*'.repeat(i);
        let s2 = '*'.repeat(i);
        let s3 = s1 + '*' + s2 + '\n';
        a1.push(s3);
    }
    let a2 = [...a1];
    a1.push('*'.repeat(n) + '\n');
    return a1.concat(a2.reverse()).join('');
}
```
```javascript
//Asterisk it
function asteriscIt(n) { 
    let str = String(n).replace(/,/g, '');
    let arr = [];
    for ( let i = 0; i < str.length; i++ ) {
        if ( i < str.length - 1 && str[i] % 2 === 0 && str[i+1] % 2 === 0 ) {
            arr.push(str[i]);
            arr.push('*');
        } else {
            arr.push(str[i]);
        }
    }
    return arr.join('');
};

//Switch/Case - Bug Fixing #6
function evalObject(value){
  var result = 0;
  switch(value.operation){
    case'+': return result = value.a + value.b; break;
    case'-': return result = value.a - value.b; break;
    case'/': return result = value.a / value.b; break;
    case'*': return  result = value.a * value.b; break;
    case'%': return result = value.a % value.b; break;
    case'^': return result = Math.pow(value.a, value.b); break;
  }
  return result;
}
```
```javascript
//String Reversing, Changing case, etc.
function reverseAndMirror(s1,s2) {
    let strOne = s1.replace(/[A-z]/g, val=> val === val.toLowerCase() ? val.toUpperCase() : val.toLowerCase());
    let strTwo = s2.replace(/[A-z]/g, val=> val === val.toLowerCase() ? val.toUpperCase() : val.toLowerCase());
    let str1 = strOne.split('').reverse(); 
    let str2 = strTwo.split('').reverse();     
    let str = str1.join(''); 
    let newStr = str.concat(strOne); 
    let strSecond = str2.join('') + '@@@';
    
    return strSecond.concat(newStr);
}
```
```javascript
//Smallest value of an array
function min(arr, toReturn) {
    let minVal = Math.min.apply(Math, arr);
    if ( toReturn === 'value') {
        return minVal;
    }
    if ( toReturn === 'index' ) {
        return arr.indexOf(minVal);
    }
}
```
```javascript
//Dubstep
function songDecoder(song){
  return song.replace(/(WUB)+/g, ' ').trim();
}

//Calculate Price Excluding VAT
//return price without vat
function excludingVatPrice(price){
    let prodPr = 0;
    if ( price === null ) {
        return -1;
    } else {
        prodPr = (100 * price)/115;
        return +prodPr.toFixed(2);
    }
}
```
```javascript
//Thankful - String Drills: Repeater
function repeater(string, n){
  return string.repeat(n);
}

//Powers of 2
function powersOfTwo(n){
   const arr = [];
   for(let i = 0; i <= n; i++){
     arr.push(Math.pow(2, i));
   }
   return arr;
}
//second solution
function powersOfTwo(n){
    let newArr = [];
    for ( let i = 0; i <= n; i++ ) {
        newArr.push( 2 ** i );
    }
    return newArr;
}
```
[The First Non Repeated Character In A String](https://www.codewars.com/kata/570f6436b29c708a32000826/javascript)
```javascript
function firstNonRepeated(s) {
    let arr = s.split('');
    for ( let i = 0; i < arr.length; i++ ) {
        if ( arr.indexOf(arr[i]) === arr.lastIndexOf(arr[i]) ) {
            return arr[i];
        } 
    } 
    return null;
}
```
[Get initials from person name] (https://www.codewars.com/kata/57b56af6b69bfcffb80000d7/train/javascript)
```javascript
//Get initials from person name
function toInitials(name) {
    let nameArray = name.split(' ');
    let nameNew = '';
    for ( let i = 0; i < nameArray.length; i++ ){
        nameNew += nameArray[i][0] + '. ';
    }
     
    return nameNew.trim();
}
```
[Sum of odd numbers](https://www.codewars.com/kata/55fd2d567d94ac3bc9000064/train/javascript)
```javascript
function rowSumOddNumbers(n) {
	  let numberOfOddElementsBeforeN = (n - 1) * (1 + n - 1) / 2;
    let nthOddNumber = (numberOfOddElementsBeforeN + 1) * 2 - 1;
    let sum = 0;
    for (let i = 0; i < n; i++ , nthOddNumber += 2) {
        sum += nthOddNumber;
    }
    return sum;
}
```
[Thinkful - String Drills: Repeater level 2](https://www.codewars.com/kata/585a1f0945376c112a00019a/train/javascript)
```javascript
function repeater(string, n) {
    return `"${string}"` + ' repeated ' + n + ' times is: ' + `"${string.repeat(n)}"`;
}

```
[Count the divisors of a number](https://www.codewars.com/kata/542c0f198e077084c0000c2e/train/javascript)
```javascript
function getDivisorsCnt(n){
    let arr = [];
    for ( let i = 1; i <= n; i++ ) {
        if ( n % i === 0 ) {
            arr.push(i);
        } 
    }
    return arr.length;
}
```
[A Rule of Divisibility by 7](https://www.codewars.com/kata/55e6f5e58f7817808e00002e/train/javascript)
```javascript
function seven(m) {
    let count = 0;
    let lastNumber = 0;
    while(m && String(m).length > 2) {
        count++;
        let x = Math.floor(m / 10);
        let y = m - 10 * x;
        m = x - 2 * y;
    }
    return [m, count];
}
```
[Count all the sheep on farm in the heights of New Zealand](https://www.codewars.com/kata/58e0f0bf92d04ccf0a000010/train/javascript)
```javascript
function lostSheep(friday,saturday,total){
    let fridaySum = friday.length ? friday.reduce((acc, curr) => acc + curr) : 0;
    let saturdaySum = saturday.length ? saturday.reduce((acc, curr) => acc + curr) : 0;
    return total - fridaySum - saturdaySum;
}
```
[String to integer conversion](https://www.codewars.com/kata/54fdadc8762e2e51e400032c/train/javascript)
```javascript
function myParseInt(str) {
    str = str.trim();
    if(/^\d+$/g.test(str)){
        return Number(str);
    }

    return "NaN";
}
```
[Most sales](https://www.codewars.com/kata/5e16ffb7297fe00001114824/train/javascript)
```javascript
function top3(products, amounts, prices) {
    let indexes = [...Array(products.length).keys()];
    return indexes.sort((a, b) => amounts[b] * prices[b] - amounts[a] * prices[a]).slice(0, 3).map(idx=>products[idx]);
}
```
[Make the Deadfish swim](https://www.codewars.com/kata/51e0007c1f9378fa810002a9/train/javascript)
```javascript
// Return the output array, and ignore all non-op characters
function parse( data ) {
    let value = 0;
    let arr = [];
    for (let k = 0; k < data.length; k++ ) {
        if ( data[k] === 'i') {
            value ++;
        }
        if (data[k] === 'd') {
            value --;
        }
        if (data[k] === 's') {
            value = value * value;
        }
        if ( data[k] === 'o') {
            arr.push(value);
        }
        if ( !data.includes('idso')) {
            continue;
        }
    }
    return arr;
}
```
[Stop gninnipS My sdroW!](https://www.codewars.com/kata/5264d2b162488dc400000001/train/javascript)
```javascript
function spinWords(string){
    let arrStr = string.split(' ');
    let arrWord;
    let newStr = [];
    for ( let i = 0; i < arrStr.length; i++ ) {
        if ( arrStr[i].length > 4 ) {
            arrWord = arrStr[i].split('').reverse();
            newStr.push(arrWord.join(''));            
        } else {
            newStr.push(arrStr[i]);
        }
    }
    return newStr.join(' ');
}
```
[Sum of all the multiples of 3 or 5](https://www.codewars.com/kata/57f36495c0bb25ecf50000e7/train/javascript)
```javascript
function findSum(n) {
    let set = new Set()
    for (let i = 1; i * 3 <= n; i++) {
        set.add(i * 3);
    }
    for (let i = 1; i * 5 <= n; i++) {
        set.add(i * 5);
    }
    let sum = 0;
    set.forEach(val=>sum += val);
    return sum;
}
```
[Product Of Maximums Of Array (Array Series #2)](https://www.codewars.com/kata/5a63948acadebff56f000018/train/javascript)
```javascript
function maxProduct(numbers, size){
    let num = 1;
    let arr = numbers.sort((a,b) => b -a );
    for (let i = 0; i < size; i++ ) {
        num *= arr[i];
    }
    return num;
}
```
[Is my string repeating the same character over and over ?](https://www.codewars.com/kata/584fa5ae25dd087e6b000070/train/javascript)
```javascript
function hasOneChar(s) {
  return (s.match(/^(.)\1*$/g)) ? true : false;
}
```
[Absent vowel](https://www.codewars.com/kata/56414fdc6488ee99db00002c/train/javascript)
```javascript
function absentVowel(x){
    let vowelsArr = ['A', 'E', 'I', 'O', 'U'];
    let str = x.toUpperCase();
    for ( let i = 0; i < str.length; i++ ) {
        if ( str.indexOf(vowelsArr[i]) < 0 ) {
            return i;
        }
    }
}
```
[Tidy Number (Special Numbers Series #9)](https://www.codewars.com/kata/5a87449ab1710171300000fd/train/javascript)
```javascript
function tidyNumber(n){
    let arrN = Array.from(String(n), Number);
    for ( let i = 1; i < arrN.length; i++ ) {
        if( arrN[i-1] <= arrN[i] ) {
            continue;
        } else {
            return false;
        }
    }
    return true;
}
```
[Lottery machine](https://www.codewars.com/kata/5832db03d5bafb7d96000107/train/javascript)
```javascript
function lottery(str) {
    let myStr = str.match(/[0-9]+/g);
    if (myStr) {
        let allDigits = myStr.join('').split('');
        let set = new Set();
        let result = []
        allDigits.forEach(digit => {
            if (!set.has(digit)) {
                set.add(digit);
                result.push(digit);
            }
        });

        return result.join('');
    }
    return "One more run!";
}
```
[Sum Mixed Array](https://www.codewars.com/kata/57eaeb9578748ff92a000009/train/javascript)
```javascript
function sumMix(x){
    let sum = 0;
    for ( let i = 0; i < x.length; i++ ) {
        if ( typeof(x[i]) === 'string' ) {
            sum += +x[i];
        } else {
            sum += x[i];
        }      
    }
    return sum;  
}
```
[Beginner Series #4 Cockroach](https://www.codewars.com/kata/55fab1ffda3e2e44f00000c6/train/javascript)
```javascript
function cockroachSpeed(s) {
  let cm = 100000;
  let sec = 3600;
  let speed = cm * s / sec;
  return Math.floor(speed);
}
```
[Help Bob count letters and digits.](https://www.codewars.com/kata/5738f5ea9545204cec000155/train/javascript)
```javascript
function countLettersAndDigits(input) {
    let arr = input.match(/[0-9a-zA-Z]/g);
    return arr ? arr.length : 0;
}
```
[Sort Out The Men From Boys](https://www.codewars.com/kata/5af15a37de4c7f223e00012d/train/javascript)
```javascript
function menFromBoys(arr){
    let set = new Set(arr);
    let newArr = [...set];
    let odd = [];
    let even = [];
    for ( let i = 0; i < newArr.length; i ++ ) {
        if ( newArr[i] % 2 ) {
            odd.push(newArr[i]);
        } else {
            even.push(newArr[i]);
        }
    }
    even.sort((a, b) => a - b);
    let oddArr = odd.sort((a, b) => b - a);
    return even.concat(oddArr);
}
```
[The Wide-Mouthed frog!](https://www.codewars.com/kata/57ec8bd8f670e9a47a000f89/train/javascript)
```javascript
function mouthSize(animal) {
  if ( animal.toLowerCase() === 'alligator' ) {
    return "small";
  }
  return "wide";
}
```
[Grasshopper - Messi goals function](https://www.codewars.com/kata/55f73be6e12baaa5900000d4/train/javascript)
```javascript
function goals (laLigaGoals, copaDelReyGoals, championsLeagueGoals) {
  return laLigaGoals + copaDelReyGoals + championsLeagueGoals;
}
```
[noobCode 01: SUPERSIZE ME.... or rather, this integer!](https://www.codewars.com/kata/5709bdd2f088096786000008/train/javascript)
```javascript
function superSize(num){
  let arr = String(num).split('').sort ((a, b) => b - a );
  return +arr.join('');
}
```
[Sub-array elements sum](https://www.codewars.com/kata/5b5e0ef007a26632c400002a/train/javascript)
```javascript
function elementsSum(arr,d=0){
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        let idx = arr.length - 1 - i;
        if (typeof (arr[i]) === 'object' && arr[i].length > idx) {
            sum += arr[i][idx];
        } else {
            if (d) {
                sum += d;
            }
        }
    }

    return sum;
}
```
[Flatten and sort an array](https://www.codewars.com/kata/57ee99a16c8df7b02d00045f/train/javascript)
```javascript
function flattenAndSort(array) {
    let newArr = [];
    for (let i = 0; i < array.length; ++i) {
        for (let j = 0; j < array[i].length; ++j) {
            newArr.push(array[i][j]);
        }
    }
    return newArr.sort((a,b) => a - b);
}
```
[Balanced Number (Special Numbers Series #1 )](https://www.codewars.com/kata/5a4e3782880385ba68000018/train/javascript)
```javascript
function balancedNum(number)
{
    let sumLeft = 0;
    let sumRight = 0;
    let middle1Indx;
    let middle2Indx;
    let arr = String(number).split(''); 
    let length = arr.length;
    if ( (length % 2) === 0 ) {
        middle1Indx = length/2 - 1;
        middle2Indx = length/2;
        for ( let i = 0; i < middle1Indx; i++ ) {
            sumLeft += +arr[i];
        }    
        for ( let i = middle2Indx + 1; i < arr.length; i++ ){
            sumRight += +arr[i];
        }
    }
    if ( (length % 2) != 0 ) {
        middle1Indx = Math.floor(length/2);
        for ( let i = 0; i < middle1Indx; i++ ) {
            sumLeft += +arr[i];
        }    
        for ( let i = middle1Indx + 1; i < arr.length; i++ ){
            sumRight += +arr[i];
        }
    }
    if ( sumLeft === sumRight ){
         return "Balanced";
     } 
     return "Not Balanced";
}
```
[My Languages](https://www.codewars.com/kata/5b16490986b6d336c900007d/train/javascript)
```javascript
function myLanguages(results) {
    let arr = [];
    for ( let key in results) {
        if ( results[key] >= 60 ) {
        arr.push(key);
        }
    }    
    return arr.sort((a,b) => results[b] - results[a]); 
}
```
[Sort array by string length](https://www.codewars.com/kata/57ea5b0b75ae11d1e800006c/train/javascript)
```javascript
function sortByLength (array) {
    array.sort((a, b) => {
        if (a.length !== b.length) {
            return a.length - b.length;
        } else {
            return a.localeCompare(b)
        }
    });

    return array;  
};
```
[Sum even numbers](https://www.codewars.com/kata/586beb5ba44cfc44ed0006c3/train/javascript)
```javascript
function sumEvenNumbers(input) {
    let sum = 0;
    for ( let i = 0; i < input.length; i++ ) {
        if ( input[i] % 2 === 0) {
            sum += input[i];
        }
    }
    return sum;
}
```
[Does my number look big in this?](https://www.codewars.com/kata/5287e858c6b5a9678200083c/train/javascript)
```javascript
function narcissistic(value) {
    let arrNum = String(value).split('');
    let length = arrNum.length;
    let sum = 0;
    for ( let i = 0; i < arrNum.length; i++ ) {
        sum += Math.pow(+arrNum[i], length);
    }   
    return sum === value ? true : false;
}
```
[The Hashtag Generator](https://www.codewars.com/kata/52449b062fb80683ec000024/train/javascript)
```javascript
function generateHashtag (str) {
    let newStr = str.trim();
    if (newStr.length === 0 ) {
        return false;
    }
    let arrWords = str.split(' ');
    let stringWords = arrWords.map(val => val.charAt(0).toUpperCase() + val.slice(1));
   
    stringWords = '#' + stringWords.join('');
    if (stringWords.length > 140) {
        return false;
    } 
    return stringWords;  
}
```
[Srot the inner ctonnet in dsnnieedcg oredr](https://www.codewars.com/kata/5898b4b71d298e51b600014b/train/javascript)
```javascript
function sortTheInnerContent(words)
{
    let arrWords = words.split(' ');
    let stringWords = [];
    for ( let i = 0; i < arrWords.length; i++ ) {
        if (arrWords[i].length === 1) {            
            stringWords.push(arrWords[i].split('').splice(0,1));
        } else {
            stringWords.push(arrWords[i].charAt(0) + arrWords[i].slice(1, arrWords[i].length-1).split('').sort().reverse().join('') + arrWords[i].slice(-1));
        }
    }
    return stringWords.join(' ');
}
```
[Persistent Bugger.](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/train/javascript)
```javascript
function persistence(num) {
    let mult = [];
    let count = 0;
    if ( String(num).length === 1 ) {
        return 0;
    }
    do {
        let numbers = String(num).split('').map(val => +val);
        mult = String(numbers.reduce((acc, carr) => acc * carr));
        count++;
        num = +mult;
    } while ( mult.length > 1 );
    let x =0;
    return count;
}
```
[Alphabetized](https://www.codewars.com/kata/5970df092ef474680a0000c9/train/javascript)
```javascript
function alphabetized(s) {
    let sorting1 = (arr, compare) => arr
        .map((item, index) => ({ item, index }))
        .sort((a, b) => compare(a.item, b.item) || a.index - b.index)
        .map(({ item }) => item);
    let arr = s.replace(/[.,\/#!$%\^&\*;:{}=\-_`~@+()\d]/g, '').split(' ').join('').split('');
    let sorted = sorting1(arr, (a, b) => a.toLowerCase().localeCompare(b.toLowerCase()));
    return sorted.join('');
}
```
[Duplicate Encoder](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/train/javascript)
```javascript
function duplicateEncode(word){
     let arr = word.toLowerCase().split('');
    let setWord = ([...new Set(arr)]); 
    let str = [];
    for ( let i = 0; i < arr.length; i++ ) {
        if ( arr.indexOf(arr[i]) === arr.lastIndexOf(arr[i]) ) {
            str.push('(');
        } else {
            str.push(')');
        }
    }
    return str.join('');
}
```
[Your order, please](https://www.codewars.com/kata/55c45be3b2079eccff00010f/train/javascript)
```javascript
function order(words){
  return words.length ? words.split(' ').sort((a, b) => a.replace(/\D/g, '').localeCompare(b.replace(/\D/g, ''))).join(' ') : '';
}
```
[Multiples of 3 or 5](https://www.codewars.com/kata/514b92a657cdc65150000006/train/javascript)
```javascript
function solution(number){
    let sum = 0;
    for ( let i = 1; i < number; i++ ) {
        if ( ((number -i) % 3) === 0 || ((number - i) % 5) === 0 ) {
            sum += number-i;
        }
    }
    return sum;
}
```
[Valid Parentheses](https://www.codewars.com/kata/52774a314c2333f0a7000688/train/javascript)
```javascript
function validParentheses(parens){
    let arrL = [];
    let arrParens = parens.split('');
    for ( let i = 0; i < arrParens.length; i++ ) {
        if ( arrParens[0] === ')') {
            return false;
        } 
        if ( arrParens[i] === '(') {
            arrL.push(arrParens[i]);
        }

        if ( arrParens[i] === ')') {
            arrL.push(arrParens[i]);
        }
        if ( arrParens[i] === ')'  && arrL.includes('('))   {
            arrL.pop();
            arrL.pop();
        } 
    }
    if ( arrL.length === 0 ) {
        return true;
    }
    return false;
}
```
[Sum of Minimums!](https://www.codewars.com/kata/5d5ee4c35162d9001af7d699)
```javascript
function sumOfMinimums(arr) {
    let sum = 0;
    let vari;
    for ( let i = 0; i < arr.length; i++ ) {
        for ( let j = 0; j < arr[i].length; j++ ) {
            vari = Math.min(...arr[i]);
        }

        sum += vari;
    }
    return sum;
}
```
[String incrementer](https://www.codewars.com/kata/54a91a4883a7de5d7800009c/train/javascript)
```javascript
function incrementString (strng) {
    let numbersMatch = strng.match(/(\D*)(\d+)/);
    if (numbersMatch) {
        let prefix = numbersMatch[1];
        let numbers = numbersMatch[2];
        let numbersOneUp = String(+numbers + 1);
        let leadingZeroes = numbers.length - numbersOneUp.length;
        return prefix + '0'.repeat(leadingZeroes >= 0 ? leadingZeroes : 0) + numbersOneUp;
    }

    return strng + '1';
} 
```
[Find the odd int](https://www.codewars.com/kata/54da5a58ea159efa38000836/train/javascript)
```javascript
function findOdd(A) {
    let obj = {};
    A.forEach(val => {
        if(val in obj) {
            obj[val]++;
         } else {
            obj[val] = 1;
         } 
    });
    let odd;
    Object.keys(obj).forEach((key) => {
        if (obj[key] % 2) {
            odd = key;
        }
    });

    return +odd;
}
```
[Playing with digits](https://www.codewars.com/kata/5552101f47fc5178b1000050/train/javascript)
```javascript
function digPow(n, p){
    let sum = 0;
    let arr = String(n).split('');
    for ( let i = 0, j = p; i < arr.length; i++, j++ ) {
        sum += +Math.pow(arr[i], j);
    }
    let result = sum / n;
    if ( Number.isInteger( result )) {
        return result;
    }
    return -1;
}
```
[Counting Duplicates](https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1/train/javascript)
```javascript
function duplicateCount(text){
    let arr = text.toLowerCase().split('');
    let duplicates = arr.filter(val => arr.indexOf(val) != arr.lastIndexOf(val));
    let newArr = Array.from(new Set(duplicates));
    if ( newArr.length > 0 ) {
        return newArr.length;
    }
    return 0;
}
```
[Tribonacci Sequence](https://www.codewars.com/kata/556deca17c58da83c00002db/train/javascript)
```javascript
function tribonacci(signature,n){
    let newArr = [];
    if ( n === 0 ) {
        return [];
    }
    if ( n === 1 ) {
      newArr.push(signature[0]);
      return newArr;
    }
    newArr = [...signature];
    let sum = 0; 
    for ( let i = 0; i < n-3; i++ ) {
        sum += newArr[i] + newArr[i+1] + newArr[i+2];
        newArr.push(sum);
        sum = 0;
    }
    return newArr;
}
```
[Replace With Alphabet Position](https://www.codewars.com/kata/546f922b54af40e1e90001da/train/javascript)
```javascript
function alphabetPosition(text) {
    let alph = "abcdefghijklmnopqrstuvwxyz";
    let alphArr = alph.split('');
    let textStr = text.toLowerCase().split(' ').join('').replace(/\W/g,'').split('');
    let out = [];
    for(let i = 0; i < textStr.length; i++ ) {
        if ( alph.includes(textStr[i])) {
            out.push(alphArr.indexOf(textStr[i]) + 1);
        }
    }
    return out.join(' ');
}
```
[IQ Test](https://www.codewars.com/kata/552c028c030765286c00007d/train/javascript)
```javascript
function iqTest(numbers){
    let arr = numbers.split(' ');
    let objOdd = {};
    let objEv = {};
    let countOdd = 0;
    let countEv = 0;
    arr.forEach(val => {
        if ( val % 2) {
            objOdd[val] = arr.indexOf(val);
            countOdd++;
        } else {
            objEv[val] = arr.indexOf(val);
            countEv++;
        }
    });
    if ( countEv === 1 ) {
        
        return +Object.values(objEv) +1;
    } 
    if ( countOdd === 1) {
        return +Object.values(objOdd) +1;
    }
}
```
[Arrh, grabscrab!](https://www.codewars.com/kata/52b305bec65ea40fe90007a7/train/javascript)
```javascript
function grabscrab(anagram, dictionary) {
    let newArr = [];
    let anagramSorted = anagram.split('').sort().join('');
    dictionary.forEach(word => {
        let wordSorted = word.split('').sort().join('');
        if(anagramSorted === wordSorted) {
            newArr.push(word);
        }
    });
    return newArr;
}
```
[Sum Strings as Numbers](https://www.codewars.com/kata/5324945e2ece5e1f32000370/train/javascript)
```javascript
function sumStrings(a,b) { 
    a = a.replace(/^0+/g, '');
    b = b.replace(/^0+/g, '');
    if (a.length < b.length) {
        a = '0'.repeat(b.length-a.length) + a;
    } else if (b.length < a.length) {
        b = '0'.repeat(a.length-b.length) + b;
    }

    let a1 = a.split('').reverse().map(val=>+val);
    let b1 = b.split('').reverse().map(val=>+val);;

    let carryOver = 0;
    let c1 = a1.map((val, index) => { 
        let sum = val + b1[index] + carryOver;
        if( sum > 9) {
            carryOver = 1;
        } else {
            carryOver = 0;
        }
        return sum % 10;
    });

    if( carryOver ) {
        c1.push(1);
    }

    return c1.reverse().join('');
}
```
[Get the Middle Character](https://www.codewars.com/kata/56747fd5cb988479af000028/train/javascript)
```javascript
function getMiddle(s)
{
    let middle;
    let arr = s.split('');
    for ( let i = 0; i < arr.length; i++ ) {
        if ( arr.length % 2 ) {
            middle = arr[Math.floor(arr.length / 2)];
        }
        if ( arr.length % 2 === 0 ) {
            let midIndx = arr.length / 2;
            middle = '' + arr[midIndx-1] + arr[midIndx];
        }
    }
    return middle;
}
```
[Isograms](https://www.codewars.com/kata/54ba84be607a92aa900000f1/train/javascript)
```javascript
function isIsogram(str){
    let strLow = str.toLowerCase();
    let arrStr = strLow.split('');
    let set = new Set(arrStr);
    return (strLow.length === set.size ) ? true : false;
}
```
[List Filtering](https://www.codewars.com/kata/53dbd5315a3c69eed20002dd/train/javascript)
```javascript
function filter_list(l) {
    let newList = [];
    l.forEach(el => {
        if ( typeof el === 'number' ) {
            newList.push(el);
        }
    });
    return newList;
}
```
[Two to One](https://www.codewars.com/kata/5656b6906de340bd1b0000ac/train/javascript)
```javascript
function longest(s1, s2) {
    let one = s1.concat(s2);
    let set = new Set(one.split(''))
    let a = Array.from(set).sort();
    return a.join('');
}
```
[You're a square!](https://www.codewars.com/kata/54c27a33fb7da0db0100040e/train/javascript)
```javascript
var isSquare = function(n){

  return (Number.isInteger(Math.sqrt(n)) || n === 0 ) ? true : false;   
}
```
[Inside Out Strings](https://www.codewars.com/kata/57ebdf1c2d45a0ecd7002cd5/train/javascript)
```javascript
function insideOut(x){
    let newArr = [];
    x.split(' ').forEach(word => {
        wordA = word.split('');
        if (wordA.length % 2) {
            // odd
            let left = wordA.splice(0, Math.floor(wordA.length / 2)).reverse();
            let right = wordA.splice(1).reverse();
            newArr.push(left.concat(wordA.concat(right)).join(''));

        } else {
            // even
            let left = wordA.splice(0, wordA.length/2).reverse();
            let right = wordA.reverse();
            newArr.push(left.concat(right).join(''));
        }
    });

    return newArr.join(' ');
}
```
[Categorize New Member](https://www.codewars.com/kata/5502c9e7b3216ec63c0001aa/train/javascript)
```javascript
function openOrSenior(data){
    let arr = [];
    for ( let i = 0; i < data.length; i++ ) {        
        if ( data[i][0] > 54  && data[i][1] > 7 ) {
            arr.push("Senior");
        } else {
            arr.push("Open");
        }
    }
    return arr;
}
```