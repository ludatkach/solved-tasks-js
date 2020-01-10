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
JavaScript:
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
