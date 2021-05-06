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
[Sort the odd](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/train/javascript)
```javascript
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
[RGB To Hex Conversion](https://www.codewars.com/kata/513e08acc600c94f01000001/train/javascript)
```javascript
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
[Bit Counting](https://www.codewars.com/kata/526571aae218b8ee490006f4/train/javascript)
```javascript
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
[Array.diff](https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript)
```javascript
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
[Find the next perfect square!](https://www.codewars.com/kata/56269eb78ad2e4ced1000013/train/javascript)
```javascript
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
[Sum of two lowest positive integers](https://www.codewars.com/kata/558fc85d8fd1938afb000014/train/javascript)
```javascript
function sumTwoSmallestNumbers(numbers) {  
  let sum = 0;
    numbers.sort((a,b) => a - b);
    sum = numbers[0] + numbers[1];
    return sum;
}
```
[Odd or Even?](https://www.codewars.com/kata/5949481f86420f59480000e7/train/javascript)
```javascript
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
```
[Sum of Odd Cubed Numbers](https://www.codewars.com/kata/580dda86c40fa6c45f00028a/train/javascript)
```javascript
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
[Squares sequence](https://www.codewars.com/kata/5546180ca783b6d2d5000062/train/javascript)
```javascript
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
````
[Square Every Digit](https://www.codewars.com/kata/546e2562b03326a88e000020/train/javascript)
```javascript
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
[Filter the number](https://www.codewars.com/kata/55b051fac50a3292a9000025/train/javascript)
```javascript
var FilterString = function(value) {
  let num='';
    for ( let i = 0; i < value.length; i++ ) {
        if ( isNaN(value[i]) === false)  {
            num +=value[i];
        }

    }
    return +num;
}
```
[Sum of the first nth term of Series](https://www.codewars.com/kata/555eded1ad94b00403000071/train/javascript)
```javascript
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
[Numbers to Letters](https://www.codewars.com/kata/57ebaa8f7b45ef590c00000c/train/javascript)
```javascript
function switcher(x){
    let arr = " ?!abcdefghijklmnopqrstuvwxyz-".split('').reverse();
    let newArr = x.map( Number);
    let string = '';
    newArr.forEach(el => {string += arr[el]});
    return string;
}
```
[Regex validate PIN code](https://www.codewars.com/kata/55f8a9c06c018a0d6e000132/train/javascript)
```javascript
function validatePIN (pin) {
    return pin.match(/^\d{4}$|^\d{6}$/) ? true : false;
}
```
[Powers of 3](https://www.codewars.com/kata/57be674b93687de78c0001d9/train/javascript)
```javascript
function largestPower(n){
    let k = 0;
    for (; Math.pow(3,k) < n; k++);
    return --k;
}
```
[Power of two](https://www.codewars.com/kata/534d0a229345375d520006a0/train/javascript)
```javascript
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
```
[Factorial](https://www.codewars.com/kata/57a049e253ba33ac5e000212/train/javascript)
```javascript
function factorial(n){
  return n === 1 || n === 0 ? 1 :  n * factorial(n-1);
}
```
[Difference Of Squares](https://www.codewars.com/kata/558f9f51e85b46e9fa000025/train/javascript)
```javascript
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
[Tail Swap](https://www.codewars.com/kata/5868812b15f0057e05000001/train/javascript)
```javascript
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
[Reverse words](https://www.codewars.com/kata/5259b20d6021e9e14c0010d4/train/javascript)
```javascript
function reverseWords(str) {
  let words = str.split(' ');
  let arrWords = [];
  let one;
  for (let i = 0; i < words.length; i++ ) {
    one = words[i].split('').reverse().join('');
    arrWords.push(one);
  }
  return arrWords.join(' ');
}
```
[Friend or Foe?](https://www.codewars.com/kata/55b42574ff091733d900002f/train/javascript)
```javascript
function friend(friends){
  let myFriends = [];
  for ( let i = 0; i < friends.length; i++ ) {
      if ( friends[i].length  === 4 ) {
          myFriends.push(friends[i]);
      }
  }
  return myFriends;
}
```
[Find the stray number](https://www.codewars.com/kata/57f609022f4d534f05000024/train/javascript)
```javascript
function stray(numbers) {
  for ( let i = 0; i < numbers.length; i++ ) {
      if ( numbers.indexOf(numbers[i]) === numbers.lastIndexOf(numbers[i])) {
        return numbers[i];
      }
  }
}
```
[The highest profit wins!](https://www.codewars.com/kata/559590633066759614000063/train/javascript)
```javascript
function minMax(arr){
    let returnArr = [];
    returnArr.push(  Math.min(...arr) );
    returnArr.push( Math.max(...arr) );
    return returnArr;
}
```
[Braces status](https://www.codewars.com/kata/58983deb128a54b530000be6/train/javascript)
```javascript
function bracesStatus(string){
    let result = [];
    let retCode = true;
    string.split('').filter(val=>'()[]{}'.indexOf(val) >= 0).forEach(val=>{
        if ('([{'.indexOf(val) >= 0) {
            result.push(val)
        } else {
            let pairs = {
                '(':')',
                '[':']',
                '{':'}',
            };

            if( val !== pairs[result.pop()]){
                retCode = false
            }
        }
    });

    return retCode && result.length === 0;
}
```
[Break camelCase](https://www.codewars.com/kata/5208f99aee097e6552000148/train/javascript)
```javascript
// complete the function
function solution(string) {
     return string.replace(/([A-Z])/g, (match) => ' ' + match);
}
```
[Jaden Casing Strings](https://www.codewars.com/kata/5390bac347d09b7da40006f6/train/javascript)
```javascript
String.prototype.toJadenCase = function () {
    return this.replace(/(^|\s)([a-z])/g, (match) => match.toUpperCase());
};
```
[Who likes it?](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/train/javascript)
```javascript
function likes(names) {
    const phraseOne = ' likes this';
    const phraseMany = ' like this';
    if ( names.length === 0 ) {
        return 'no one' + phraseOne;
    }
    for ( let i = 0; i < names.length; i++ ) {
        if ( names.length === 1) {
            return names[i] + phraseOne;
        }
        if ( names.length === 2) {
            return names[i] +' and ' + names[i+1] + phraseMany;
        }

        if ( names.length === 3) {
            return names[i] + ', ' + names[i+1] + ' and ' + names[i+2] + phraseMany;
        }

        if ( names.length > 3) {
            return names[i] + ', ' + names[i+1] + ' and ' + (names.length - 2) + ' others' + phraseMany;
        }
    }
}
```
[Equal Sides Of An Array](https://www.codewars.com/kata/5679aa472b8f57fb8c000047/train/javascript)
```javascript
function findEvenIndex(arr)
{
        for (let i = 0; i < arr.length; i++) {
        let leftArr = i < 1 ? [] : arr.slice(0, i);
        let leftSum = leftArr.length ? leftArr.reduce((acc, val) => acc + val) : 0;
        let rightArr = i >= arr.length - 1 ? [] : arr.slice(i + 1);
        let rightSum = rightArr.length ? rightArr.reduce((acc, val) => acc + val) : 0;
        if (leftSum === rightSum) {
            return i;
        }
    }
    return -1;
}
```
[Triple trouble](https://www.codewars.com/kata/55d5434f269c0c3f1b000058/train/javascript)
```javascript
function tripledouble(num1, num2) {
    let matchNum = String(num1).match(/(\d)\1\1/g);
    for(let i = 0;  matchNum && i < matchNum.length; i++) {
        let sub = matchNum[i].slice(1);
        if(String(num2).search(sub) >= 0) {
            return 1;
        }
    }
    return 0;
}
```
[Summing a number's digits](https://www.codewars.com/kata/52f3149496de55aded000410/train/javascript)
```javascript
function sumDigits(number) {
    let sum = 0;
    let absNum = Math.abs(number);
    let numStr = String(absNum).split('').map(val => +val);
    for ( let i = 0;  i < numStr.length; i++ ) {
        sum += numStr[i];
    }
    return sum;
}
```
[Form The Minimum](https://www.codewars.com/kata/5ac6932b2f317b96980000ca/train/javascript)
```javascript
function minValue(values){
    let set = new Set(values);
    let arr = Array.from(set).sort();    
    let newNum = arr.splice(0, arr.length);
    return +newNum.join('');
}
```
[Testing 1-2-3](https://www.codewars.com/kata/54bf85e3d5b56c7a05000cf9/train/javascript)
```javascript
var number=function(array){
    let newArr = [];
    for (let i = 0; i < array.length; i++ ) {
        let item = (i+1) + ": " + array[i];
        newArr.push(item);
    }
    return newArr;
}
```
[Decode the Morse code](https://www.codewars.com/kata/54b724efac3d5402db00065e/train/javascript)
```javascript
decodeMorse = function(morseCode){
    let decodePhrase = [];
    let arrWords = morseCode.trim().split("   ");
    let arrNew = arrWords.map(val => val.split(' '));
    for ( let i = 0; i < arrNew.length; i++ ) {
        let phrase = [];
        for (let j = 0; j < arrNew[i].length; j++ ) {            
            let element = MORSE_CODE[arrNew[i][j]];
            phrase.push(element);
        }
        decodePhrase.push(phrase.join(''));        
    }    
    return decodePhrase.join(' ');
}
```
[Decode the Morse code](https://www.codewars.com/kata/54b724efac3d5402db00065e/train/javascript)
```javascript
decodeMorse = function(morseCode){
  return morseCode.trim().split('   ').map(word=>word.split(' ').map(letter=>MORSE_CODE[letter]).join('')).join(' ');

}
```
[Consecutive strings](https://www.codewars.com/kata/56a5d994ac971f1ac500003e/train/javascript)
```javascript
function longestConsec(strarr, k) {
    let strLongestWord = '';
    for (let i = 0; i < strarr.length - k + 1; i++) {
        let word = '';
        for (let j = 0; j < k; j++) {
            word = word.concat(strarr[i + j]);
        }
        if (strLongestWord.length < word.length) {
            strLongestWord = word;
        }
    }
    return strLongestWord;
}
```
[Sum of a sequence](https://www.codewars.com/kata/586f6741c66d18c22800010a/train/javascript)
```javascript
const sequenceSum = (begin, end, step) => {
    let sum = 0;
    for (let i = begin; i <= end; i += step) {
        if (begin < end) {
            sum += i;
        }
        else {
            return i;
        }        
    }
    return sum;
};
```
[Odd-Even String Sort](https://www.codewars.com/kata/580755730b5a77650500010c/train/javascript)
```javascript
function sortMyString(S) {
    let odd = [];
    let even = [];
    let arrWords = S.split('');
    for ( let i = 0; i < arrWords.length; i++ ) {
        if ( i % 2 === 0 || i === 0) {
            even.push(arrWords[i]);
        } else {
            odd.push(arrWords[i]);
        }
    }
    even.push(' ');
    return even.concat(odd).join('');
}
```
[Find the missing letter](https://www.codewars.com/kata/5839edaa6754d6fec10000a2/train/javascript)
```javascript
function findMissingLetter(array)
{
  let alphabet = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
  let indxL = alphabet.indexOf(array[0]);
  for ( let i = 1; i < array.length; i++ ){
      if ( array[i] !== alphabet.charAt(indxL+i)) {
          return alphabet.charAt(indxL+i);
      }
  }
}
```
[Chess Fun #1: Chess Board Cell Color](https://www.codewars.com/kata/5894134c8afa3618c9000146/train/javascript)
```javascript
function chessBoardCellColor(cell1, cell2) {
    if ( (cell1.match(/([ACEG])([1357])/) || cell1.match(/([BDFH])([2468])/)) && (cell2.match(/([ACEG])([1357])/) || cell2.match(/([BDFH])([2468])/)) ||
    (cell1.match(/([ACEG])([2468])/) || cell1.match(/([BDFH])([1357])/)) && (cell2.match(/([ACEG])([2468])/) || cell2.match(/([BDFH])([1357])/))) {
        return true;
    }
    return false;
  
}
```
[Dan's great power generator](https://www.codewars.com/kata/582c42e0f000e54a7d000086/train/javascript)
```javascript
function danspower(num, power) {
   let result = 0;
   let number =  Math.pow(num,power);
   if ( number % 2 ) {
       let arr = String(number).split('');
       let digit = arr[arr.length-1];
       if (  digit > 4 ) {
        result = (Math.round(number / 10)) * 10;
        return result;
       } else {
        result = (Math.floor(number / 10)) * 10;
        return result;
       }       
   } else {
       return Math.pow(num,power);
   } 
   return result; 
}
```
[Return substring instance count](https://www.codewars.com/kata/5168b125faced29f66000005/train/javascript)
```javascript
function solution(fullText, searchText){
    let m = fullText.match(new RegExp(searchText, 'g'))
    return m ? m.length : 0;
}
```
[Pick peaks](https://www.codewars.com/kata/5279f6fe5ab7f447890006a7/train/javascript)
```javascript
function pickPeaks(arr){
    let arrPos = [];
    let arrPeaks = [];
    let uphillVal = 0;
    let uphillIdx = -1;

    for (let i = 1; i < arr.length; i++) {
        if (arr[i - 1] < arr[i]) {

            uphillVal = arr[i];
            uphillIdx = i;
        } else if (arr[i - 1] > arr[i]) {
            if (uphillIdx > 0) {
                arrPos.push(uphillIdx);
                arrPeaks.push(uphillVal);
                uphillIdx = -1;
            }
        }
    }
    return { pos: arrPos, peaks: arrPeaks };
}
```
[No oddities here](https://www.codewars.com/kata/51fd6bc82bc150b28e0000ce/train/javascript)
```javascript
function noOdds( values ){
    let result = [];
    for (let i = 0; i < values.length; i++ ) {
        if ( i === 0 || i % 2 === 0 )
        result.push(values[i]);
    }
    return result;
}
```
[Complete The Pattern #2](https://www.codewars.com/kata/55733d3ef7c43f8b0700007c/train/javascript)
```javascript
function pattern(n){
    let num = '';
    let newArr = [];
    for (let i = n; i > 0; i--) {
        num += String(i);
        newArr.push(num);
    }
    return newArr.reverse().join('\n');
}
```
[Format words into a sentence](https://www.codewars.com/kata/51689e27fe9a00b126000004/train/javascript)
```javascript
function formatWords(words){
    words = [].concat.apply([], words).filter(val => val.length > 0);
    if (words.length == 0) {
        return '';
    } else if (words.length == 1) {
        return words[0];
    } else {
        return words.splice(0, words.length - 1).join(', ') + " and " + words[0];
    }
}
```
[Evens times last](https://www.codewars.com/kata/5a1a9e5032b8b98477000004/train/javascript)
```javascript
function evenLast(numbers) {
   let sum = 0;
   if ( numbers.length === 0 ) {
     return 0;
   }
   let last = numbers[numbers.length-1];
   for ( let i = 0; i < numbers.length; i++ ) {
       if ( i % 2 === 0 ) {
           sum += numbers[i];
       }
   }
   return sum * last;
}
```
[Find the first non-consecutive number](https://www.codewars.com/kata/58f8a3a27a5c28d92e000144/train/javascript)
```javascript
function firstNonConsecutive (arr) {
  for (let i = 0; i < arr.length - 1; i++) {
        let a = arr[i + 1] - arr[i];
        if (a > 1) {
            return arr[i+1];
        } 
    }
    return null;
}
```
[Complete The Pattern #1](https://www.codewars.com/kata/5572f7c346eb58ae9c000047/train/javascript)
```javascript
function pattern(n){
    let arr = [];
    for (let i = 1; i <= n; i++) {
        arr.push(String(i).repeat(i))
    }
    return arr.join('\n');
}
```
[IP Validation](https://www.codewars.com/kata/515decfd9dcfc23bb6000006/train/javascript)
```javascript
function isValidIP(str) {
  return str.split('.').filter(val => val.match(/^0$|^[1-9]+\d*$/) && +val < 256 && +val >= 0).length === 4;   
}
```
[Largest 5 digit number in a series](https://www.codewars.com/kata/51675d17e0c1bed195000001/train/javascript)
```javascript
function solution(digits){
    let strNum = String(digits);
    let max = 0;
    for (let i = 0; i < strNum.length - 4; i++) {
        let number = strNum.slice(i, i + 5);
        if (+number > max) {
            max = +number;
        }
    }
    return max;
}
```
[Is this a triangle?](https://www.codewars.com/kata/56606694ec01347ce800001b/train/javascript)
```javascript
function isTriangle(a,b,c)
{
  if ( a + b > c && a + c > b && c + b > a ) {
    return true;
  } else {
   return false;
  }
}
```
[Stringy Strings](https://www.codewars.com/kata/563b74ddd19a3ad462000054/train/javascript)
```javascript
function stringy(size) {
  let result = '';
  for ( let i = 0; i < size; i++ ) {
    if ( i === 0 || i % 2 === 0 ) {
      result += '1';
    } else {
      result += '0';
    }
  }
  return result;
}
```
[Rock Paper Scissors!](https://www.codewars.com/kata/5672a98bdbdd995fad00000f)
```javascript
const rps = (p1, p2) => {
  if ( (p1 === 'scissors' && p2 === 'paper') || (p1 === 'rock' && p2 === 'scissors') || (p1 === 'paper' && p2 === 'rock') ) {
    return 'Player 1 won!';
  }
  if ( p1 === 'paper'  && p2 === 'scissors' || p1 === 'scissors' && p2 === 'rock' || p1 === 'rock' && p2 === 'paper' ) {
    return 'Player 2 won!';
  } 
  
  if ( p1 === p2 ) {
  return 'Draw!';
  }
};
```
[Are You Playing Banjo?](https://www.codewars.com/kata/53af2b8861023f1d88000832/train/javascript)
```javascript
function areYouPlayingBanjo(name) {
    let strName = name.split('');
    if ( strName[0] === 'R' || strName[0] === 'r' ) {
        return name + " plays banjo";
    } else {
        return name + " does not play banjo";
    }
}
```
[The Supermarket Queue](https://www.codewars.com/kata/57b06f90e298a7b53d000a86/train/javascript)
```javascript
function queueTime(customers, n) {
    let registers = [];
    let queueTime = 0;
    if ( customers.length === 0 ) {
      return 0;
    }
    for (let i = 0; customers.length && i < n; i++) {
        registers.push(customers.shift())
    }
    do {
        registers.sort((a, b) => a - b);
        let minTime = registers[0];
        queueTime += minTime;
        registers = registers.map(val => val - minTime).filter(val => val > 0);
        let openRegisters = n - registers.length;
        for (let i = 0; customers.length && i < openRegisters; i++) {
            registers.push(customers.shift())
        }
    } while (registers.length);
    return queueTime;
}
```
[Will you make it?](https://www.codewars.com/kata/5861d28f124b35723e00005e/train/javascript)
```javascript
const zeroFuel = (distanceToPump, mpg, fuelLeft) => {
  return (( mpg * fuelLeft > distanceToPump) || ( mpg * fuelLeft === distanceToPump )) ? true : false;
};
```
[Maximum Length Difference](https://www.codewars.com/kata/5663f5305102699bad000056/train/javascript)
```javascript
function mxdiflg(a1, a2) {
    if ( a1.length === 0 || a2.length === 0 ) {
        return -1;
    }
    let maxArr = [];
    if ( a1.length > a2.length ) {
        for ( let i = 0; i < a1.length; i++ ) {
            for ( let j = 0; j < a2.length; j++ ) {
                let result = Math.abs(a1[i].length - a2[j].length);
                maxArr.push(result);
            }
        }
    } else {
        for ( let i = 0; i < a2.length; i++ ) {
            for ( let j = 0; j < a1.length; j++ ) {
                let result = Math.abs(a2[i].length - a1[j].length);
                maxArr.push(result);
            }
        }
    }
    maxArr.sort((a,b) => b - a);
    return maxArr[0]; 
}
```
[Transportation on vacation](https://www.codewars.com/kata/568d0dd208ee69389d000016/train/java)
```javascript
function rentalCarCost(d) {
  return d > 0 && d < 3 ? 40 * d : ( d < 7 ? 40 * d - 20 : ( d >= 7 ? 40 * d - 50 : 0));
}
```
[Short Long Short](https://www.codewars.com/kata/50654ddff44f800200000007/train/javascript)
```javascript
function solution(a, b){
  if (  a.length <  b.length ) {
    return a.concat(b) + a;
  } else {
    return b.concat(a) + b;
  }
}
```
[Simple parenthesis removal](https://www.codewars.com/kata/5a3bedd38f27f246c200005f/train/javascript)
```javascript
function solve(s) {
    let m = s.replace(/\(([a-z])/g, "(+$1").match(/(\-\()|(\+\()|(\()|(\))|(\+[a-z])|(\-[a-z])|([a-z])/gi);
    let vec = [];
    if(m) {
        let braces = [];
    
        m.forEach(val=>{
            switch (val) {
                case '+(':
                case '-(':
                case '(':
                    braces.push(val);
                    break;
                case ')':
                    braces.pop();
                    break;
                default:
                    let inversion = braces.filter(val=>val==='-(').length % 2;
                    if(inversion) {
                        let lex = val.split('');
                        if(lex.length > 1) {
                            lex[0] = lex[0]==='+' ? '-' : '+';
                        }
                        val = lex.join('');
                    }
                    vec.push(val);
            }

        });
    }

    return vec.join('').replace(/^\+/,"");
}
```
[Factorial](https://www.codewars.com/kata/54ff0d1f355cfd20e60001fc/train/javascript)
```javascript
function factorial(n)
{
  let product = 1;
  if ( n < 0 || n > 12 ) {
    throw RangeError;
  } 
  if( n === 0 ) {
      return 1;
  }
  for (let i = 1; i <= n; i++ ) {
    product *= i;
  }
  return product;
}
```
[The Office VI - Sabbatical](https://www.codewars.com/kata/57fe50d000d05166720000b1/train/javascript)
```javascript
function sabb(x, val, happ){
    let count = 0;
    'sabticl'.split('').forEach(letter=> {
        count += x.split('').filter(val=>val===letter).length;
    });
    let sum = count + val + happ;
    return sum > 22 ? 'Sabbatical! Boom!' : 'Back to your desk, boy.';
}
```
[Palindrome chain length](https://www.codewars.com/kata/525f039017c7cd0e1a000a26/train/javascript)
```javascript
var palindromeChainLength = function(n) {
    let steps = 0;
    for(let str = String(n); str !== str.split('').reverse().join(''); steps++) {
        let num = +str.split('').reverse().join('');
        let sum = +str + num;
        str = String(sum);
    }

    return steps;
};
```
[Words to sentence](https://www.codewars.com/kata/57a06005cf1fa5fbd5000216/train/javascript)
```javascript
function wordsToSentence(words) {
  
  return words.join(' ');
}
```
[Find the Difference in Age between Oldest and Youngest Family Members](https://www.codewars.com/kata/5720a1cb65a504fdff0003e2/train/javascript)
```javascript
function differenceInAges(ages){
    let result = [];
    let minR = Math.min(...ages);
    let maxR = Math.max(...ages);
    result.push(minR);
    result.push(maxR);
    result.push(maxR - minR);
    return result;
}
```
[Anagram Detection](https://www.codewars.com/kata/529eef7a9194e0cbc1000255/train/javascript)
```javascript
// write the function isAnagram
var isAnagram = function(test, original) {
    let newTest = test.toLowerCase().split('').sort().join('');
    let newOriginal = original.toLowerCase().split('').sort().join('');
    if ( newTest === newOriginal) {
        return true;
    }
    return false;
};
```
[Sort Numbers](https://www.codewars.com/kata/5174a4c0f2769dd8b1000003/train/javascript)
```javascript
function solution(nums){
   let newArr = [];
   if (nums === null || nums.length === 0 ) {
        return [];
    }  else {
       newArr = nums.sort((a,b) => a - b);
    } 
    return newArr;
}
```
[Gauß needs help! (Sums of a lot of numbers).](https://www.codewars.com/kata/54df2067ecaa226eca000229/train/javascript)
```javascript
function f(n) {
    if (typeof n === 'number' && n > 0 && n % 1 === 0) {
        for(let i = n-1; i > 0; i--) {
            n += i;
        }
        return n;
    }
    return false;
};
```
[Merge two arrays](https://www.codewars.com/kata/583af10620dda4da270000c5/train/javascript)
```javascript
function mergeArrays(a, b) {
    let result = [];
    for (let i = 0; i < Math.max(a.length, b.length); i++) {
        if(a.length > i) {
            result.push(a[i]);
        }
        if(b.length > i) {
            result.push(b[i]);
        }
    }
    return result;
}
```
[Remove exclamation marks](https://www.codewars.com/kata/57a0885cbb9944e24c00008e)
```javascript
function removeExclamationMarks(s) {
    let str = s.split('');
    for (let i = 0; i < str.length; i++ ) {
        if ( str[i].match(/!/g)) {
          str[i] = '';          
        }
      } 
      return str.join('');
}
```
[How many lightsabers do you own?](https://www.codewars.com/kata/51f9d93b4095e0a7200001b8/train/javascript)
```javascript
function howManyLightsabersDoYouOwn(name) {
  if ( name === 'Zach') {
    return 18;
  } 
  return 0;
}  
```
[Opposites Attract](https://www.codewars.com/kata/555086d53eac039a2a000083/train/javascript)
```javascript
function lovefunc(flower1, flower2){
   return( ((flower1 % 2) && (flower2 % 2 === 0 )) || (( flower2 % 2) && (flower1 % 2 === 0 ))) ? true : false; 
}
```
[Grasshopper - Personalized Message](https://www.codewars.com/kata/5772da22b89313a4d50012f7/train/javascript)
```javascript
function greet (name, owner) {
  if ( name === owner ) {
    return 'Hello boss';
  }
  return 'Hello guest';
}
```
[Exclusive "or" (xor) Logical Operator](https://www.codewars.com/kata/56fa3c5ce4d45d2a52001b3c/train/javascript)
```javascript
function xor(a, b) {
 return  ( a === true && b === false  || b === true && a === false ) ? true : false;
 
}
```
[Will there be enough space?](https://www.codewars.com/kata/5875b200d520904a04000003/train/javascript)
```javascript
function enough(cap, on, wait) {
let pas = cap - on;
  if ( pas - wait >= 0 ) {
    return 0;
  }
  if ( pas - wait < 0 ) {
    return Math.abs(pas - wait);
  }
}
```
[Volume of a Cuboid](https://www.codewars.com/kata/58261acb22be6e2ed800003a/train/javascript)
```javascript
var Kata;

Kata = (function() {
  function Kata() {}

  Kata.getVolumeOfCuboid = function(length, width, height) {
    
   return length * width * height;
  };

  return Kata;

})();
```
[Expressions Matter](https://www.codewars.com/kata/5ae62fcf252e66d44d00008e/train/javascript)
```javascript
function expressionMatter(a, b, c) {
  let num1 = a * (b + c);
  let num2 = a * b * c;
  let num3 = a + b * c;
  let num4 =(a + b) * c;
  let num5 = a + b + c;
  
  return Math.max(num1, num2, num3, num4, num5);
}
```
[Watermelon](https://www.codewars.com/kata/55192f4ecd82ff826900089e/train/javascript)
```javascript
function divide(weight){
  if (weight === 2) {
    return false;
  }
  return ( weight % 2 === 0 ) ? true : false;
}
```
[Filter out the geese](https://www.codewars.com/kata/57ee4a67108d3fd9eb0000e7/train/javascript)
```javascript
function gooseFilter (birds) {
  var geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
    let result = [];
    for ( let i = 0; i < birds.length;) {
      if ( geese.includes(birds[i])) {
        birds.splice(i, 1);
      } else {
        i++;
      }
    }
    return birds;
}
```
[Alternate capitalization](https://www.codewars.com/kata/59cfc000aeb2844d16000075/train/javascript)
```javascript
function capitalize(s){
    let result1 = '';
    let result2 = '';
    let arrayRes = [];
    for (let i = 0; i < s.length; i++ ) {
        if ( i % 2 === 0 ) {
            let letter = s[i].toUpperCase();
            result1 += letter;
        } else {
            result1 += s[i];
        }
    }
    arrayRes.push(result1);
    for ( let i = 0; i < s.length; i++ ) {
        if ( i % 2 ) {
            let letter = s[i].toUpperCase();
            result2 += letter;
        } else {
            result2 += s[i];
        }
    }
    arrayRes.push(result2);
    return arrayRes;
};
```
[Moves in squared strings (I)](https://www.codewars.com/kata/56dbe0e313c2f63be4000b25/train/javascript)
```javascript
function vertMirror(strng) {
    let newArr = strng.split('\n');
    let result = [];
    let val = [];
    for ( let i = 0; i < newArr.length; i++ ){
        val = newArr[i].split('').reverse().join('');
        result.push(val);
    }
    return result.join('\n');
}

function horMirror(strng) {
    let newArr = strng.split('\n').reverse();
    return newArr.join('\n');
}


function oper(fct, s) {
    return fct(s);
}
```
[Take a Ten Minute Walk](https://www.codewars.com/kata/54da539698b8a2ad76000228/train/javascript)
```javascript
function isValidWalk(walk) {
    if (walk.length != 10) {
        return false;
    }
    let x = 0;
    let y = 0;
    walk.forEach(element => {
        switch (element) {
            case 'n':
                y++;
                break;
            case 's':
                y--;
                break;
            case 'e':
                x++;
                break;
            case 'w':
                x--;
                break;
        }
    });
    if (x || y) {
        return false;
    }

    return true;
}
```
[Build Tower](https://www.codewars.com/kata/576757b1df89ecf5bd00073b/train/javascript)
```javascript
function towerBuilder(nFloors) {
    let result = [];
    for (let i = 0; i < nFloors; i++) {
        let row = '';
        let spaces = nFloors - i - 1;
        let stars = i;
        for (let j = 0; j < spaces; j++) {
            row += ' ';
        }
        for (let j = 0; j < stars; j++) {
            row += '*';
        }
        row += '*';
        for (let j = 0; j < stars; j++) {
            row += '*';
        }
        for (let j = 0; j < spaces; j++) {
            row += ' ';
        }
        result.push(row);
    }
    return result;
}
```
[Building Strings From a Hash](https://www.codewars.com/kata/51c7d8268a35b6b8b40002f2/train/javascript)
```javascript
//https://docs.google.com/spreadsheets/d/1QQaljCrFc7n3ZPZWv69sZYvmcnXqqLHn7OeJXGcxRJc/edit?usp=sharing

```
[Building Strings From a Hash](https://www.codewars.com/kata/51c7d8268a35b6b8b40002f2/train/javascript)
```javascript
function solution(pairs){
  return Object.keys(pairs).map(key=> key + ' = ' + pairs[key]).join(',');
}
```
[Vasya - Clerk](https://www.codewars.com/kata/555615a77ebc7c2c8a0000b8/train/javascript)
```javascript
function tickets(peopleInLine){
    let bank = {
        25: 0,
        50: 0,
        100: 0
    };

    for (let i = 0; i < peopleInLine.length; i++) {
        let val = peopleInLine[i];
        bank[val]++;
        let change = val - 25;

        while (change) {
            let d25 = change / 25;
            let d50 = change / 50;
            if (d50 >= 1 && bank[50] > 0) {
                change -= 50;
                bank[50]--;
            } else if (d25 >= 1 && bank[25] > 0) {
                change -= 25;
                bank[25]--;
            } else {
                return "NO";
            }
        }
    }

    return "YES";
}
```
[SQL Basics: Simple GROUP BY](https://www.codewars.com/kata/58111f4ee10b5301a7000175/train/sql)
```sql
SELECT age, count(*) as people_count from people
GROUP BY age; 
```
[Count the Digit](https://www.codewars.com/kata/566fc12495810954b1000030/train/javascript)
```javascript
function nbDig(n, d) {
    let result = [];
    let count = 0;
    for (let i = 0; i <= n; i++) {
        result.push(i ** 2);
    }
    for (let i = 0; i < result.length; i++) {
        count += String(result[i]).split('').filter(val => val === String(d)).length;
    }
    return count;
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
[Find the middle element](https://www.codewars.com/kata/545a4c5a61aa4c6916000755/train/javascript)
```javascript
var gimme = function (inputArray) {
    let sorted = [...inputArray].sort((a, b) => a - b);
    return inputArray.findIndex(val => val === sorted[1]);
};
```
[You're a square!](https://www.codewars.com/kata/54c27a33fb7da0db0100040e/train/javascript)
```javascript
var isSquare = function(n){
  if ( n < 0 ) {
    return false;
  }
  return (Number.isInteger(Math.sqrt(n))) ? true : false;
}
```
[Triple Trouble](https://www.codewars.com/kata/5704aea738428f4d30000914/train/javascript)
```javascript
function tripleTrouble(one, two, three){
  let str = '';
  for ( let i = 0; i < one.length; i++ ) {
    str += one[i];
    str += two[i];
    str += three[i];
  }
  return str;
 }
```
[Convert string to camel case](https://www.codewars.com/kata/517abf86da9663f1d2000003/train/javascript)
```javascript
function toCamelCase(str){
    let newStrArr = str.replace(/[^a-zA-Z]/g, ' ').split(' ');
    for ( let i = 0; i < newStrArr.length; i++ ) {
        let newWord = newStrArr[i].split('');
        if ( i > 0 ) {
            let letter = newWord.splice(0,1).join('').toUpperCase();
            let myStr = newWord.join('');
            newStrArr[i] = letter.concat(myStr);
        }
    }
    return newStrArr.join('');
}
```
[Number Of Occurrences](https://www.codewars.com/kata/52829c5fe08baf7edc00122b/train/javascript)
```javascript
Array.prototype.numberOfOccurrences = function(val) {
  let count = 0;
  for ( let i = 0; i < this.length; i++ ) {
    if ( this[i] === val ) {
      count++;
    }
  }
  return count;
}
```
[Are they the "same"?](https://www.codewars.com/kata/550498447451fbbd7600041c/train/javascript)
```javascript
function comp(array1, array2){
    if (array1 === null || array2 === null || array1.length != array2.length) {
        return false;
    }
    
    if(!array1.length) {
        return true;
    }

    array1.sort((a, b) => a - b);
    array2.sort((a, b) => a - b);
    for (let i = 0; i < array1.length; i++) {
        if (array2[i] != Math.pow(array1[i], 2)) {
            return false;
        }
    }
    return true;
}
```
[Functional Addition](https://www.codewars.com/kata/538835ae443aae6e03000547/train/javascript)
```javascript
function add(n) {
  return function(m) {return n+m;};
}
```
[Split Strings](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001/train/javascript)
```javascript
function solution(str){
   let newStr = '';
   let arrStr = [];
   for ( let i = 0; i <= str.length-1; i+=2 ) {
       if ( str.length % 2 === 0 ) {
           newStr += str[i] + str[i+1];
           arrStr.push(newStr);
           newStr ='';
       } 
       if ( str.length % 2 ) {
            if ( i === str.length-1 ){
                newStr += str[i] + '_';
                arrStr.push(newStr);
            } else {
                newStr += str[i] + str[i+1];
                arrStr.push(newStr);
                newStr ='';
            } 
       }
   }
   return arrStr;
}
```
[TV channels](https://www.codewars.com/kata/5836dce6966f8d1d43000007/train/javascript)
```javascript
function redarr(arr) {
    let newObj  = {};
    let newSet = new Set(arr);
    let newArr = Array.from(newSet).sort();
    for ( let  i = 0; i < newArr.length; i++ ) {
        newObj[String(i)] = newArr[i];
    }
    return newObj;
}
```
[Common array elements](https://www.codewars.com/kata/5a6225e5d8e145b540000127/train/javascript)
```javascript
function common(a,b,c){
    let objB = {};
    let objC = {};

    b.forEach(element => {
        objB[element] = element in objB ? objB[element] + 1 : 1;
    });
    c.forEach(element => {
        objC[element] = element in objC ? objC[element] + 1 : 1;
    });

    let summ = 0;
    a.forEach(element => {
        if(objB[element] > 0 && objC[element] > 0) {
            summ += element;
            objB[element]--;
            objC[element]--;
        }
    });

    return summ;
}
```
[Simple Fun #321: Scratch lottery II](https://www.codewars.com/kata/594a2758954a44749f000359/train/javascript)
```javascript
function scratch(lottery){
    let numbers = [5, 10, 20, 50, 100, 200, 500, 1000, 2000, 5000, 10000];
    let sum = 0;
    let oneElArr = [];
    for (let i = 0; i < lottery.length; i++) {
        oneElArr = lottery[i].split(' ');
        let myset = new Set();
        for (let j = 0; j < oneElArr.length - 1; j++) {
            if (oneElArr[j] !== '###') {
                myset.add(oneElArr[j]);
            }
        }
        if(myset.size < 2) {
            let amount = 0;
            let num = oneElArr[oneElArr.length-1];
            if (num === '###') {
                amount = 10000;
            } else if (numbers.includes(+num)) {
                amount = +num;
            } 
            sum += amount;
        }       
    }
    return sum;  
}
```
[Consonant value](https://www.codewars.com/kata/59c633e7dcc4053512000073/train/javascript)
```javascript
function solve(s) {
    let alphabetArr = [0, 'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'];
    let newArr = s.split(/[aeiou]/g);
    let sumArr = [];
    let sum = 0;
    for ( let i = 0; i < newArr.length; i++ ) {
        for ( let j = 0; j < newArr[i].length; j++ ) {
            if ( alphabetArr.includes(newArr[i][j])){
                sum += alphabetArr.indexOf(newArr[i][j]);
            }
        }
        sumArr.push(sum);
        sum = 0;
    }
    let result = Math.max(...sumArr);
    return result;
};
```
[Sums of Parts](https://www.codewars.com/kata/5ce399e0047a45001c853c2b/train/javascript)
```javascript
function partsSums(ls) {
    if ( ls === null || !ls.length ) {
      return [0];
    }
    let result = [];
    let sum = ls.reduce((acc, val) => acc + val);    
    result.push(sum);
    ls.forEach(element => result.push((sum -= element)));
    return result;
}
```
[Detect Pangram](https://www.codewars.com/kata/545cedaa9943f7fe7b000048/train/javascript)
```javascript
function isPangram(string){
    let alphabet = 'abcdefghijklmnopqrstuvwxyz';
    let newStr = string.toLowerCase().match(/[a-z]/g);
    let mySet = new Set(newStr);
    let arr = Array.from(mySet).sort().join('');
    if ( alphabet === arr ) {
        return true;
    }
    return false;
}
```
[Predict your age!](https://www.codewars.com/kata/5aff237c578a14752d0035ae/train/javascript)
```javascript
function predictAge(age1,age2,age3,age4,age5,age6,age7,age8){
  return Math.floor(Math.sqrt(age1*age1 + age2*age2 + age3*age3 + age4*age4 + age5*age5 + age6*age6 + age7*age7 + age8*age8)/2);
}
```
[A String of Sorts](https://www.codewars.com/kata/536c6b8749aa8b3c2600029a/train/javascript)
```javascript
function sortString(string,ordering) {
    let result = [];
    let stringArr = string.split('');
    let orderingArr = ordering.split('');
    let newOrdering = Array.from(new Set(orderingArr));

    newOrdering.forEach(element => {
        result.push(...stringArr.filter(val=>val === element));
        stringArr = stringArr.filter(val=>val !== element);
    });
    result.push(...stringArr);

    return result.join('');
}
```
[Sorted? yes? no? how?](https://www.codewars.com/kata/580a4734d6df748060000045/train/javascript)
```javascript
function isSortedAndHow(array) {
    let asc = array.every((element, index)=>{
        if(index>0) {
            return array[index-1] <= element;
        } else {
            return true;
        }
    });

    if(asc) {
        return 'yes, ascending'; 
    }

    let des = array.every((element, index)=>{
        if(index>0) {
            return array[index-1] >= element;
        } else {
            return true;
        }
    });

    if(des) {
        return 'yes, descending';
    }

    return 'no';
}
```
[Number of Decimal Digits](https://www.codewars.com/kata/58fa273ca6d84c158e000052)
```javascript
function digits(n) {
    let arrDigits = String(n).split('');
    let count = 0;
    for ( let i = 0; i < arrDigits.length; i++ ) {
        count++;
    }
    return count;
}
```
[Number of Decimal Digits](https://www.codewars.com/kata/58fa273ca6d84c158e000052/train/javascript)
```javascript
function digits(n) {
    let arrDigits = String(n).split('');
    let count = 0;
    for ( let i = 0; i < arrDigits.length; i++ ) {
        count++;
    }
    return count;
}
```
[Enumerable Magic #5- True for Just One?](https://www.codewars.com/kata/54599705cbae2aa60b0011a4/train/javascript)
```javascript
function one(arr, fun) {
    return arr.filter(value=>fun(value)).length === 1;
}
```
[Find all non-consecutive numbers](https://www.codewars.com/kata/58f8b35fda19c0c79400020f/train/javascript)
```javascript
function allNonConsecutive (arr) {
    let result = [];
    for (let j = 1; j < arr.length; j++) {
        if ((arr[j - 1] + 1) != arr[j]) {
            result.push({i:j,n:arr[j]});
        }
    }

    return result;
}
```
[Is it even?](https://www.codewars.com/kata/555a67db74814aa4ee0001b5/train/javascript)
```javascript
function testEven(n) {
  return ( Math.abs(n) % 2 === 0 ) ? true : false;
}
```
[All Star Code Challenge #18](https://www.codewars.com/kata/5865918c6b569962950002a1/train/javascript)
```javascript
function strCount(str, letter){  
  let count = 0;
  for ( let i = 0; i < str.length; i++ ) {
    if ( str[i] === letter ) {
      count++;
    }
  }
  return count;
}
```
[You Can't Code Under Pressure #1](https://www.codewars.com/kata/53ee5429ba190077850011d4/train/javascript)
```javascript
function doubleInteger(i) {
  
  return i*2;
}
```
[Grasshopper - Messi Goals](https://www.codewars.com/kata/55ca77fa094a2af31f00002a/train/javascript)
```javascript
var laLigaGoals = 43;
var championsLeagueGoals = 10;
var copaDelReyGoals = 5;

var totalGoals = laLigaGoals + championsLeagueGoals + copaDelReyGoals;
```
[N-th Power](https://www.codewars.com/kata/57d814e4950d8489720008db/train/javascript)
```javascript
function index(array, n){
  return  ( n < array.length ) ? (Math.pow(array[n], n)) : -1;
    
}
```
[What is between?](https://www.codewars.com/kata/55ecd718f46fba02e5000029/train/javascript)
```javascript
function between(a, b) {
  let arr = [];
  for ( let i = a; i <= b; i++ ) {
    arr.push(i);
  }
  return arr;
}
```
[Tip Calculator](https://www.codewars.com/kata/56598d8076ee7a0759000087/train/javascript)
```javascript
function calculateTip(amount, rating) {
    let tipCalc = {
        terrible: 0,
        poor: .05,
        good: .1,
        great: .15,
        excellent: .2
    };
    rating = rating.toLowerCase();
    let tip = 0;
    if (rating.toLowerCase() in tipCalc) {
        tip = tipCalc[rating];
        return Math.ceil(amount * tip);
    }
    return "Rating not recognised";
}
```
[Beginner Series #1 School Paperwork](https://www.codewars.com/kata/55f9b48403f6b87a7c0000bd/train/javascript)
```javascript
function paperwork(n, m) {
  if ( n < 0 || m < 0 ){
            return 0;
        }
  return n * m;
}
```
[No zeros for heros](https://www.codewars.com/kata/570a6a46455d08ff8d001002/train/javascript)
```javascript
function noBoringZeros(n) {
    let str = String(n).split('');
    str = str.reverse();
    for ( let i = 0; i < str.length; i++ ) {
        if ( str[i] != "0" ) {
            return +str.reverse().join('');
        } else {
            str.splice(str[i], 1);
            i--;
        }
    }
    return +str.reverse().join('');
}
```
[Coding 3min : Symmetric Sort](https://www.codewars.com/kata/5705aeb041e5befba20010ba/train/javascript)
```javascript
function sc(array){
    let sorted = array.sort((a,b) => a - b);
    let leftArr = [];
    let rightArr = [];
    for ( let i = 0; i < sorted.length; i++ ) {
        if ( i % 2 === 0 ) {
            leftArr.push(sorted[i]);
        } 
        if ( i % 2) {
            rightArr.push(sorted[i]);
        }
    }
    return leftArr.concat(rightArr.reverse());
}
```
[Is the string uppercase?](https://www.codewars.com/kata/56cd44e1aa4ac7879200010b/train/javascript)
```javascript
String.prototype.isUpperCase = function() {
  return /^[A-Z\s\W]+$/.test(this);
}
```
[Computer problem series #1: Fill the Hard Disk Drive](https://www.codewars.com/kata/5d49c93d089c6e000ff8428c/train/javascript)
```javascript
function save(sizes, hd) {
    let i = 0;
    for ( ; i < sizes.length; i++ ) {
      if( (hd -= sizes[i]) < 0 ) {
        return i;
      }
    }    
    return i;
}
```
[Find the Middle of the Product](https://www.codewars.com/kata/5ac54bcbb925d9b437000001/train/javascript)
```javascript
function findMiddle(str){
console.log(str);
    let nums = [];
    if ( str === null  || typeof str != 'string' ) {
      return -1;
    }
    for ( let i = 0; i < str.length; i++ ) {
        if ( /[0-9]/.test(str[i]) ) {
            nums.push(+str[i]);
        } 
    }
    if (nums.length === 0 ) {
        return -1;
    }
    let product = nums.reduce((acc,cur) => acc * cur);
    let sumArr = String(product).split('');
    if ( sumArr.length % 2 ) {
        return +sumArr[Math.floor(sumArr.length/2)];
    } 
    if ( sumArr.length % 2 === 0 ) {
        let result = [];
        result.push(sumArr[sumArr.length/2-1]);
        result.push(sumArr[sumArr.length/2]);
        return +result.join('');
    } 
    return -1;
    
}
```
[Find Screen Size](https://www.codewars.com/kata/5bbd279c8f8bbd5ee500000f/train/javascript)
```javascript
function findScreenHeight(width, ratio) {
    let arr = ratio.split(':');
    let height = (width * +arr[1]) / +arr[0];
    return '' + width + 'x' + height;
}
```
[Find the area of the rectangle!](https://www.codewars.com/kata/580a0347430590220e000091/train/javascript)
```javascript
function area(d,l){
  return ( d < l || d === l ) ? "Not a rectangle" : +((Math.sqrt(d**2 - l**2)) * l).toFixed(2);
}
```
[Integer Difference](https://www.codewars.com/kata/57741d8f10a0a66915000001/train/javascript)
```javascript
const intDiff = (arr, n) => {
    let count = 0;
    for (let i = 0; i < arr.length; i++ ) {
        for ( let j = i+1; j < arr.length; j++ ) {
            if ( Math.abs(arr[i] - arr[j]) === n ) {
                count++;
           }
        }            
    }
    return count;
}
```
[What dominates your array?](https://www.codewars.com/kata/559e10e2e162b69f750000b4/train/javascript)
```javascript
function dominator(arr) {
    let arrLength = arr.length;
    let obj = {};
    arr.forEach(element => {
        element in obj ? obj[element]++ : obj[element] = 1; 
    }); 
    let maxKey;
    let maxEl = Number.MIN_VALUE;
    for ( key in obj) {
        if (obj[key] >= maxEl){
            maxEl = obj[key]
            maxKey = +key;
        }
    }
    return ( obj[maxKey] > arrLength/2 ) ? maxKey : -1;
}
```
[Find all occurrences of an element in an array](https://www.codewars.com/kata/59a9919107157a45220000e1/train/javascript)
```javascript
const findAll = (array, n) => {
    if ( !array.includes(n) ) {
        return [];
    }
    let result = [];
    for ( let i = 0; i < array.length; i++ ) {
        if ( array[i] === n ) {
            result.push(i);
        }
    }
    return result;
}
```
[The Poet And The Pendulum](https://www.codewars.com/kata/5bd776533a7e2720c40000e5/train/javascript)
```javascript
function pendulum(values) {
    let left = [];
    let right = [];
    values.sort((a,b) => a - b);
    for ( let i = 0; i < values.length; i++ ) {
        if ( i % 2 === 0 ) {
            left.push(values[i]);
        } else {
            right.push(values[i]);
        }
    }
    return left.reverse().concat(right);
}

```
[Find min and max](https://www.codewars.com/kata/57a1ae8c7cb1f31e4e000130/train/javascript)
```javascript
function getMinMax(arr){
    let newArr = [];
    arr.sort((a,b) => a - b);
    newArr.push(arr[0], arr[arr.length-1]);
    return newArr;
};
```
[Halving Sum](https://www.codewars.com/kata/5a58d46cfd56cb4e8600009d/train/javascript)
```javascript
function halvingSum(n) {
console.log(n);
    let sum = n;
    for ( let i = 2; i < n ; i*=2 ) {
        sum += Math.floor(n/i);
    }
    return sum;
}
```
[Sort rectangles and circles by area II](https://www.codewars.com/kata/5a1ebc2480171f29cf0000e5/train/javascript)
```javascript
function sortByArea(array) {
  const clone = [...array];
  return clone.sort((a, b) => {
        let areaA = 0;
        let areaB = 0;
        if (typeof a === 'object') {
            areaA = a[0] * a[1];
        } else {
            areaA = Math.pow(a, 2) * Math.PI;
        }

        if (typeof b === 'object') {
            areaB = b[0] * b[1];
        } else {
            areaB = Math.pow(b, 2) * Math.PI;
        }

        return areaA - areaB;
    });
}
```
[Basic Calculator](https://www.codewars.com/kata/5296455e4fe0cdf2e000059f/train/javascript)
```javascript
function calculate(num1, operation, num2) {
   switch ( operation) {
        case "+":  return num1 + num2;
            breake;
        case "-": return num1 - num2;
            breake;
        case "/": if ( num2 === 0) return null;
                    else return num1 / num2;
            breake;
        case "*": return num1 * num2;
            breake;
        default: return null;
    }
}
```
[Miles per gallon to kilometers per liter](https://www.codewars.com/kata/557b5e0bddf29d861400005d/train/javascript)
```javascript
function converter (mpg) {
  let kmlt = ( mpg * 1.609344/ 4.54609188 ).toFixed(2);
  return  ( kmlt[kmlt.length-1] === 0 ) ? +(kmlt.slice(0, kmlt[kmlt.length-1])) :  +kmlt;
}
```
[Not above the one!](https://www.codewars.com/kata/5b5097324a317afc740000fe/train/javascript)
```javascript
function binaryCleaner(arr) {
  let arr1 =[];
  let arr2 = [];
  for ( let i = 0; i < arr.length; i++ ) {
    if ( arr[i] === 1 || arr[i] === 0 ) {
      arr1.push(arr[i]);
    } else {
      arr2.push(i);
    }
  }
  let result = [];
  result.push(arr1);
  result.push(arr2);
  return result;
}
```
[Next bigger number with the same digits](https://www.codewars.com/kata/55983863da40caa2c900004e/train/javascript)
```javascript
function nextBigger(n){
    let arr = String(n).split('')
    // find split location
    for (var i = arr.length-1; i > 0 && +arr[i - 1] >= +arr[i]; i--);
    if (i > 0) {
        // splice and sort tail
        let tailSorted = arr.splice(i).sort();
        for (var j = 0; j < tailSorted.length && +arr[i-1] >= +tailSorted[j]; j++);
        // swap
        [arr[i-1], tailSorted[j]] = [tailSorted[j], arr[i-1]];

        return +arr.concat(tailSorted).join('');
    }

    return -1;
}
```
[Even or Odd](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/javascript)
```javascript
function even_or_odd(number) {
  if ( number % 2 === 0 ) {
    return "Even";
  } else {
    return "Odd";
  }
}
```
[Caffeine Script](https://www.codewars.com/kata/5434283682b0fdb0420000e6/train/javascript)
```javascript
function caffeineBuzz(n){
  let answer ='';
  
  if (n % 3 === 0 ) {
    answer = "Java";
  }

  if ( n % 3 === 0 && n % 4 === 0 ) {
    answer = "Coffee";
  }

  if ( answer.length && n % 2 === 0) {
    answer += "Script";
  }  
  
  return answer.length ? answer : "mocha_missing!";

}
```
[Enumerable Magic #25 - Take the First N Elements](https://www.codewars.com/kata/545afd0761aa4c3055001386/train/javascript)
```javascript
public class ZywOo {
  public static int[] take(int[] arr, int n) {
    int size = Math.min(arr.length, n);
    int[] result = new int[size];
    for ( int i = 0; i < size; i++ ) {
      result[i] = arr[i];
    }     
    return result;
  }
}
```
[esreveR](https://www.codewars.com/kata/5413759479ba273f8100003d/train/javascript)
```javascript
reverse = function(array) {
  let result = [];
  for ( let i = array.length-1; i >= 0; i-- ) {
    result.push(array[i]);
  }
  return result;
}
```
[Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence](https://www.codewars.com/kata/57fb09ef2b5314a8a90001ed/train/javascript)
```javascript
function replace(s){
  let str = 'aeuioAEUIO';
  let result = [];
  for ( let i = 0; i < s.length; i++ ) {
    if (str.match(s[i])) {
      result.push('!');
    } else {
      result.push(s[i]);
    }
  }
  return result.join('');  
}
```
[Find min and max](https://www.codewars.com/kata/57a1ae8c7cb1f31e4e000130/train/javascript)
```javascript
function getMinMax(arr){
    let newArr = [];
    arr.sort((a,b) => a - b);
    newArr.push(arr[0], arr[arr.length-1]);
    return newArr;
};
```
[Halving Sum](https://www.codewars.com/kata/5a58d46cfd56cb4e8600009d/train/javascript)
```javascript
function halvingSum(n) {
console.log(n);
    let sum = n;
    for ( let i = 2; i < n ; i*=2 ) {
        sum += Math.floor(n/i);
    }
    return sum;
}
```
[Sort rectangles and circles by area II](https://www.codewars.com/kata/5a1ebc2480171f29cf0000e5/train/javascript)
```javascript
function sortByArea(array) {
  const clone = [...array];
  return clone.sort((a, b) => {
        let areaA = 0;
        let areaB = 0;
        if (typeof a === 'object') {
            areaA = a[0] * a[1];
        } else {
            areaA = Math.pow(a, 2) * Math.PI;
        }

        if (typeof b === 'object') {
            areaB = b[0] * b[1];
        } else {
            areaB = Math.pow(b, 2) * Math.PI;
        }

        return areaA - areaB;
    });
}
```
[Basic Calculator](https://www.codewars.com/kata/5296455e4fe0cdf2e000059f/train/javascript)
```javascript
function calculate(num1, operation, num2) {
   switch ( operation) {
        case "+":  return num1 + num2;
            breake;
        case "-": return num1 - num2;
            breake;
        case "/": if ( num2 === 0) return null;
                    else return num1 / num2;
            breake;
        case "*": return num1 * num2;
            breake;
        default: return null;
    }
}
```
[Miles per gallon to kilometers per liter](https://www.codewars.com/kata/557b5e0bddf29d861400005d/train/javascript)
```javascript
function converter (mpg) {
  let kmlt = ( mpg * 1.609344/ 4.54609188 ).toFixed(2);
  return  ( kmlt[kmlt.length-1] === 0 ) ? +(kmlt.slice(0, kmlt[kmlt.length-1])) :  +kmlt;
}
```
[Not above the one!](https://www.codewars.com/kata/5b5097324a317afc740000fe/train/javascript)
```javascript
function binaryCleaner(arr) {
  let arr1 =[];
  let arr2 = [];
  for ( let i = 0; i < arr.length; i++ ) {
    if ( arr[i] === 1 || arr[i] === 0 ) {
      arr1.push(arr[i]);
    } else {
      arr2.push(i);
    }
  }
  let result = [];
  result.push(arr1);
  result.push(arr2);
  return result;
}
```
[Next bigger number with the same digits](https://www.codewars.com/kata/55983863da40caa2c900004e/train/javascript)
```javascript
function nextBigger(n){
    let arr = String(n).split('')
    // find split location
    for (var i = arr.length-1; i > 0 && +arr[i - 1] >= +arr[i]; i--);
    if (i > 0) {
        // splice and sort tail
        let tailSorted = arr.splice(i).sort();
        for (var j = 0; j < tailSorted.length && +arr[i-1] >= +tailSorted[j]; j++);
        // swap
        [arr[i-1], tailSorted[j]] = [tailSorted[j], arr[i-1]];

        return +arr.concat(tailSorted).join('');
    }

    return -1;
}
```
[Even or Odd](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/sql)
```javascript
function even_or_odd(number) {
  if ( number % 2 === 0 ) {
    return "Even";
  } else {
    return "Odd";
  }
}
```
[Caffeine Script](https://www.codewars.com/kata/5434283682b0fdb0420000e6/train/javascript)
```javascript
function caffeineBuzz(n){
  let answer ='';
  
  if (n % 3 === 0 ) {
    answer = "Java";
  }

  if ( n % 3 === 0 && n % 4 === 0 ) {
    answer = "Coffee";
  }

  if ( answer.length && n % 2 === 0) {
    answer += "Script";
  }  
  
  return answer.length ? answer : "mocha_missing!";

}
```
[esreveR](https://www.codewars.com/kata/5413759479ba273f8100003d/train/javascript)
```javascript
reverse = function(array) {
  let result = [];
  for ( let i = array.length-1; i >= 0; i-- ) {
    result.push(array[i]);
  }
  return result;
}
```
[Selective fear of numbers](https://www.codewars.com/kata/55b1fd84a24ad00b32000075/train/javascript)
```javascript
var AmIAfraid = function(day, num){
  switch(day) {
      case 'Monday': if (num === 12) return true;
                     else return false;
        break;
      case 'Tuesday': if ( num > 95 ) return true;
                      else return false;
        break;
      case 'Wednesday': if ( num === 34 ) return true;
                        else return false;
        break;
      case 'Thursday': if ( num === 0 ) return true;
                        else return false;
        break;
      case 'Friday': if ( num % 2 === 0 ) return true;
                     else return false;
        break;
      case 'Saturday': if ( num === 56 ) return true;
                        else return false;
        break;
      case 'Sunday': if ( num === 666 || num === -666 ) return true;
                     else return false;
        break;
      default: return false;
    }
}
```
[Difference of 2](https://www.codewars.com/kata/5340298112fa30e786000688/train/javascript)
```javascript
function twosDifference(input){
    let pairs = [];
    input.sort((a,b)=>a-b);
    input.forEach((element, index) => {
        for(let j = index + 1; j < input.length; j++) {
            if(Math.abs(element - input[j]) === 2) {
                pairs.push([element, input[j]]);
            }
        }
    });
    return pairs;
}
```
[Simple Fun #176: Reverse Letter](https://www.codewars.com/kata/58b8c94b7df3f116eb00005b/train/javascript)
```javascript
function reverseLetter(str) {
  return str.match(/[a-z]+/g).join('').split('').reverse().join('');
}
```
[Multiply array values and filter non-numeric](https://www.codewars.com/kata/55ed875819ae85ca8b00005c/train/javascript)
```javascript
function multiplyAndFilter(array, multiplier){
    let result = [];
    array.forEach(element => {
        if ( typeof element === "number" ) {
            result.push(element * multiplier);
        }
    });
    return result;
}
```
[Pandemia](https://www.codewars.com/kata/5e2596a9ad937f002e510435/train/javascript)
```javascript
function infected(s) {
    let continentArr = s.split('X');
    let total = 0;
    let infected = 0;
    for (let i = 0; i < continentArr.length; i++) {
        total += continentArr[i].length;
        let ones = continentArr[i].search("1");
        if (ones >= 0) {
            infected += continentArr[i].length
        }
    }
    return !total ? 0 : 100 * infected / total;
}
```
[Get Planet Name By ID](https://www.codewars.com/kata/515e188a311df01cba000003/train/javascript)
```javascript
function getPlanetName(id){
  var name;
  switch(id){
    case 1:
      name = 'Mercury';
      break;
    case 2:
      name = 'Venus';
      break;
    case 3:
      name = 'Earth';
      break;
    case 4:
      name = 'Mars';
      break;
    case 5:
      name = 'Jupiter';
      break;
    case 6:
      name = 'Saturn';
      break;
    case 7:
      name = 'Uranus';
      break;
    case 8:
      name = 'Neptune';
      break;
  }
  
  return name;
}
```
[Area or Perimeter](https://www.codewars.com/kata/5ab6538b379d20ad880000ab/train/javascript)
```javascript
const areaOrPerimeter = function(l , w) {
  return  l === w ? l * w : (2 * l + 2 * w);
  
};
```
[Get Nth Even Number](https://www.codewars.com/kata/5933a1f8552bc2750a0000ed/train/javascript)
```javascript
function nthEven(n){
    return n * 2 - 2;
}
```
[Debug Sum of Digits of a Number](https://www.codewars.com/kata/563d59dd8e47a5ed220000ba/train/javascript)
```javascript
function getSumOfDigits(integer) {
  let sum = 0;
  let digits =  Math.floor(integer).toString();
  for(let ix = 0; ix < digits.length; ix++) {
    sum += +digits[ix];
  }
  return sum;
}
```
[Consecutive Ducks](https://www.codewars.com/kata/5dae2599a8f7d90025d2f15f/train/javascript)
```javascript
function consecutiveDucks(num) {
    let  count = 0; 
    for (let  i = 1; i * (i + 1) < 2 * num; i++) 
    { 
        let a = (1.0 * num-(i * (i + 1)) / 2) / (i + 1) % 1; 
        if (a === 0)  
            return true;      
    } 
    return false; 
}
```
[noobCode 03: CHECK THESE LETTERS... see if letters in "String 1" are present in "String 2"](https://www.codewars.com/kata/57470efebf81fea166001627/train/javascript)
```javascript
function letterCheck(arr) {
    let newArr1 = arr[0].toLowerCase().split('');
    let newArr2 = arr[1].toLowerCase().split('');
    for (let i = 0; i < newArr2.length; i++) {
        if (newArr1.indexOf(newArr2[i]) < 0) {
            return false;
        }
    }
    return true;
}
```
[Row Weights](https://www.codewars.com/kata/5abd66a5ccfd1130b30000a9/train/javascript)
```javascript
function rowWeights(array){
    sum1 = 0;
    sum2 = 0;
    for ( let i = 0; i < array.length; i++ ){
        if ( i % 2 === 0 ) {
            sum1 += array[i];
        } else {
            sum2 += array[i];
        }        
    }
    return [sum1, sum2];
}
```
[Maximum Multiple](https://www.codewars.com/kata/5aba780a6a176b029800041c/train/javascript)
```javascript
function maxMultiple(divisor, bound){
    for ( let i = bound; i >= 0; i-- ){
        if ( Number.isInteger(i/divisor) ) {
            return i;
        }
    }
    return 0;
}
```
[Maximum Triplet Sum (Array Series #7)](https://www.codewars.com/kata/5aa1bcda373c2eb596000112/train/cpp)
```javascript
function maxTriSum(numbers){
    let newArr = new Set(numbers);
    let arr = Array.from(newArr).sort((a,b) => b - a );
    return arr[0] + arr[1] + arr[2];
}
```
[Number Zoo Patrol](https://www.codewars.com/kata/5276c18121e20900c0000235/train/javascript)
```javascript
function findNumber(array) {
    if(array.length) {
      let max =  array.reduce((prev, curr) => Math.max(prev, curr));
      if (max != array.length) {
          let sum = array.reduce((prev, curr) => prev + curr);
          let n = array.length + 1;
          let expectedSum = n*(n + 1) / 2;
          return expectedSum - sum;
      }
    }
    return array.length + 1;
}
```
[Highest Scoring Word](https://www.codewars.com/kata/57eb8fcdf670e99d9b000272/train/javascript)
```javascript
function high(x){
    let result = [];
    let sum = 0;
    let newArr = x.split(" ");
    let alphabet =  '0abcdefghijklmnopqrstuvwxyz'.split('');
    for ( let i = 0; i < newArr.length; i++ )  {
        for ( let j = 0; j < newArr[i].length; j++ ) {
            let indx = alphabet.indexOf(newArr[i][j]);
            sum += indx;
        }
        result.push([newArr[i], sum]);
        sum = 0;
    }  
    result.sort((a,b) => b[1] - a[1]);
    return result[0][0];
}
```
[Which are in?](https://www.codewars.com/kata/550554fd08b86f84fe000a58/train/javascript)
```javascript
function inArray(array1,array2){
    let result = [];
    for ( let i = 0; i < array1.length; i++ ) {
      if ( typeof array1[i] != 'string' ) {
        continue;
      }
        for ( let j = 0; j < array2.length; j++ ) {
            if ( array2[j].search(array1[i]) >= 0 ) {
                result.push(array1[i]);
            }
        }        
    }
    let newArr = result.filter((el, i) => i === result.indexOf(el)).sort();
    return newArr;
}

```
[Delete occurrences of an element if it occurs more than n times](https://www.codewars.com/kata/554ca54ffa7d91b236000023/train/javascript)
```javascript
function deleteNth(arr,n){
    let objCounters = {};
    let result = [];
    arr.forEach(element => {
        let elementCount = element in objCounters ? objCounters[element] : 0;
        if(elementCount < n) {
            objCounters[element] = elementCount + 1;
            result.push(element);
        }
    });
    return result;
}
```
[CamelCase Method](https://www.codewars.com/kata/587731fda577b3d1b0001196/train/ruby)
```javascript
String.prototype.camelCase=function(){
    if ( !this.length ) {
      return "";
    }
    let str = this.split(' ');
    let result = [];
    for ( let i = 0; i < str.length; i++ ) { 
        let word = str[i];
        if(word.length) {
          word = word[0].toUpperCase() + word.substring(1);     
          result.push(word);
        }
    }
    return result.join("");
}
```
[Take a Number And Sum Its Digits Raised To The Consecutive Powers And ....¡Eureka!!](https://www.codewars.com/kata/5626b561280a42ecc50000d1/train/javascript)
```javascript
function sumDigPow(a, b) {
    let result= [];
    let sum = 0;
    for ( let i = a; i <= b; i++ ) {
        let num = (""+ i).split('');
        for ( let j = 0; j < num.length; j++ ) {
            let newD = Math.pow(+num[j],j+1);
            sum += newD;
            if ( sum === i) {
                result.push( sum);
            } 
        }
        sum = 0;
    }
    return result;
}
```
[Count characters in your string](https://www.codewars.com/kata/52efefcbcdf57161d4000091/train/javascript)
```javascript
function count (string) {  
    let result = {};
    let count = 0;
    if ( !string.length ) {
        return {};
    }
    let newStr = string.match(/[a-zA-Z]+/g).join('').split('');
    newStr.forEach(el  => {
        result[el] ? count++ : count = 1;
        result[el] = count; 
    });
    return result;
}
```
[Mexican Wave](https://www.codewars.com/kata/58f5c63f1e26ecda7e000029/train/javascript)
```javascript
function wave(str){
   let result = [];
    let arrStr = str.split('');
    let newArr;
    for ( let i = 0; i < str.length; i++ ) {
        if ( arrStr[i] === ' ') {
            continue;
        }
        let oldLetter = arrStr[i];
        arrStr[i] = arrStr[i].toUpperCase();  
        newArr = arrStr.join(''); 
        arrStr[i] = oldLetter;
        result.push(newArr);
    }       
    return result;
}
```
[Valid Phone Number](https://www.codewars.com/kata/525f47c79f2f25a4db000025/train/javascript)
```javascript
function validPhoneNumber(phoneNumber){
  return phoneNumber.match(/^\(\d\d\d\)\s{1}\d\d\d\-\d\d\d\d$/) ? true : false;
}
```
[Word a10n (abbreviation)](https://www.codewars.com/kata/5375f921003bf62192000746/train/javascript)
```javascript
function abbreviate(string) {
    let result = [];
    let allStr = string.split(/[a-zA-Z]+/);
    let arr = string.trim().split(/[\W]+/);
    let output = [];
    for ( let i = 0; i < arr.length; i++ ) {
        let word = arr[i].split('');
        if ( word.length > 3 ) {
               let str = '' + word[0] + ( word.length - 2) + word[word.length-1];
                result.push(str);
           
        } else {
            result.push(arr[i]);
        }
    }
    for ( let i = 0; i < result.length; i++ ) {
        output.push(allStr[i], result[i]);
    }
    return output.join("");
}
```
[Dashatize it](https://www.codewars.com/kata/58223370aef9fc03fd000071/train/javascript)
```javascript
function dashatize(num) {
    let newNum = String(Math.abs(num)).split('');
    let result = [];

    let last = "";
    newNum.forEach((value, index) => {
        if (result.length && last !== "-" && +value % 2) {
            result.push("-");
        }
        result.push(value);
        last = value;
        if (index < newNum.length - 1 && +value % 2) {
            result.push("-");
            last = "-";
        }
    });
    return result.join("");
}
```
[Pete, the baker](https://www.codewars.com/kata/525c65e51bf619685c000059/train/javascript)
```javascript
function cakes(recipe, available) {
    let res = [];
    for ( let key in recipe ) {
         if (  available.hasOwnProperty(key)) {
              //res.push(key);
              let n = Math.floor(available[key] / recipe[key]);
              res.push(n);
         } else {
              return 0;
         }
    }
    return Math.min(...res);
}
```
[Moving Zeros To The End](https://www.codewars.com/kata/52597aa56021e91c93000cb0/train/javascript)
```javascript
var moveZeros = function (arr) {
    let zeros = [];
    for ( let i = 0; i < arr.length; i++ ) {
        if (arr[i] === 0 ) {
            zeros.push(arr[i]);
            arr.splice(i,1);   
            i--;         
        }
    }
    return arr.concat(zeros);
}
```
[Where my anagrams at?](https://www.codewars.com/kata/523a86aa4230ebb5420001e1/train/javascript)
```javascript
function anagrams(word, words) {
    let result = [];
    let nwWords = [...words];
    let wrd = word.split('').sort().join('');
    for ( let i = 0; i < nwWords.length; i++ ) {
        if ( nwWords[i].split('').sort().join('') === wrd ) {
            result.push(words[i]);
        }
    }
    return result;
}
```
[Find the missing term in an Arithmetic Progression](https://www.codewars.com/kata/52de553ebb55d1fca3000371/train/javascript)
```javascript
var findMissing = function (list) { 
    let step = (list[list.length-1] - list[0])/list.length;
    for ( let i = 0; i < list.length-1; i++ ) {
        if ( list[i+1] !== list[i] + step) {
            return list[i] + step;
        }
    }
}
```
[First non-repeating character](https://www.codewars.com/kata/52bc74d4ac05d0945d00054e/train/javascript)
```javascript
function firstNonRepeatingLetter(s) {
    let str = s;
    let arr = [];
    let newStr = str.toLowerCase().split('');
    for ( let i = 0; i < newStr.length; i++ ) {
        if ( newStr.indexOf(newStr[i]) === newStr.lastIndexOf(newStr[i])) {
            arr.push(s[i]);
        } 
    }
    if (!arr.length) {
        return '';
    }
    return arr[0];
}
```
[Human Readable Time](https://www.codewars.com/kata/52685f7382004e774f0001f7/train/javascript)
```javascript
function humanReadable(seconds) {
    let minutes = Math.floor(seconds / 60);
    let sec = seconds % 60;
    let mins = minutes % 60;
    let hours = Math.floor(minutes / 60);

    return ("00" + hours).slice(-2) + ":" + ("00" + mins).slice(-2) + ":" + ("00" + sec).slice(-2);
}
```
[Weight for weight](https://www.codewars.com/kata/55c6126177c9441a570000cc/train/javascript)
```javascript
function orderWeight(strng) {
    let string = strng;
    let arr = string.trim().split(' ');
    let sum = 0;
    let result = [];
    for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr[i].length; j++) {
            sum += +arr[i][j];
        }
        result.push([sum, arr[i]]);
        sum = 0;
    }
    let resStr = [];
    result.sort((a, b) => {
        let compResult = a[0]- b[0];
        if( compResult === 0) {
            return a[1].localeCompare(b[1])
        } 
        return compResult;
    });

    result.forEach(b => resStr.push(b[1]));
    return resStr.join(' ');
}
```
[Perimeter of squares in a rectangle](https://www.codewars.com/kata/559a28007caad2ac4e000083/train/javascript)
```javascript
function perimeter(n) {
    let nPlus = n + 3;
    let fibSumNPlus = (Math.pow(1+Math.sqrt(5),nPlus) - Math.pow(1-Math.sqrt(5),nPlus))/(Math.pow(2,nPlus)*Math.sqrt(5)) - 1;
    return Math.round( fibSumNPlus * 4 );
}
```
[Math Issues](https://www.codewars.com/kata/5267faf57526ea542e0007fb/train/javascript)
```javascript
Math.round = function(number) {
    let intN = +String(number).match(/^[1-9]+/);
    let decN = +String(number).match(/\.[1-9]/);
    if ( decN > 0.4 ) {
        return intN + 1;
    }
    return +(number - decN).toFixed(); 
  };
  
  Math.ceil = function(number) {
    let intN = +String(number).match(/^[1-9]+/);
    let decN = number - intN;
    if ( decN === 0 ) {
        return intN; 
    }
    return intN + 1;
  };
  
  Math.floor = function(number) {
    let intN = +String(number).match(/^[1-9]+/);
    if ( intN > 0 ) {
        return intN; 
    }
    return 0;
  };
```
[Sum of pairs](https://www.codewars.com/kata/54d81488b981293527000c8f/train/javascript)
```javascript
var sum_pairs=function(ints, s){
  let set = new Set();
  set.add(ints[0]);
  for (let i = 1; i < ints.length; i++ ){
    let num = s - ints[i];
    if (set.has(num)){
      return [num,ints[i]];
    } else {
        set.add(ints[i]);
    }  
}
  return undefined;
}
```
[Extract the domain name from a URL](https://www.codewars.com/kata/514a024011ea4fb54200004b/train/javascript)
```javascript
function domainName(url){
   let group = url.match(/(?:http(?:s)*\:\/\/)*(?:www\.)*([\da-zA-Z\-]+)(?:\..*)/);
    if ( group ) {
        return group[1];
    }
    return 0;
}
```
[Scramblies](https://www.codewars.com/kata/55c04b4cc56a697bb0000048/train/javascript)
```javascript
function scramble(str1, str2) {
    let str1M = {};
    for (const c of str1) {
        if (str1M.hasOwnProperty(c)) {
            str1M[c]++;
        } else {
            str1M[c] = 1;
        }
    }

    for (const c of str2) {
        if (!str1M.hasOwnProperty(c)) {
            return false;
        } else {
            if (str1M[c] < 1) {
                return false;
            } else {
                str1M[c]--;
            }
        }
    }

    return true;
}
```
[Beeramid](https://www.codewars.com/kata/51e04f6b544cf3f6550000c1/train/javascript)
```javascript
// Returns number of complete beeramid levels
var beeramid = function(bonus, price) {

  let level = 0;
  let sum = 0;
  if ( bonus <= 0 ) {
      return 0;
  }
  let cans = Math.floor(bonus/price);
  let res = Math.sqrt(cans);
  for ( let i = 1; i <= res; i++ ) {
      sum += i*i;
    if ( sum <= cans ) {
        level++;
    }
  }
  return level;
}
```
[Is my friend cheating?](https://www.codewars.com/kata/5547cc7dcad755e480000004/train/javascript)
```javascript
function removeNb (n) {
    let result = [];
    let sum =  n * (n+1) / 2;
    for ( let i = 1; i <= n; i++) {
        let num = (sum - i) /(1 + i);
        if (  Number.isInteger(num) && num <= n ) {
            result.push([i, num]);
        }
    }
    return result;
}
```
[Add new item (collections are passed by reference)](https://www.codewars.com/kata/566dc05f855b36a031000048/train/javascript)
```javascript
function addExtra( listOfNumbers ){
    let newArr = listOfNumbers.concat(5);
    return newArr;
}
```
[Convert PascalCase string into snake_case](https://www.codewars.com/kata/529b418d533b76924600085d/train/javascript)
```javascript
function toUnderscore(string) {
    if ( /^\d+$/.test(string) ) {
        return '' + string;
    }
    let result = [];
    let upLetter = '';
    for ( let i = 0; i < string.length; i++ ) {
        if ( /[A-Z]/.test(string[i]) ) {            
            if ( i === 0 ) {
                upLetter = string.substring(i,i+1);
                result.push(upLetter.toLowerCase());                
            } else {
                upLetter = string.substring(i,i+1);
                result.push('_', upLetter.toLowerCase());                
            }  
        } else {
            result.push(string[i]);            
        }
    }
    return result.join(''); 
}
```
[TV channels](https://www.codewars.com/kata/5836dce6966f8d1d43000007/train/javascript)
```javascript
function redarr(arr) {
    let newObj  = {};
    let newSet = new Set(arr);
    let newArr = Array.from(newSet).sort();
    for ( let  i = 0; i < newArr.length; i++ ) {
        newObj[String(i)] = newArr[i];
    }
    return newObj;
}

function redarr(arr) {
 let newObj = {};
 let newArr = [... new Set(arr)].sort();
  for ( let i = 0; i < newArr.length; i++ ) {
    newObj[String(i)] = newArr[i];
  }
  return newObj;
}
```
[Freudian translator](https://www.codewars.com/kata/5713bc89c82eff33c60009f7/train/javascript)
```javascript
function toFreud(string) {
  if ( !string.length ) {
    return "";
  }
  let result = [];
  let arr = string.split(" ");
  for ( let i = 0; i < arr.length; i++ ) {
    result.push("sex");
  }

return result.join(" ");
}
```
[Snail](https://www.codewars.com/kata/521c2db8ddc89b9b7a0000c1/train/javascript)
```javascript
snail = function(array) {
    let result = [];
    let limLeft = 0, limRight = array[0].length, limTop = 0, limBottom = array.length;

    let locX = limLeft;
    let locY = limTop;

    while (limLeft < limRight && limTop < limBottom) {
        // move right
        for (; locX < limRight; locX++) {
            result.push(array[locY][locX]);
        }
        limTop++;
        // move down
        for (locX--, locY++; locY < limBottom; locY++) {
            result.push(array[locY][locX]);
        }
        limRight--;
        // move left
        for (locX--, locY--; locX >= limLeft; locX--) {
            result.push(array[locY][locX]);
        }
        limBottom--;
        // move up
        for (locX++, locY--; locY >= limTop; locY--) {
            result.push(array[locY][locX]);
        }
        limLeft++;
        locY++;
        locX++;
    }

    return result;
}
```
[Find the unique number](https://www.codewars.com/kata/585d7d5adb20cf33cb000235/train/javascript)
```javascript
function findUniq(arr) {
    let obj = {};
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] in obj) {
            obj[arr[i]]++;
        } else {
            obj[arr[i]] = 1;
        }
    }
    
    for (let [key, value] of Object.entries(obj)) {
        if (value === 1) {
            return +key;
        }
    }
}
```
[Tic-Tac-Toe Checker](https://www.codewars.com/kata/525caa5c1bf619d28c000335/train/javascript)
```javascript
function isSolved(board) {
    let win = [
        [[0, 0], [0, 1], [0, 2]],
        [[1, 0], [1, 1], [1, 2]],
        [[2, 0], [2, 1], [2, 2]],
        [[0, 0], [1, 0], [2, 0]],
        [[0, 1], [1, 1], [2, 1]],
        [[0, 2], [1, 2], [2, 2]],
        [[0, 0], [1, 1], [2, 2]],
        [[0, 2], [1, 1], [2, 0]]
    ];
    let emptyCounter = 0;
    for (let i = 0; i < win.length; i++) {
        let check = win[i];
        let set = new Set();
        for (let j = 0; j < check.length; j++) {
            let cell = check[j];
            let rowCheck = cell[0];
            let colCheck = cell[1];
            let value = board[rowCheck][colCheck];
            if (value === 0) {
                emptyCounter++;
            }
            set.add(value);
        }
        if (set.size === 1) {
            if (set.has(1)) {
                return 1;
            } else if (set.has(2)) {
                return 2;
            }
        }
    }

    return emptyCounter ? -1 : 0;
}
```
[Encrypt this!](https://www.codewars.com/kata/5848565e273af816fb000449/train/javascript)
```javascript
var encryptThis = function(text) {
    let textArr = text.split(' ');
    for (let i = 0; i < textArr.length; i++) {
        let wordAr = textArr[i].split('');
        wordAr[0] = String(wordAr[0].charCodeAt(0));
        [wordAr[1], wordAr[wordAr.length - 1]] = [wordAr[wordAr.length - 1], wordAr[1]];
        textArr[i] = wordAr.join('');
    }
    return textArr.join(' ');
}
```
[Josephus Survivor](https://www.codewars.com/kata/555624b601231dc7a400017a/train/java)
```javascript
function josephusSurvivor(n,k){
    let arr = [];
    for (let i = 1; i <= n; i++ ) {
        arr.push(i);
    }
    for ( let j = k - 1; arr.length > 1; j += (k-1) ) {
        j = j % arr.length;
        arr.splice(j,1);
    }
    return arr[0];
}
```
[Get key/value pairs as arrays](https://www.codewars.com/kata/515dfd2f1db09667a0000003/train/javascript)
```javascript
function keysAndValues(data){
     let keys = [];
     let value = [];
     for( key in data) {
         keys.push(key);
         value.push(data[key]);
     }
     return [keys, value];
}
```
[What is my name score? #1](https://www.codewars.com/kata/576a29ab726f4bba4b000bb1/train/javascript)
```javascript
function nameScore(name){
    let sum = 0;
    let newName = name.toUpperCase().split('');
    for ( key in alpha) {
        let smth = key.split('');
        let val = alpha[key];
        smth.forEach(element => {
            alpha[element] = val;
        });
    }
    for ( let i = 0; i < newName.length; i++ ) {      
      if ( newName[i] in alpha ) {
        sum += alpha[newName[i]];
      } else {
          sum += 0;
      }
    }
  return {[name]: sum};
}

function nameScore(name){
    for(key in alpha) {
        key.split('').forEach(letter => alpha[letter] = alpha[key]);
    }
    let sum = 0;
    name.toUpperCase().split('').forEach(letter => letter in alpha ? sum += alpha[letter]:0);
    return {[name]: sum};
}
```
[Leap Years](https://www.codewars.com/kata/526c7363236867513f0005ca/train/javascript)
```javascript
function isLeapYear(year) {
  return ( Number.isInteger(year / 4) && !Number.isInteger(year / 100)|| Number.isInteger(year / 4) && Number.isInteger(year/400) ) ? true : false;
}
```
[Return the Missing Element](https://www.codewars.com/kata/5299413901337c637e000004/train/javascript)
```javascript
function getMissingElement(superImportantArray){
  let sorted = superImportantArray.sort((a,b) => a - b);
  for ( let i = 0; i < sorted.length; i++ ) {
    if ( sorted[i] != i ) {
      return i;
    }
  }
}
```
[Grasshopper - Terminal game combat function](https://www.codewars.com/kata/586c1cf4b98de0399300001d/train/javascript)
```javascript
function combat(health, damage) {
  return health - damage > 0 ?  health - damage : 0;
}
```
[Dollars and Cents](https://www.codewars.com/kata/55902c5eaa8069a5b4000083/train/javascript)
```javascript
function formatMoney(amount){
  if (Number.isInteger(amount)) {
    return '$' + amount + '.00';
  } else if ( /^\d+\.\d{1}$/.test(amount)) {
    return '$' + amount + '0';
  } else {
    return '$' + amount;
  }
}
```
[Find Multiples of a Number](https://www.codewars.com/kata/58ca658cc0d6401f2700045f/train/javascript)
```javascript
function findMultiples(integer, limit) {
    const result = [];
    for ( let i = integer; i <= limit; i++ ) {
        let res = i / integer;
        if (Number.isInteger(res)) {
            result.push(i);
        }
    }
    return result;
}
```
[Hello, Name or World!](https://www.codewars.com/kata/57e3f79c9cb119374600046b/train/javascript)
```javascript
function hello(name) {
 
 return  name ? "Hello, " + name[0].toUpperCase() + name.slice(1).toLowerCase() + "!" : 'Hello, World!';
  
}
```
[Grasshopper - Terminal game move function](https://www.codewars.com/kata/563a631f7cbbc236cf0000c2/train/javascript)
```javascript
function move (position, roll) {
  return roll * 2 + position;
}
```
[Cat years, Dog years](https://www.codewars.com/kata/5a6663e9fd56cb5ab800008b/train/javascript)
```javascript
var humanYearsCatYearsDogYears = function(humanYears) {
  if( humanYears === 1) {
    return [humanYears, 15, 15]
  }
  if ( humanYears === 2) {
    return [humanYears, 24, 24]
  }
  if(humanYears > 2) {
    return [humanYears, 24+ (humanYears-2)*4, 24+ (humanYears-2)*5]
  }
}
```
[Twice as old](https://www.codewars.com/kata/5b853229cfde412a470000d0/train/javascript)
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  if (sonYearsOld*2 > dadYearsOld) {
    return (sonYearsOld*2) - dadYearsOld;
  } else {
    return dadYearsOld - (sonYearsOld*2);
  }
}
```
[Grasshopper - Check for factor](https://www.codewars.com/kata/55cbc3586671f6aa070000fb/train/javascript)
```javascript
function checkForFactor (base, factor) {
  if (base % factor === 0) {
    return true;
  }  else {
    return false;
  } 
}
```
[Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence](https://www.codewars.com/kata/57fb09ef2b5314a8a90001ed/train/javascript)
```javascript
function replace(s){
  let str = 'aeuioAEUIO';
  let result = [];
  for ( let i = 0; i < s.length; i++ ) {
    if (str.match(s[i])) {
      result.push('!');
    } else {
      result.push(s[i]);
    }
  }
  return result.join('');  
}
```
[Welcome to the City](https://www.codewars.com/kata/5302d846be2a9189af0001e4/train/javascript)
```javascript
function sayHello( name, city, state ) {
  let person = name.join(' ');
  return "Hello, " + person + "! " + "Welcome to " + city + ', ' + state + '!';
}
```
[Grasshopper - Debug sayHello](https://www.codewars.com/kata/5625618b1fe21ab49f00001f/train/javascript)
```javascript
function sayHello(name) {
  return 'Hello, ' + name;
}
```
[Exclamation marks series #1: Remove a exclamation mark from the end of string](https://www.codewars.com/kata/57fae964d80daa229d000126/train/javascript)
```javascript
function remove(s){
  if (s[s.length-1] === '!' ) {
    return s.slice(0, s.length-1)
  } else 
     return s 
  
}
```
[Exclamation marks series #6: Remove n exclamation marks in the sentence from left to right](https://www.codewars.com/kata/57faf7275c991027af000679/train/java)
```javascript
function remove(s,n){
    let arr = [];
    let num = 0;
    for (let j = 0; j < s.length; j++) {
        if(s[j] === '!' && num < n) {
          num++;
        } else {
          arr.push(s[j]);
        }
    }
    return arr.join('');
}
```
[Round up to the next multiple of 5](https://www.codewars.com/kata/55d1d6d5955ec6365400006d/train/java)
```javascript
function roundToNext5(n){
  if(n < 0 && Math.abs(n%5) != 0 ) {
        return n + Math.abs(n%5);
    } else {
        if( (Math.abs(n%5)) === 0 ) {
            return n;
        } else {
            return n - Math.abs(n%5) + 5;
        }
    } 
}
```
[Fizz Buzz](https://www.codewars.com/kata/5300901726d12b80e8000498/train/javascript)
```javascript
function fizzbuzz(n) {
  let result = [];
  for (let i = 1; i <= n; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
      result.push('FizzBuzz');
    } else if(i % 5 === 0) {
      result.push('Buzz');
    } else if (i % 3 === 0) {
      result.push( 'Fizz');
    } else {
      result.push(i);
    }
  }
  return result;
}
```
[Running out of space](https://www.codewars.com/kata/56576f82ab83ee8268000059/train/javascript)
```javascript
function spacey(array){
  let newArr = [];
  let element = '';
  for(let i = 0; i < array.length; i++) {
    element += array[i];
    newArr.push(element);
  }
  return newArr;
}
```
[Return a string's even characters.](https://www.codewars.com/kata/566044325f8fddc1c000002c/train/javascript)
```javascript
function evenChars(string) {
  let arr = [];
 if(string.length < 2 || string.length > 100 ) {
   return "invalid string";
 } else {
   for(let i = 0; i < string.length; i++) {
     if(i %2 != 0 ) {
       arr.push(string[i]);
      }
   }   
 }
   return arr;
}
```
[Digitize](https://www.codewars.com/kata/5417423f9e2e6c2f040002ae/train/javascript)
```javascript
function digitize(n) {
    let arr = n.toString().split('');
    return arr.map(el => +el);
}
```
[Find the nth Digit of a Number](https://www.codewars.com/kata/577b9960df78c19bca00007e/train/javascript)
```javascript
var findDigit = function(num, nth){
    let n = Math.abs(num).toString().split('');
    if(nth < 1) {
      return -1;
    }  else if(nth > n.length) {
        return 0;
    } else {
        return +n[n.length-nth];
    }
}
```
[Name Array Capping](https://www.codewars.com/kata/5356ad2cbb858025d800111d/train/javascript)
```javascript
function capMe(names) {
  let result = [];  
  for(el of names) {
    let nm = el.toLowerCase().slice(1);
    result.push(el[0].toUpperCase() + nm);
  }
  return result;
}
```
[Simple beads count](https://www.codewars.com/kata/58712dfa5c538b6fc7000569/train/javascript)
```javascript
function countRedBeads(n) {
  return n < 2 ? 0 : (n - 1 ) * 2;
}
```
[Find the vowels](https://www.codewars.com/kata/5680781b6b7c2be860000036/train/haskell)
```javascript
function vowelIndices(word){
    let result = [];
    for (let i = 0; i < word.length; i++) {
        let s = word.charAt(i);
        if (s.match(/[aeiouy]/gi)) {
            result.push(i+1);
        }
    }
    return result;
}
```
[All Inclusive?](https://www.codewars.com/kata/5700c9acc1555755be00027e/train/javascript)
```javascript
function containAllRots(strng, arr) {
    let count = 0;
    let strngAr = strng.split('');
    for(let i = 0; i < strngAr.length; i++ ) {
        let el = strngAr.shift();
        let newEl = strngAr.join('') + el;
        if( !arr.includes(newEl)) {
          count++;
        } 
        strngAr = newEl.split('');
    }
    return count > 0 ? false : true;
}
```
[The Coupon Code](https://www.codewars.com/kata/539de388a540db7fec000642/train/javascript)
```javascript
function checkCoupon(enteredCode, correctCode, currentDate, expirationDate){
    let curDate = new Date(currentDate).getTime();
    let expDate = new Date(expirationDate).getTime(); 
    return (enteredCode === correctCode && curDate <= expDate) ? true : false;
}
```
[The most common letter](https://www.codewars.com/kata/5a434a9dc5e284724f000011/train/javascript)
```javascript
function replaceCommon(string, letter) {
    let newStr = string.split('');
    let arr = string.split(' ').join('').split('');
    let obj = {};
    let myLet = '';
    arr.forEach(el => el in obj ? obj[el]++ : obj[el] = 1);
    let values = Object.values(obj);
    let maxEl = Math.max(...values);

    for( let j = 0; j < newStr.length; j++) {
        if(myLet === '' && obj[newStr[j]] === maxEl) {
            myLet = newStr[j];
        }

        if(newStr[j] === myLet) {
            newStr[j] = letter;
        }
    }

    return newStr.join('');
}
```
[16+18=214](https://www.codewars.com/kata/5effa412233ac3002a9e471d/train/javascript)
```javascript
function add(num1, num2) {
    let result = [];
    let num1Arr = num1.toString().split('').reverse();
    let num2Arr = num2.toString().split('').reverse();
    let length1 = +num1.toString().length;
    let length2 = +num2.toString().length;
    if(length1 > length2) {
        for( let i = 0;  i < length1; i++ ) {
            if( !num2Arr[i]) {
                result.push(+num1Arr[i]);
            } else {
                result.push(+num1Arr[i] + +(num2Arr[i]));
            }            
        }
    } else {
        for( let i = 0;  i < length2; i++ ) {
            if( !num1Arr[i]) {
                result.push(+num2Arr[i]);
            } else {
                result.push(+num1Arr[i] + +(num2Arr[i]));
            }
            
        }
    }
    return +result.reverse().join('');  
}
```
[Substituting Variables Into Strings: Padded Numbers](https://www.codewars.com/kata/51c89385ee245d7ddf000001/train/javascript)
```javascript
function solution(value){
   let val = value.toString();
   while(val.length < 5 ) {
    val = '0' + val;
  }
  return 'Value is ' + val;
}
```
[Area of a Circle](https://www.codewars.com/kata/537baa6f8f4b300b5900106c/train/javascript)
```javascript
var circleArea = function(radius) {
 return (radius <= 0 || typeof radius != 'number') ? false : +(radius * radius * Math.PI).toFixed(2) ;  
};
```
[Collatz Conjecture Length](https://www.codewars.com/kata/54fb963d3fe32351f2000102/train/javascript)
```javascript
function collatz(n){
   let arr = [];
    arr.push(n);
    for(let i = n; i > 1;) {        
        if( i % 2 === 0 ) {
            let res = i/2;
            arr.push(res);
            i = res;
        } else {
            let res = i*3 + 1
            arr.push(res);
            i = res;
        }    
    }    
    return arr.length;
}
```
[Use reduce() to calculate the sum of the values in an array](https://www.codewars.com/kata/532b4057484b0e58e8000766/train/javascript)
```javascript
function sum(array) {
  return array.reduce((a,b) => a + b);
}
```
[Debug Sum of Digits of a Number](https://www.codewars.com/kata/563d59dd8e47a5ed220000ba/train/javascript)
```javascript
function getSumOfDigits(integer) {
  var sum = 0;
  var digits =  Math.floor(integer).toString();
  for(var ix = 0; ix < digits.length; ix++) {
    sum += +digits[ix];
  }
  return sum;
}
```
[Convert to Binary](https://www.codewars.com/kata/59fca81a5712f9fa4700159a/train/javascript)
```javascript
function toBinary(n){
  return +n.toString(2);
}
```
[Logical calculator](https://www.codewars.com/kata/57096af70dad013aa200007b/train/javascript)
```javascript
function logicalCalc(array, op){
  let result = array[0];
  for(let i = 1; i < array.length; i++) {
    if(op === "XOR") {
      result ^= array[i];
    } else if(op === "OR") {
       result |= array[i];
    } else if(op === "AND") {
      result &= array[i];
    }
  }
  return result ? true : false;
}
```
[Grasshopper - If/else syntax debug](https://www.codewars.com/kata/57089707fe2d01529f00024a/train/javascript)
```javascript
function checkAlive (health) {
  if (health <= 0) {    
    return false
  } else {
    return true
  }
}
```
[Grasshopper - Debug](https://www.codewars.com/kata/55cb854deb36f11f130000e1/train/javascript)
```javascript
function weatherInfo (temp) {
  var c = convertToCelsius(temp)
  if (c > 0)
    return (c + " is above freezing temperature")
  else
    return (c + " is freezing temperature")
}

function convertToCelsius (temperature) {
  var celsius = (temperature - 32) * (5/9)
  return celsius
}
```
[Palindrome Strings](https://www.codewars.com/kata/57a5015d72292ddeb8000b31/train/javascript)
```javascript
function isPalindrome(line) {
  let word = line.toString().split('').reverse().join('');
  return line.toString() === word ? true : false;
}
```
[Simple validation of a username with regex](https://www.codewars.com/kata/56a3f08aa9a6cc9b75000023/train/javascript)
```javascript
function validateUsr(username) {
   return /^[0-9a-z_]{4,16}$/.test(username);
}
```
[Power](https://www.codewars.com/kata/562926c855ca9fdc4800005b/train/javascript)
```javascript
function numberToPower(number, power){
 let res = number;
    if(power === 0) {
        return 1;
    } 
    for(let i = 1; i < power; i++ ) {
        res *= number;    
    }
    return res;
}
```
[Implement Array.prototype.filter()](https://www.codewars.com/kata/56dd9b84fe5754786f0014f7/train/javascript)
```javascript
Array.prototype.filter = function(fnc) {
    let result = [];
    for(let i = 0; i < this.length; i++) {
        if(fnc(this[i])) {
            result.push(this[i]);
        }
    }
    return result;
 };
```
[Add Length](https://www.codewars.com/kata/559d2284b5bb6799e9000047/train/javascript)
```javascript
function addLength(str) {
  let arr = str.split(' ');
  let result = [];
  let count = 0;
  for(let i = 0; i < arr.length; i++) {
      for(let j = 0; j < arr[i].length; j++){
        count++;
      }
      result.push(arr[i] + ' ' + count);
      count = 0;
  }
  return result; 
}
```
[Simple Fun #152: Invite More Women?](https://www.codewars.com/kata/58acfe4ae0201e1708000075/train/javascript)
```javascript
function inviteMoreWomen(L) {
  let men = 0;
  let women = 0;
 for(let i = 0; i < L.length; i++){
   if(L[i] === 1) men++;
   else women++;
 }
  if(women < men){
    return true;
  }
 return false; 
}
```
[Greatest common divisor](https://www.codewars.com/kata/5500d54c2ebe0a8e8a0003fd/train/javascript)
```javascript
function mygcd(x,y){
    let result = [];
    for(let i = 1; i <= y; i++){
       if(Number.isInteger(x/i) && Number.isInteger(y/i)){
        result.push(i);
       } 
    }
    result.reverse();
    return result[0];
}
```
[JavaScript class-like objects](https://www.codewars.com/kata/513e1e47c600c93cef000001/train/javascript)
```javascript
class Animal {    
  constructor(name, type){
    this.name = name;
    this.type = type;
  }  
  toString(){    
    return this.name + ' is a ' + this.type;
  }
}
```
[Form The Largest](https://www.codewars.com/kata/5a4ea304b3bfa89a9900008e/train/javascript)
```javascript
function maxNumber(n){
 return +(n.toString().split('').sort().reverse().join(''));
}
```
[Milk and Cookies for Santa](https://www.codewars.com/kata/52af7bf41f5a1291a6000025/train/javascript)
```javascript
function timeForMilkAndCookies(date){
  return (date.getMonth() == 11 && date.getDate() == 24) ? true : false;
}
```
[Reverse a Number](https://www.codewars.com/kata/555bfd6f9f9f52680f0000c5/train/javascript)
```javascript
function reverseNumber(n) {
    let str = n.toString().split('');
    let negativeNum;
    if(str[0] === '-') {
        negativeNum = str.splice(str[0],1);
        return +(negativeNum + str.reverse().join(''));
    } else {
        return +(str.reverse().join(''));
    }
}
```
[Format With](https://www.codewars.com/kata/5892c13cd9f2a384d6000100)
```javascript
String.prototype.formatWith = function () {
    let output = this;
    for (let i = 0; i < arguments.length; i++) {
        let arg = arguments[i];
        let reg = new RegExp("\\{" + i + "\\}", "g");
        output = output.replace(reg, arg);
    }
    return output;
}
```
[shorter concat [reverse longer]](https://www.codewars.com/kata/54557d61126a00423b000a45/train/javascript)
```javascript
function shorter_reverse_longer(a,b){
    if(a.length === b.length || a.length > b.length) {
        return b + a.split('').reverse().join('') + b;
    } else  {
        return a + b.split('').reverse().join('') + a; 
    }
}
```
[Alphabet war](https://www.codewars.com/kata/59377c53e66267c8f6000027/train/javascript)
```javascript
function alphabetWar(fight)
{
    let left = {"w": 4, "p": 3, "b": 2, "s": 1};
    let right = {"m": 4, "q": 3, "d": 2, "z": 1};
    let countLeft = 0;
    let countRight = 0;
    for(let i = 0; i < fight.length; i++){
        if(fight[i] in left) {
            countLeft += left[fight[i]];
        } else if( fight[i] in right) {
            countRight += right[fight[i]];
        }
    }
    if(countLeft > countRight) {
        return "Left side wins!";
    } else if (countRight > countLeft){
        return "Right side wins!";
    }
    return "Let's fight again!";
}
```
[Small enough? - Beginner](https://www.codewars.com/kata/57cc981a58da9e302a000214/train/javascript)
```javascript
function smallEnough(a, limit){
  count = true;
  for(let i = 0; i < a.length; i++) {
    if(a[i] > limit) {
      count = false;
    }
  }
  return count;
}
```
[All unique](https://www.codewars.com/kata/553e8b195b853c6db4000048/train/javascript)
```javascript
function hasUniqueChars(str){
  let mySet = new Set(str);
  return str.length === mySet.size;
}
```
[Find Count of Most Frequent Item in an Array](https://www.codewars.com/kata/56582133c932d8239900002e/train/javascript)
```javascript
function mostFrequentItemCount(collection) {
  if(collection.length === 0) {
    return 0;
  }
  let obj = {};
  collection.forEach(el => {
    el in obj ? obj[el]++ : obj[el] = 1;    
  });
 return Math.max(...Object.values(obj));
}
```
[Bumps in the Road](https://www.codewars.com/kata/57ed30dde7728215300005fa/train/javascript)
```javascript
function bump(x){
  let count = 0;
  for(let i = 0; i < x.length; i++){
    if(x[i] === 'n') count++;
  }
  return (count > 15) ? "Car Dead" : "Woohoo!";
}
```
[Monotone travel](https://www.codewars.com/kata/54466996990c921f90000d61/train/javascript)
```javascript
var isMonotone = function(arr){
  for(let i = 0; i < arr.length-1; i++){
    if(arr[i] <= arr[i+1]){
      continue;
    } else {
      return false;
    }
  }
  return true; 
}
```
[Indexed capitalization](https://www.codewars.com/kata/59cfc09a86a6fdf6df0000f1/train/javascript)
```javascript
function capitalize(s,arr){
  let result = [];
  for(let i = 0; i < s.length; i++){
    if(arr.includes(i) ){
      result.push(s[i].toUpperCase());
    } else {
      result.push(s[i]);
    }
  }
  return result.join('');
};

```
[Build a square](https://www.codewars.com/kata/59a96d71dbe3b06c0200009c/train/javascript)
```javascript
function generateShape(integer){
    let result ='';
    for(let i = 1; i <= integer; i++){
      for(let j = 1; j <= integer; j++){
        result += '+';        
      }
      if(i === integer){
        continue;
      } else {
        result += '\n';
      }      
    }
    return result;
}
```
[How many stairs will Suzuki climb in 20 years?](https://www.codewars.com/kata/56fc55cd1f5a93d68a001d4e/train/javascript)
```javascript
function stairsIn20(s){
  let res = [].concat(...s);
  return res.reduce((a,b) => a + b) * 20;
}
```
[Grasshopper - Function syntax debugging](https://www.codewars.com/kata/56dae9dc54c0acd29d00109a/train/javascript)
```javascript
function main (verb, noun){
  return verb + noun;
}
```
[Javascript filter - 1](https://www.codewars.com/kata/525d9b1a037b7a9da7000905/train/javascript)
```javascript
function searchNames( logins ){
    let result = [];
    logins.filter(el => {
       if(el[0].charAt(el[0].length-1) === '_'){
           result.push(el);
       }
    })
    return result;
}
```
[Search for letters](https://www.codewars.com/kata/52dbae61ca039685460001ae/train/javascript)
```javascript
function change(string){
    let  arrL = 'abcdefghijklmnopqrstuvwxyz'.split('');
    let result = [];
    for(let i = 0; i < arrL.length; i++){
        if(string.toLowerCase().includes(arrL[i])) {
            result.push(1);
        } else {
            result.push(0);
        }
    }
    return result.join('');
}
```
[Find The Duplicated Number in a Consecutive Unsorted List](https://www.codewars.com/kata/558dd9a1b3f79dc88e000001/train/javascript)
```javascript
function findDup( arr ){
  for(let i = 0; i < arr.length-1; i++){
    if(arr.indexOf(arr[i]) != arr.lastIndexOf(arr[i])){
         return arr[i];
       }
  }
  return false;
  
}
```
[Largest Elements](https://www.codewars.com/kata/53d32bea2f2a21f666000256/train/javascript)
```javascript
function largest(n,xs){
  if(n === 0){
    return [];
  }
  let result = [];
  let arr = xs.sort((a,b)=> b - a);
  for(let i = 0; i < arr.length; i++){    
    if( i< n){
      result.push(arr[i]);
    }     
  }
  return result.reverse();
}
```
[Say hello!](https://www.codewars.com/kata/55955a48a4e9c1a77500005a/train/javascript)
```javascript
function greet(name) {
  if(name === null || !name.length){
    return null;
  } else {
    return 'hello ' + name + '!';
  }
  
}
```
[Minimize Sum Of Array (Array Series #1)](https://www.codewars.com/kata/5a523566b3bfa84c2e00010b/train/javascript)
```javascript
function minSum(arr) {
  let newArr = arr.sort((a,b) => a - b);
    let result = [];
    for(let  i = 0; i < newArr.length/2; i++){
      result.push(newArr[i] * newArr[newArr.length-1-i]);
    }
    return result.reduce((cur, next) => cur + next);
}
```
[Maximum Product](https://www.codewars.com/kata/5a4138acf28b82aa43000117/train/javascript)
```javascript
function adjacentElementsProduct(array) {
  let result = [];
  for(let i = 0; i < array.length-1; i++){
    result.push(array[i] * array[i+1]);
  }
  result.sort((a,b) => b-a);
  return result[0];
}
```
[Array Leaders (Array Series #3)](https://www.codewars.com/kata/5a651865fd56cb55760000e0/train/javascript)
```javascript
var arrayLeaders = numbers => {
  console.log(numbers);
    let result = [];
    let sum;
    for(let i = 0; i < numbers.length; i++) {
        sum = 0;
        for(let j = i+1; j < numbers.length; j++){
            sum += numbers[j];            
        }
        if(numbers[i] > sum) {
            result.push(numbers[i]);            
        }
    }
    return result;
}
```
[Maximum Gap (Array Series #4)](https://www.codewars.com/kata/5a7893ef0025e9eb50000013/train/javascript)
```javascript
function maxGap (numbers){
    let newArr = numbers.sort((a,b) => a - b);
    let result = [];
    for(let i = 0; i < newArr.length-1; i++){
        result.push(Math.abs(newArr[i] - newArr[i+1]));
    }
    return Math.max(...result);
}
```
[Simple remove duplicates](https://www.codewars.com/kata/5ba38ba180824a86850000f7/train/javascript)
```javascript
function solve(arr){
    let newArr = arr.reverse();
    let result = new Set(newArr);
    return [...result].reverse();
}
```
[Validate Credit Card Number](https://www.codewars.com/kata/5418a1dd6d8216e18a0012b2/train/java)
```javascript
function validate(n){
    let nArr = ('' + n).split('');
    let result = [];
    for(let i = 0; i < nArr.length; i++) {
        if(nArr.length % 2 === 0) {
            if(i % 2 === 0) {
                nArr[i] = +nArr[i] * 2;
                if(nArr[i] > 9) nArr[i] = nArr[i] - 9;
                result.push(nArr[i]);
            } else {
                result.push(+nArr[i]);
            }
        } else {
            if(i % 2 != 0) {
                nArr[i] = +nArr[i] * 2;
                if(nArr[i] > 9) nArr[i] = nArr[i] - 9;
                result.push(nArr[i]);
            } else {
                result.push(+nArr[i]);
            }
        }  
    } 
    return (result.reduce((a,b) => a + b) % 10  === 0) ;
}
```
[Alternate case](https://www.codewars.com/kata/57a62154cf1fa5b25200031e/train/javascript)
```javascript
function alternateCase(s) {
  let result = [];
    let arr = s.split('');
    for(let i = 0; i < arr.length; i++){
      for(let j = 0; j < arr[i].length; j++) {
        if(arr[i][j] == arr[i][j].toUpperCase()){
          result.push(arr[i][j].toLowerCase());
        } else {
          result.push(arr[i][j].toUpperCase());
        }
      }
    }
    return result.join('');
}
```
[Data Reverse](https://www.codewars.com/kata/569d488d61b812a0f7000015/train/javascript)
```javascript
function dataReverse(data) {
    let newData = [];
    let oneB = [];
    for(let i = 0; i < data.length; i++){
        if(i && i % 8 == 0) {
            newData.push(oneB);
            oneB = [];
        }
        oneB.push(data[i]);
    }
    if(oneB.length)
        newData.push(oneB);
    return [].concat(...newData.reverse());
}
```
[Counting in the Amazon](https://www.codewars.com/kata/55b95c76e08bd5eef100001e/train/javascript)
```javascript
function countArara(n) {
    let result = [];  
    if(n % 2 === 0) {
      for(let i = 0; i < n/2; i++){
        result.push("adak");
      }    
    } else {
      for(let i = 0; i < (n-1)/2; i++){
        result.push("adak");
      }  
      result.push("anane");
    }      
    return result.join(' ');
}
```
[Smallest unused ID](https://www.codewars.com/kata/55eea63119278d571d00006a/train/javascript)
```javascript
function nextId(ids){
  console.log(ids);
    let arr =  Array.from(new Set(ids.sort((a,b) => a - b)));
    let i;
    for(i = 0; i < arr.length; i++){
      if( i != arr[i] ) {
        return i;
      }         
    }
    return i;
}
```
[Training JS #2: Basic data types--Number](https://www.codewars.com/kata/571edd157e8954bab500032d/train/javascript)
```javascript
var v1=50;v2=100,v3=150,v4=200,v5=2,v6=250
function equal1(){
  var a=v1   
  var b=v1   
  return a+b;
}
//Please refer to the example above to complete the following functions
function equal2(){
  var a=v3  //set number value to a
  var b= v1  //set number value to b
  return a-b;
}
function equal3(){
  var a=v1   //set number value to a
  var b= v5  //set number value to b
  return a*b;
}
function equal4(){
  var a=v4   //set number value to a
  var b=v5   //set number value to b
  return a/b;
}
function equal5(){
  var a=v6  //set number value to a
  var b=v3   //set number value to b
  return a%b;
}
```
[Push a hash/an object into array](https://www.codewars.com/kata/527b3cd0492b6b15250060af/train/javascript)
```javascript
items = []
items.

```
[Training JS #5: Basic data types--Object](https://www.codewars.com/kata/571f1eb77e8954a812000837/train/javascript)
```javascript
function animal(obj){
  return "This " + obj.color + ' ' + obj.name + " has " + obj.legs + " legs.";
}
```
[Meeting](https://www.codewars.com/kata/59df2f8f08c6cec835000012/train/javascript)
```javascript
function meeting(s) {
    let arr = s.split(";");
    let family = [];
    for(let i = 0; i < arr.length; i++){
        let person = arr[i].split(":");
        let first = person[0].toUpperCase();
        let last = person[1].toUpperCase();
        family.push([last, first]);
    }
    let all = family.sort((a,b) => {
        let res = a[0].localeCompare(b[0]);
        if(res)
            return res;
        return a[1].localeCompare(b[1]); 
    });
    let result ='';
    for(let i = 0; i < all.length; i++){
        result += '(' + all[i][0] + ', ' + all[i][1] + ')';
    }
    return result;
}
```
[Pre-FizzBuzz Workout #1](https://www.codewars.com/kata/569e09850a8e371ab200000b/train/javascript)
```javascript
function preFizz(n) {
  let arr = [];
  for(let i = 1; i<= n; i++){
    arr.push(i);
  }
  return arr;
}
```
[Quarter of the year](https://www.codewars.com/kata/5ce9c1000bab0b001134f5af/train/javascript)
```javascript
const quarterOf = (month) => {
  if(month > 0 && month < 4){
    return 1;
  } else if(month > 3 && month < 7){
    return 2;
  } else if(month > 6 && month < 10){
    return 3;
  } else {
    return 4;
  }
  
}
```
[FIXME: Get Full Name](https://www.codewars.com/kata/597c684822bc9388f600010f/train/javascript)
```javascript
class Dinglemouse{
  
  constructor( firstName, lastName ){
    this.firstName = firstName;
    this.lastName = lastName;
  }
  
  getFullName(){
    if(!this.lastName){
      return this.firstName;
    }
    if(!this.firstName){
      return this.lastName;
    }
    return this.firstName + " " + this.lastName;
  }
  
}
```
[NATO Phonetic Alphabet](https://www.codewars.com/kata/54530f75699b53e558002076/train/javascript)
```javascript
var nato = (function() {
  var letters =  {
    "A": "Alpha",  "B": "Bravo",   "C": "Charlie",
    "D": "Delta",  "E": "Echo",    "F": "Foxtrot",
    "G": "Golf",   "H": "Hotel",   "I": "India",
    "J": "Juliett","K": "Kilo",    "L": "Lima",
    "M": "Mike",   "N": "November","O": "Oscar",
    "P": "Papa",   "Q": "Quebec",  "R": "Romeo",
    "S": "Sierra", "T": "Tango",   "U": "Uniform",
    "V": "Victor", "W": "Whiskey", "X": "X-ray",
    "Y": "Yankee", "Z": "Zulu"
  }
  
  return function(word) {
    let arr = word.split('');
    let result = [];
    arr.forEach(el => {
      let upCase = el.toUpperCase();
      if(upCase in letters) result.push(letters[upCase]);
    })
    return result.join(' ');
  }
})()
```
[Even numbers in an array](https://www.codewars.com/kata/5a431c0de1ce0ec33a00000c/train/javascript)
```javascript
function evenNumbers(array, number) {
    let result = [];
    for(let i = array.length-1; result.length < number && i >= 0; i--){
        if(array[i] % 2  === 0)
            result.push(array[i]);
    }
    return result.reverse();
}
```
[Find sum of top-left to bottom-right diagonals](https://www.codewars.com/kata/5497a3c181dd7291ce000700/train/javascript)
```javascript
function diagonalSum(matrix){
    let newArr = [].concat(...matrix);
    let step = Math.sqrt(newArr.length) + 1;
    let sum = 0;
    for(let i = 0; i < newArr.length; i+=step){
        sum += newArr[i];
    }
    return sum;
}
```
[Word values](https://www.codewars.com/kata/598d91785d4ce3ec4f000018/train/javascript)
```javascript
function wordValue(a) {
    let alphabet = "abcdefghijklmnopqrstuvwxyz";
    let result = [];
    for(let i = 0; i < a.length; i++){
        let sum = 0;
        for(let j = 0; j < a[i].length; j++) {
            if(alphabet.includes(a[i][j])){
                sum += alphabet.indexOf(a[i][j])+1;
            }
        }
        result.push(sum * (i+1));
    }
    return result;
}
```
[Who ate the cookie?](https://www.codewars.com/kata/55a996e0e8520afab9000055/train/javascript)
```javascript
function cookie(x){
  if(typeof x === 'number'){
    return "Who ate the last cookie? It was Monica!";
  } else if(typeof x === 'string'){
    return "Who ate the last cookie? It was Zach!";
  } else 
    return "Who ate the last cookie? It was the dog!";
}
```
[Collatz Conjecture (3n+1)](https://www.codewars.com/kata/577a6e90d48e51c55e000217/train/javascript)
```javascript
var hotpo = function(n){
 if(n == 0 ) return 0; 
  let count = 0;
  while(n > 1) {
    if(n % 2 === 0 && n > 1){
       count++;
      n = n/2;
    } 
    if( n % 2 != 0 && n > 1){
      count++;
      n = 3*n+1;
    }  
  }  
  return count;
}
```
[Array element parity](https://www.codewars.com/kata/5a092d9e46d843b9db000064/train/javascript)
```javascript
function solve(arr){
   let set = new Set();
    arr.forEach(el => {
        if(set.has(el*(-1))){
            set.delete(el);
            set.delete(el*(-1));
        }else
           set.add(el);
    });
    return set.values().next().value;
};
```
[Multiplication table for number](https://www.codewars.com/kata/5a2fd38b55519ed98f0000ce/train/javascript)
```javascript
function multiTable(number) {
  let result = [];
  for(let i = 1; i < 11; i++){
    if(i === 10) {
      result.push(i + ' * ' + number + ' = ' + number*i);
    } else {
      result.push(i + ' * ' + number + ' = ' + number*i + '\n');
    }
  }
  return result.join('');
}
```
[Averages of numbers](https://www.codewars.com/kata/57d2807295497e652b000139/train/javascript)
```javascript
function averages(numbers) {
  let result = [];
  if(numbers == undefined || numbers.length < 2){
    return [];
  }
  for(let i = 0; i < numbers.length-1; i++){
    if(numbers.length > 1) {
      let el = (numbers[i] + numbers[i+1]) / 2;
      result.push(el);
     }
  }    
    return result;
  }
```
[Return the day](https://www.codewars.com/kata/59dd3ccdded72fc78b000b25/train/javascript)
```javascript
function whatday(num) { 
  if(num > 7 || num < 1) {
    return "Wrong, please enter a number between 1 and 7";
  }
  switch(num) {
      case 1: return"Sunday";
      case 2: return "Monday";
      case 3: return "Tuesday";
      case 4: return "Wednesday";
      case 5: return "Thursday";
      case 6: return "Friday";
      case 7: return "Saturday";
  }


}
```
[Is there a vowel in there?](https://www.codewars.com/kata/57cff961eca260b71900008f/train/javascript)
```javascript
function isVow(a){
   let letters = String.fromCharCode.apply(null, a).split('');
   let result = [];
   let  vowels = ['a','e','o','u','i'];
   for(let i = 0; i < letters.length; i++){
     if(vowels.includes(letters[i])){
       result.push(letters[i]);
     } else {
         result.push(a[i]);
     }
   }
   return result;
}
```
[Fix your code before the garden dies!](https://www.codewars.com/kata/57158fb92ad763bb180004e7/train/javascript)
```javascript
function rainAmount(mm){
    if (mm < 40) {
         return ("You need to give your plant " + (40 - mm) + "mm of water");
    } else {
         return "Your plant has had more than enough water for today!";
    }
}
```
[Are arrow functions odd?](https://www.codewars.com/kata/559f80b87fa8512e3e0000f5/train/javascript)
````javascript
function odds(values){
  let array = [];
  for(let i = 0; i < values.length; i++){
    if(values[i] % 2 != 0) {
      array.push(values[i]);
    }
  }
  return array;
}
````
[Multiply characters](https://www.codewars.com/kata/52e9aa89b5acdd26d3000127/train/javascript)
```javascript
function spam(number){
  let result = '';
  for(let i = 0; i < number; i++){
    result += "hue";
  }
  return result;
}
```
[ToLeetSpeak](https://www.codewars.com/kata/57c1ab3949324c321600013f/train/javascript)
```javascript
function toLeetSpeak(str) {
    let obj = {
      A : '@',
      B : '8',
      C : '(',
      D : 'D',
      E : '3',
      F : 'F',
      G : '6',
      H : '#',
      I : '!',
      J : 'J',
      K : 'K',
      L : '1',
      M : 'M',
      N : 'N',
      O : '0',
      P : 'P',
      Q : 'Q',
      R : 'R',
      S : '$',
      T : '7',
      U : 'U',
      V : 'V',
      W : 'W',
      X : 'X',
      Y : 'Y',
      Z : '2'
    };
  let result = [];
  for(let i = 0; i < str.length; i++){
    if(str[i] === ' '){
      result.push(' ');
    } else 
        result.push(obj[str[i]]);
  }
  return result.join('');
}
```
[Simple frequency sort](https://www.codewars.com/kata/5a8d2bf60025e9163c0000bc/train/javascript)
```javascript
function solve(arr){
  let obj = {};
  for (let el of arr){
    if (obj[el]) obj[el]++;
    else obj[el] = 1;
  }
  arr = arr.sort((a,b)=>obj[b] === obj[a]? a-b : obj[b]-obj[a]);
  return arr;
}
```
[Take the Derivative](https://www.codewars.com/kata/5963c18ecb97be020b0000a2/train/javascript)
```javascript
function derive(coefficient,exponent) {
  let mult = coefficient * exponent;
  return '' + mult +'x^' + (exponent-1) + '';
}
```
[Find out whether the shape is a cube](https://www.codewars.com/kata/58d248c7012397a81800005c/train/javascript)
```javascript
var cubeChecker = function(volume, side){
  if(volume <= 0 || side <= 0){
    return false;
  } 
  if(volume === side*side*side ){
    return true;
  }
  return false;
};
```
[Training JS #4: Basic data types--Array](https://www.codewars.com/kata/571effabb625ed9b0600107a/train/javascript)
```javascript
function getLength(arr){
  //return length of arr
  return arr.length;
}
function getFirst(arr){
  //return the first element of arr
  return arr[0];
}
function getLast(arr){
  //return the last element of arr
  return arr[arr.length-1];
}
function pushElement(arr){
  var el=1;
  arr.push(el);  
  return arr;
}
function popElement(arr){
  //pop an element from arr
  let el = arr.pop();
  return arr;
}
```
[Remove the time](https://www.codewars.com/kata/56b0ff16d4aa33e5bb00008e/train/javascript)
```javascript
function shortenToDate(longDate) {
    let coma = longDate.indexOf(',');
    return longDate.substring(0,coma);
}
```
[They say that only the name is long enough to attract attention.](https://www.codewars.com/kata/574b1916a3ebd6e4fa0012e7/train/javascript)
```javascript
function isOpposite(s1,s2){
  if(s1.length === 0  || s2.length === 0){
    return false;
  }
  for(let i = 0; i < s1.length; i++){
    if(s1.length != s2.length || s1[i] === s2[i] )
      return false;
  }
  return true;
}
```
["this" is a problem](https://www.codewars.com/kata/547c71fdc5b2b38db1000098/train/javascript)
```javascript
function NameMe(first, last) {
    this.firstName = first;
    this.lastName = last;
    return {firstName: first, lastName: last, name: this.firstName + ' ' + this.lastName};
}
```
[Fun with ES6 Classes #2 - Animals and Inheritance](https://www.codewars.com/kata/56f935002e6c0d55fa000d92/train/javascript)
```javascript
class Shark extends Animal {
  constructor(name, age, status) {
    super(name, age, 0, "shark", status);
      /* Make a call to the parent class's constructor with the correct arguments */
  }
}

class Cat extends Animal {
  // Do the same here as you did for Shark - define your constructor function and any other methods you need
    constructor(name, age, status) {
      super(name, age, 4, "cat", status);
    }
  introduce() {
    return `Hello, my name is ${this.name} and I am ${this.age} years old.` + "  Meow meow!";
  }
}
class Dog extends Animal {
    constructor(name, age, status, master) {
      super(name, age, 4, "dog", status);
      this.master = master;
    }  
  
  greetMaster(){
    return `Hello ${this.master}`;
  }
  
}
```
[Age Range Compatibility Equation](https://www.codewars.com/kata/5803956ddb07c5c74200144e/train/javascript)
```javascript
function datingRange(age){
    let minAge;
    let maxAge;
    if(age <= 14){
        minAge = age - 0.10 * age;
        maxAge = age + 0.10 * age;        
    } else {
        minAge = age / 2 + 7;
        maxAge = (age - 7) * 2;
    }
    return Math.floor(minAge) + "-" + Math.floor(maxAge);
}
```
[Training JS #10: loop statement --for](https://www.codewars.com/kata/5721a78c283129e416000999/train/javascript)
```javascript
function pickIt(arr){
  var odd=[],even=[];
  for(let i = 0; i < arr.length; i++){
    if(arr[i] % 2 === 0){
      even.push(arr[i]);
    } else{
      odd.push(arr[i]);
    }
  }    
  return [odd,even];
}
```
[For UFC Fans (Total Beginners): Conor McGregor vs George Saint Pierre](https://www.codewars.com/kata/582dafb611d576b745000b74/train/javascript)
```javascript
var quote = function(fighter) {
  if(fighter.toLowerCase() === 'george saint pierre'){
    return "I am not impressed by your performance.";
  }
  if(fighter.toLowerCase() === 'conor mcgregor'){
    return "I'd like to take this chance to apologize.. To absolutely NOBODY!";
  }
};
```
[Homogenous arrays](https://www.codewars.com/kata/57ef016a7b45ef647a00002d/train/javascript)
```javascript
function filterHomogenous(arrays) {
    let count = 0;
    let result = [];
    for(let i = 0; i < arrays.length; i++){
      for(let j = 0; j < arrays[i].length-1; j++){          
        if(typeof arrays[i][j] === typeof arrays[i][j+1]){
          count++;
        } else{
          break;
        }
      }
      if((count+1) === arrays[i].length){
          result.push(arrays[i]);
      } 
      count = 0;     
    }
    return result;
}
```
[Sum of array singles](https://www.codewars.com/kata/59f11118a5e129e591000134/train/javascript)
```javascript
function repeats(arr){
  let result = [];
  let obj = {};
  for(let i = 0; i < arr.length; i++){
    if(obj[arr[i]] ){
      obj[arr[i]]++;
    } else {
      obj[arr[i]] = 1;
    }
  }
  for(el in obj){
    if(obj[el] === 1){
      result.push(+el);
    }
  }
  let sum = result.reduce((el, ex) => el + ex);
  return sum;
};
```
[Counting Array Elements](https://www.codewars.com/kata/5569b10074fe4a6715000054/train/javascript)
```javascript
function count(array){
  let obj = {};
  for(let i = 0; i < array.length; i++){
    if(obj[array[i]]){
      obj[array[i]]++;
    } else {
      obj[array[i]] = 1;
    }
  }
  return obj;
}

```
[validate code with simple regex](https://www.codewars.com/kata/56a25ba95df27b7743000016/train/javascript)
```javascript
function validateCode (code) {  
  let patt = new RegExp(/^[123]/);
  return patt.test(code);
}
```
[MakeUpperCase](https://www.codewars.com/kata/57a0556c7cb1f31ab3000ad7/train/javascript)
```javascript
function makeUpperCase(str) {
  return str.toUpperCase();
}
```
[Remove First and Last Character](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0/train/javascript)
```javascript
function removeChar(str){
let newArr = str.split('');
    newArr.splice(0,1);
    newArr.splice(-1);
    return newArr.join('');

};
```
[Find the Remainder](https://www.codewars.com/kata/524f5125ad9c12894e00003f/train/javascript)
```javascript
function remainder(a, b){
  if(b === 0){
    return NaN;
  } 
  return a > b ?  a % b : b % a;
}
```
[Arithmetic List!](https://www.codewars.com/kata/541da001259d9ca85d000688/train/javascript)
```javascript
var seqlist = function(first,c,l){
    let result = [];
    result.push(first);
    for(let i = 1; i < l; i++){
        result.push(first+c);
        first +=c;
    }
    return result;
}
```
[Numbers in strings](https://www.codewars.com/kata/59dd2c38f703c4ae5e000014/train/javascript)
```javascript
function solve(s){
    let result = [];
    let regexStr = s.match(/[a-z]+|[^a-z]+/gi);
    for(let i = 0; i < regexStr.length; i++){
        if(Number.isInteger(+regexStr[i])){
            result.push(regexStr[i]);
        }
    }    
    return +result.sort((a,b) => b - a)[0];
};
```
[Interview Question (easy)](https://www.codewars.com/kata/5b358a1e228d316283001892/train/javascript)
```javascript
function getStrings(city){
    let obj = {};
    let result = '';
    let cityLow = city.toLowerCase().split(' ').join('');
    for(let i = 0; i < cityLow.length; i++){
      if(obj[cityLow[i]]){
        obj[cityLow[i]] +='*';        
      } else {
        obj[cityLow[i]] = '*';
      }
    }
    let keys = Object.keys(obj);
    let last = keys[keys.length-1];
    for(let el in obj){
        if(el === last) {
            result += '' + el +':'+obj[el];
        } else {
            result += '' + el +':'+obj[el] +',';
        }        
    }
    return result;
}
```
[Remove String Spaces](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/javascript)
```javascript
let str = '';
function noSpace(x){
  for (let i = 0; i < x.length; i++ ) {
    str = x.replace(/\s+/g, '');
  }
  return str;
}
```
```javascript
function noSpace(x){
  return x.replace(/\s+/g, '');
}
```
[SevenAte9](https://www.codewars.com/kata/559f44187fa851efad000087/train/javascript)
```javascript
function sevenAte9(str){
    let result = '';
    for(let i = 0; i <= str.length-1; i++){
        if(str[i-1] === '7' && str[i] === '9' && str[i+1] === '7'){
            result += str[i+1];
            i = i+1;
        } else if(i === str.length-1){
            result += str[i];
        } else{
            result += str[i];
        }
    }
    return result;
}
```
[Give me the k first digits. Odd digits.](https://www.codewars.com/kata/59e8afdd0863c7bcb300013a/train/javascript)
```javascript
function findOddDigits(n, k) {
    let newStr = String(n).split('');
    let result ='';
    for(let i = 0; i < newStr.length; i++){        
        if(+newStr[i] % 2 != 0 && result.length < k){
            result += newStr[i];
        }       
    }
    if(k > result.length){
      return 0;
    }
    return +result;
}
```
[L2: Triple X](https://www.codewars.com/kata/568dc69683322417eb00002c/train/javascript)
```javascript
function tripleX(str){
  for(let i = 0; i < str.length; i++){
    if(str[i] === 'x') {
      if(str[i+1] === 'x' && str[i+2] === 'x' ){
        return true;
      } else {
        return false;
      }
    } 
  }
  return false;
}
```
[All Star Code Challenge #22](https://www.codewars.com/kata/5865cff66b5699883f0001aa/train/javascript)
```javascript
function toTime(seconds) {
    let min = Math.floor(seconds / 60);
    let hours = Math.floor(min / 60);   
    let res = Math.floor(min  - hours * 60); 
    if(hours < 1){
        return '' + hours + ' hour(s) and ' + min + ' minute(s)';
    } else {
        return '' + hours + ' hour(s) and ' + res + ' minute(s)';
    }  

}
```
[Letterbox Paint-Squad](https://www.codewars.com/kata/597d75744f4190857a00008d/train/javascript)
```javascript
var paintLetterboxes = function(start, end) {
    let arr = [0,0,0,0,0,0,0,0,0,0];    
    for(let i = start; i <= end; i++){
        let startArr = i.toString().split('');
        for(let j = 0; j < startArr.length; j++){
            let k = +startArr[j];
            arr[k]++;
        }
    }
    return arr;
}
```
[simple calculator](https://www.codewars.com/kata/5810085c533d69f4980001cf/train/javascript)
```javascript
function calculator(a,b,sign){
  if(sign === '+' && typeof a === 'number' && typeof b === 'number' ){
    return a + b;
  } else if(sign === '-' && typeof a === 'number' && typeof b === 'number'){
    return a - b;
  } else if(sign === '/' && typeof a === 'number' && typeof b === 'number'){
    return a / b;
  } else if(sign === '*' && typeof a === 'number' && typeof b === 'number'){
    return a * b;
  } else {
    return "unknown value";
  }
}
```
[Evil or Odious](https://www.codewars.com/kata/56fcfad9c7e1fa2472000034/train/javascript)
```javascript
function evil(n) {
    let str = n.toString(2);
    let evil = 0;
    for(let i = 0; i < str.length; i++){
        if(+str[i] === 1){
            evil++;
        }
    }   
    return (evil % 2 === 0) ? "It's Evil!" : "It's Odious!";
}
```
[NBA full 48 minutes average](https://www.codewars.com/kata/587c2d08bb65b5e8040004fd/train/javascript)
```javascript
function pointsPer48(ppg, mpg) {
  if( ppg === 0 || mpg === 0){
    return 0;
  }
  return +(48 * ppg / mpg).toFixed(1);
}
```
[Even or Odd - Which is Greater](https://www.codewars.com/kata/57f7b8271e3d9283300000b4/train/javascript)
```javascript
function evenOrOdd(str) {
  let odd = 0;
    let even = 0;
    for(let i = 0; i < str.length; i++){
        if(str[i] % 2 === 0){
            even += +str[i];
        } else{
            odd += +str[i];
        }
    }
    if(even > odd){
        return 'Even is greater than Odd';
    } else if( even < odd){
        return 'Odd is greater than Even';
    } else {
        return 'Even and Odd are the same';
    }
}
```
[Convert a string to an array](https://www.codewars.com/kata/57e76bc428d6fbc2d500036d/train/javascript)
```javascript
function stringToArray(string){
  let arr =[];
  let buff ='';
  for ( let i = 0; i < string.length; i++ ) {
    if (string[i] === ' '){
    arr.push(buff);
    buff = '';
    continue;
    } else {
      buff += string[i];
    }
  }

  if (buff.length){
    arr.push(buff);
  }
  return arr;
}
```
```javascript
function stringToArray(string){

  let res = [];
  res = string.split(" ");
  return res;
}
```
[Correct the mistakes of the character recognition software](https://www.codewars.com/kata/577bd026df78c19bca0002c0/train/javascript)
```javascript
function correct(string){
    let strArr = string.split('');
    let newStr = strArr.map(x=>{ switch(x) {
        case '5': return 'S';
        case '0': return 'O';
        case '1': return 'I';
        default: return x;
    }}). join('');
    return newStr;
}

```
[Reversed sequence](https://www.codewars.com/kata/5a00e05cc374cb34d100000d/train/javascript)
```javascript
const reverseSeq = n => {
    let arr = [];
    for ( let i = n; i >= 1; i--) {
        arr.push(i);
    }
    return arr;
  
};
```
[easy logs](https://www.codewars.com/kata/5b68c7029756802aa2000176/train/javascript)
```javascript
function logs(x , a, b){
  return (Math.log(a)/Math.log(x)) +( Math.log(b)/Math.log(x));
}
```
[Training JS #18: Methods of String object--concat() split() and its good friend join()](https://www.codewars.com/kata/57280481e8118511f7000ffa/train/javascript)
```javascript
function splitAndMerge(string, separator) {
    let arr = string.split(' ');
    let arr2 = [];
    for(let i = 0; i < arr.length;i++){
        let x = arr[i].split('').join(separator);
        arr2.push(x);
    }
    return arr2.join(' ');
}
```
[Simple Fun #136: Missing Values](https://www.codewars.com/kata/58a66c208b88b2de660000c3/train/javascript)
```javascript
function missingValues(arr) {
  let obj = {};
  let result = [];
  for(let i = 0; i < arr.length; i++){
    if(obj[arr[i]]){
      obj[arr[i]]++;
    } else {
      obj[arr[i]] = 1;
    }
  }
  for(let i in obj){
    if(obj[i] === 1) {
      result.push(i);
      result.push(i);
    }
    if(obj[i] === 2) {
      result.push(i);
    }
  }
  return result.reduce((el, ac) => el * ac);
  
}
```
[Peak array index](https://www.codewars.com/kata/5a61a846cadebf9738000076/train/javascript)
```javascript
function peak(arr){
    let left = [];
    let sumL = 0;
    let sumR = 0;
    for(let i = 1; i < arr.length; i++){
        left.push(arr[i-1]);
        sumL = left.reduce((el,ac) => el + ac);
        for(let j = i+1; j < arr.length; j++){
           sumR += arr[j];
        }
        if(sumL === sumR){
            return i;
        } else{
            sumR = 0;
        }
    }
    return -1;
}
```
[Take an Arrow to the knee, Functionally](https://www.codewars.com/kata/5b7bd90ef643c4df7400015d/train/javascript)
```javascript
var ArrowFunc = function(arr) {
  return arr.map( el=> String.fromCharCode(el)).join(''); //Complete this function
}
```
[Coloured Triangles](https://www.codewars.com/kata/5a25ac6ac5e284cfbe000111/train/javascript)
```javascript
function triangle(row) {
  let res = [];
    while(row.length > 1) {
        for(let i = 0; i < row.length-1; i++){    
            if(row[i] === "G" && row[i+1] === "G"){ 
                res.push("G");
            }
            if(row[i] === "R" && row[i+1] === "R"){ 
                res.push("R");
            }
            if(row[i] === "B" && row[i+1] === "B"){ 
                res.push("B");
            }
            if(row[i] === "B" && row[i+1] === "G" || row[i] === "G" && row[i+1] === "B") {
            res.push("R");
            }
            if(row[i] === "R" && row[i+1] === "G" || row[i] === "G" && row[i+1] === "R") {
            res.push("B");
            }
            if(row[i] === "B" && row[i+1] === "R" || row[i] === "R" && row[i+1] === "B") {
            res.push("G");
            }            
        }
        row = res.join('');
        res = [];
    }
    return row;
}
```
[Compare Strings by Sum of Chars](https://www.codewars.com/kata/576bb3c4b1abc497ec000065/train/javascript)
```javascript
function compare(s1, s2) {
    if(s1 === '' ||s1 === null || s1.match(/[^a-zA-Z]/g)){
        s1 = '';        
    }
    if(s2 === '' || s2 === null || s2.match(/[^a-zA-Z]/g)){
        s2 = '';        
    }
    s1 = s1.toUpperCase();
    s2 = s2.toUpperCase();
    let sum1 = 0;
    let sum2 = 0;
    if(s1.length >= s2.length){        
        for(let i = 0; i < s1.length; i++){
            if(!s2[i]){
                sum1 += s1.charCodeAt(i);
            } else {
                sum1 += s1.charCodeAt(i);
                sum2 += s2.charCodeAt(i);
            }            
        }        
    } else{
        for(let i = 0; i < s2.length; i++){
            if(!s1[i]){
                sum2 += s2.charCodeAt(i);
            } else {
                sum1 += s1.charCodeAt(i);
                sum2 += s2.charCodeAt(i);
            }
        }        
    }
    if(sum1 === sum2){
        return true;
    } else{
        return false;
    }
}
```
[Nth Smallest Element (Array Series #4)](https://www.codewars.com/kata/5a512f6a80eba857280000fc/train/javascript)
```javascript
function nthSmallest(arr, pos){
  let arrS = arr.sort((a,b) => a - b);
  return arrS[pos-1];
}
```
[Jumping Number (Special Numbers Series #4)](https://www.codewars.com/kata/5a54e796b3bfa8932c0000ed/train/javascript)
```javascript
function jumpingNumber(n){
    let strN = n.toString(); 
    let indx = 0;
    for(let i = 0; i < strN.length-1; i++){
        let x = +strN[i+1];
      if(Math.abs(+strN[i] - +strN[i+1]) === 1){
        continue;
      } else {
        indx++;
      }
    }
    return indx ? "Not!!" : "Jumping!!";
}
```
[Regexp Basics - is it a letter?](https://www.codewars.com/kata/567de72e8b3621b3c300000b/train/javascript)
```javascript
String.prototype.isLetter = function() {
  if(this.length> 1 || !this.length){
    return false;
  } else{
    if((this.charCodeAt(0) >= 65 && this.charCodeAt(0) <= 90) || (this.charCodeAt(0) >= 97 && this.charCodeAt(0) <= 122)){
      return true;
    } else{
      return false;
    }
  }
}
```
[How many arguments](https://www.codewars.com/kata/5c44b0b200ce187106452139/train/javascript)
```javascript
function args_count(){
  //that returns the number of arguments provided
  return arguments.length;
  
}
```
[Average Scores](https://www.codewars.com/kata/57b68bc7b69bfc8209000307/train/javascript)
```javascript
function average(scores) {
   return Math.round(scores.reduce((acc, a)=> acc + a)/scores.length);
}
```
[Partial Word Searching](https://www.codewars.com/kata/54b81566cd7f51408300022d/train/javascript)
```javascript
function wordSearch(query, seq){
  let result = [];  
  for(let i = 0; i < seq.length; i++){
    el = seq[i].toLowerCase();
    if(el.includes(query.toLowerCase())){
      result.push(seq[i]);
    }
  }
  if(!result.length){
    result.push("Empty");
  }
  return  result;
}
```
[Factorial Factory](https://www.codewars.com/kata/528e95af53dcdb40b5000171/train/javascript)
```javascript
function factorial (n) {
  if(n < 0 ){
    return null;
  } else if(n === 0 || n === 1){
    return 1;
  } else {
    return n * factorial(n-1);
  }
}
```
[Easy mathematical callback](https://www.codewars.com/kata/54b7c8d2cd7f51a839000ebf/train/javascript)
```javascript
function processArray(arr, callback) {
    for(let i = 0; i < arr.length; i++){
      arr[i] = callback(arr[i]);
    }
  return arr
}
```
[Automorphic Number (Special Numbers Series #6)](https://www.codewars.com/kata/5a58d889880385c2f40000aa/train/javascript)
```javascript
function automorphic(n){
   let sqr = (n * n).toString().split('').reverse();
    let num = n.toString().split('').reverse();
    for(let i = 0; i < num.length; i++){
        if( num[i] === sqr[i] ){
            continue;
        } else {
            return "Not!!";
        }
    }
    return "Automorphic"; 
}
```
[Disarium Number (Special Numbers Series #3)](https://www.codewars.com/kata/5a53a17bfd56cb9c14000003/train/javascript)
```javascript
function disariumNumber(n){
    let sum = 0;
    let num = n.toString().split('');
    for(let i = 0; i < num.length; i++){
      sum += Math.pow(+num[i], i+1); 
    }
    return sum === n ? "Disarium !!" : "Not !!";
}
```
[By 3, or not by 3? That is the question . . .](https://www.codewars.com/kata/59f7fc109f0e86d705000043/train/javascript)
```javascript
function divisibleByThree(str){
  let sum = 0;
  for(let i = 0; i < str.length; i++){
    sum += +str[i];
  }
  return (sum % 3 === 0) ? true : false;
}
```
[Simple Fun #37: House Numbers Sum](https://www.codewars.com/kata/58880c6e79a0a3e459000004/train/javascript)
```javascript
function houseNumbersSum(inputArray) {
  let sum = 0;
  for(let i = 0; i < inputArray.length; i++){
    if(inputArray[i] === 0){
     return sum;
    } else{
      sum += inputArray[i];
    }
  }
  return sum;  
}
```
[Simple string characters](https://www.codewars.com/kata/5a29a0898f27f2d9c9000058/train/javascript)
```javascript
function solve(s){
  let uppercase = 0;
  let lowercase = 0;
  let numbers = 0;
  let specialChar = 0;
  for(let i = 0; i < s.length; i++){
    if(s[i].match(/[A-Z]/)){
      uppercase++;
    } 
    if(s[i].match(/[a-z]/)){
      lowercase++;        
    } 
    if(s[i].match(/[0-9]/)){
      numbers++;
    }     
    if(s[i].match(/\W|_/)){
       specialChar++;
    }
  }
  return [uppercase, lowercase, numbers, specialChar];
}
```
[Filter unused digits](https://www.codewars.com/kata/55de6173a8fbe814ee000061/train/javascript)
```javascript
function unusedDigits(){
    let str = ''; 
    let res = '';
    for(let i = 0; i < arguments.length; i++){
        if(arguments[i][0] === 0){
            continue;
        } else {
            str += arguments[i];
        }
    }
    for(let i = 0; i <= 9; i++){
        if( str.match(i)){
            continue;
        } else {
            res += i;
        }
    }
    return res.split('').sort().join('');
}
```
[Complete The Pattern #6 - Odd Ladder](https://www.codewars.com/kata/5574940eae1cf7d520000076/train/javascript)
```javascript
function pattern(n){
 var output="";
   if( n <= 0){
     return output;
   }
  for(let i = 1; i <= n; i+=2){
    let el = String(i).repeat(i);        
    if(i === n || i === (n-1)){
      output += el;
    } else {
      output += el + "\n";
    }
  }
 return output;
}
```
[Format a string of names like 'Bart, Lisa & Maggie'.](https://www.codewars.com/kata/53368a47e38700bd8300030d/train/javascript)
```javascript
function list(names){
    let arr = [];
    if(!names.length){
        return '';
    }
    for(let i = 0; i < names.length; i++){
        let name = Object.values(names[i]).join('');
      arr.push(name);
    }
    if(arr.length > 1) {
        let last = arr.splice(arr.length-1);
        return arr.join(', ') + ' & ' + last;
    }
    if(arr.length === 1){
        return arr.join('');
    }    
}
```
[Determine if the poker hand is flush](https://www.codewars.com/kata/5acbc3b3481ebb23a400007d/train/javascript)
```javascript
function isFlush(cards) {
    let count = 0;
    let x = cards[0].charAt(cards[0].length-1);
    for(let i = 0; i < cards.length; i++){      
      if(cards[i].match(x)){
        count++;
      }
    }
    return count === 5 ? true : false;
}
```
[Nth power rules them all!](https://www.codewars.com/kata/58aed2cafab8faca1d000e20/train/javascript)
```javascript
function modifiedSum(a, n) {
  let sum = a.reduce((el, sum)=> sum + el);
  let pw = [];
  for(let i = 0; i < a.length; i++){
    pw.push(Math.pow(a[i], n));
  }
  let result = pw.reduce((el, sum) => sum + el);
  return result - sum;
}
```
[For the sake of argument](https://www.codewars.com/kata/5258b272e6925db09900386a/train/javascript)
```javascript
function numbers(){
  let count = 0;
  for(let i = 0; i < arguments.length; i++){
    if(typeof arguments[i] === 'number'){
      count++;
    } 
  }
  return count === arguments.length 
}
```
[Grasshopper - Create the rooms](https://www.codewars.com/kata/56a29b237e9e997ff2000048/train/javascript)
```javascript
var rooms = {
}

room1 = {
  'name': 'room1[name]',
  'description': 'room1[description]',
  'completed': 'room1[completed]'
},
room2 = {
  'name': 'room1[name]',
  'description': 'room1[description]',
  'completed': 'room1[completed]'
},
room3 = {
  'name': 'room1[name]',
  'description': 'room1[description]',
  'completed': 'room1[completed]'
}

rooms['room1'] = room1;
rooms['room2'] = room2;
rooms['room3'] = room3;
```
[Insert dashes](https://www.codewars.com/kata/55960bbb182094bc4800007b/train/javascript)
```javascript
function insertDash(num) {
    let str = String(num);
    let result = '';
    result += str[0];
    for(let i = 1; i < str.length; i++){
      if(str[i-1] % 2 != 0 && str[i] % 2 != 0){
        result += '-' + str[i];
      } else{
        result += str[i];
      }
    }
    return result;
}
```
[Roman Numerals Decoder](https://www.codewars.com/kata/51b6249c4612257ac0000005/train/javascript)
```javascript
function solution(roman){
  let symbols = {
        "I": 1,
        "V": 5,
        "X": 10,
        "L": 50,
        "C": 100,
        "D": 500,
        "M": 1000
    };
  let table = [];
  for (let i = 0; i < roman.length; i++) {
        table.push(symbols[roman[i]]);
  }
  let year = 0;
  let curElement = 0;
  while (table.length) {
        curElement = table.shift();
        if(table.length) {
            let nexElement = table[0];
            if(curElement >= nexElement) {
                year += curElement;
            } else {
                table.shift();
                year += Math.abs(curElement - nexElement);
            }
        } else {
            year += curElement;
        }
  }
  return year;
}
```
[Roman Numerals Decoder](https://www.codewars.com/kata/51b6249c4612257ac0000005/train/javascript)
```javascript
function solution(roman){
  let symbols = {
        "I": 1,
        "V": 5,
        "X": 10,
        "L": 50,
        "C": 100,
        "D": 500,
        "M": 1000
  };
  let table = [];
  for (let i = 0; i < roman.length; i++) {
        table.push(symbols[roman[i]]);
  }
  let year = 0;
  for (let i = 0; i < table.length; i++) {
        if (table[i + 1] > table[i]) {
            year += table[i + 1] - table[i];
            i++;
        } else {
            year += table[i];
        }
  }
  return year;
}
```
[The maximum and minimum difference -- Simple version](https://www.codewars.com/kata/583c5469977933319f000403/train/javascript)
```javascript
function maxAndMin(arr1,arr2){
    let result = [];
    let min;
    let max;
    if(arr1.length <= arr2.length){
        for(let i = 0; i < arr2.length; i++){
            for(let j = 0; j < arr1.length; j++){
                result.push(Math.abs(arr2[i]-arr1[j]));
            }
        }
        min = result.sort((a,b) => a - b)[0];
        max = result.sort((a,b) => a - b)[result.length-1];
     } else{
       for(let i = 0; i < arr1.length; i++){
            for(let j = 0; j < arr2.length; j++){
                result.push(Math.abs(arr1[i]-arr2[j]));
            }
        }
       min = result.sort((a,b) => a - b)[0];
       max = result.sort((a,b) => a - b)[result.length-1];
     }
    return [max, min];
  
  
}
```
[Shared Bit Counter](https://www.codewars.com/kata/58a5aeb893b79949eb0000f1/train/javascript)
```javascript
function sharedBits(a, b) {
   let binA = "00000000000000000000000000000000" + a.toString(2);
   binA = binA.substring(binA.length-28);
   let binB = "00000000000000000000000000000000" + b.toString(2);
   binB = binB.substring(binB.length-28);
   let count = 0;
   for(let i = 0; i < binA.length; i++){
     if(+binA[i] === 1 && +binB[i] === 1) {
       count++;
     }
   }
   return count >= 2;
}
```
[Contamination #1 -String-](https://www.codewars.com/kata/596fba44963025c878000039/train/javascript)
```javascript
function contamination(text, char){
  if(text === "" || char === ""){
    return "";
  }
  let result = "";
  for(let i = 0; i < text.length; i++){
    result += char;
  }
  return result;
}
```
[Steps in Primes](https://www.codewars.com/kata/5613d06cee1e7da6d5000055/train/javascript)
```javascript
function step(g, m, n) {
  console.log(g,m,n);
    let result = [];
    for (let i = m; i <= n; i++) {
        let prime = true;
        for (let j = 2; j * j <= i; j++) {
            if (i % j === 0) {
                prime = false;
                break;
            }
        }
        if (prime) {
            result.push(i);
        }

    }
    for (let i = 0; i < result.length; i++) {        
        if ( result.includes(result[i] + g)){
            let next = result[i] + g;
            return [result[i], next];
        }        
    }
    return null;
}
```
[Barking mad](https://www.codewars.com/kata/54dba07f03e88a4cec000caf/train/javascript)
```javascript
function Dog (breed) {
  this.breed = breed;
}

var snoopy = new Dog("Beagle");

snoopy.bark = function() {
  return "Woof";
};

var scoobydoo = new Dog("Great Dane");
scoobydoo.bark = function() {
  return "Woof";
};
```
[Special Number (Special Numbers Series #5)](https://www.codewars.com/kata/5a55f04be6be383a50000187/train/javascript)
```javascript
function specialNumber(n){
  let num = n.toString();
  let check = 0;
  for(let i = 0; i < num.length; i++){
    if(/[012345]+/.test(num[i])){
      check++;
    }
  }
  return check === num.length ? "Special!!" : "NOT!!";
}
```
[Candy problem](https://www.codewars.com/kata/55466644b5d240d1d70000ba/train/javascript)
```javascript
function candies(kids){
  let sum = 0;
  if(kids.length > 1){
    let max = Math.max(...kids);
    for(let i = 0; i < kids.length; i++) {
      if(kids[i] < max){
        sum += max - kids[i];
      }
    }
    return sum;
  } else {
    return -1;
  }
}
```
[CubeSummation](https://www.codewars.com/kata/550e9fd127c656709400024d/train/javascript)
```javascript
function cubeSum(n, m){
  if( n === m){
    return 0;
  }
  let result = [];
  if(n > m) {
    for(let i = m + 1; i <= n; i++){
      result.push(Math.pow(i, 3));
    }
  } else{
    for(let i = n + 1; i <= m; i++){
      result.push(Math.pow(i, 3));
    }
  }
  return result.reduce((a,b) => a + b);
}
```
[Simple consecutive pairs](https://www.codewars.com/kata/5a3e1319b6486ac96f000049/train/javascript)
```javascript
function pairs(ar){
  let count = 0;
  for(let i = 0; i < ar.length-1; i+=2){
    if( Math.abs(ar[i]-ar[i+1]) === 1) {
      count++;
    }
  }
  return count;
};
```
[Make the small words big!](https://www.codewars.com/kata/57b4dd38d2a31c75f7000299/train/javascript)
```javascript
function smallWordHelper(sentence){
    let wordsArr = sentence.split(' ');
    let result = [];
    for(let i = 0; i < wordsArr.length; i++){
      if( wordsArr[i].length < 4){
        result.push(wordsArr[i].toUpperCase());
      } else{
        let word ='';
        for(let j = 0; j < wordsArr[i].length; j++){
           if(wordsArr[i][j].match(/[aoiue]/i)){
              continue;
            } else{
                word += wordsArr[i][j];
            }
        }
          result.push(word);
      }
    }
    return result.join(' ');
}
```
[Grasshopper - Basic Function Fixer](https://www.codewars.com/kata/56200d610758762fb0000002/train/javascript)
```javascript
function addFive(num) {
  var total = num + 5
  return total;
}
```
[USD => CNY](https://www.codewars.com/kata/5977618080ef220766000022/train/javascript)
```javascript
function usdcny(usd) {
  return (usd * 6.75).toFixed(2) + ' Chinese Yuan';
}
```
[Last](https://www.codewars.com/kata/541629460b198da04e000bb9/train/javascript)
```javascript
function last(list){
  console.log(list);
  if(arguments.length > 1){
    return arguments[arguments.length-1];
  }  
  if(typeof list === 'object' || typeof list === 'string'){
    return list[list.length-1];
  }
  
  return list;
  
}
```
[Dominant array elements](https://www.codewars.com/kata/5a04133e32b8b998dc000089/train/javascript)
```javascript
function solve(arr){
    let result = [];
    let count = 0;
    for(let i = 0; i < arr.length; i++){
      count = 0;
      for(let j = i+1; j < arr.length; j++){      
        if(arr[i] > arr[j]){
          count++;
          continue;
        } else{
          break;
        }
      }
      if(count === arr.length - 1 -i){
        result.push(arr[i]);
      }
    }
    return result;
};
```
[Valid Spacing](https://www.codewars.com/kata/5f77d62851f6bc0033616bd8/train/javascript)
```javascript
function validSpacing(s) {
    if(!s.length || s.match(/^[a-zA-Z]$/)){
        return true;
    }
    let newStr = s.trim();
    if(s.length === newStr.length){
        for(let i = 0; i < s.length-1; i++){
            if(s[i] === ' ' && s[i+1] === ' '){
                return false;
            } 
        }
        return true;
    } else{
        return false;
    }
}
```
[Max-min arrays](https://www.codewars.com/kata/5a090c4e697598d0b9000004/train/javascript)
```javascript
function solve(arr){
  let sorted = arr.sort((a,b) => b - a);
  let result = [];
  for(let i = 0; i < sorted.length/2; i++){
    let l = i, r = sorted.length - 1- i;
    if( r - l > 0){
      result.push(sorted[l]);
      result.push(sorted[r]);
    } else{
      result.push(sorted[l]);
      break;
    }      
  } 
  return result;
};
```
[Zalgo text reader](https://www.codewars.com/kata/588fe9eaadbbfb44b70001fc/train/javascript)
```javascript
function readZalgo(zalgotext) {
 return  zalgotext.split(' ').map(element => element.split('').filter(value => /[\w\d\.\,\!\?]/.test(value)).join('')).join(' ');
}
```
[Unique string characters](https://www.codewars.com/kata/5a262cfb8f27f217f700000b/train/javascript)
```javascript
function solve(a,b){
  let setUnion = [...a,...b];
  let setDiff = setUnion.filter((num)=> !a.includes(num) || !b.includes(num))
  return setDiff.join('');
};
```
[Replace all items](https://www.codewars.com/kata/57ae18c6e298a7a6d5000c7a/train/javascript)
```javascript
function replaceAll(seq, find, replace) {
  let result = [];
  let str = '';
  if(typeof seq === 'object'){
    for(let i = 0; i < seq.length; i++){
      if(seq[i] === find){
        result.push(replace);
      } else{
        result.push(seq[i]);
      }
    }
    return result;
  } 
  if(typeof seq === 'string'){
    for(let i = 0; i < seq.length; i++){
      if(seq[i] === find){
        str += replace;
      } else{
        str += seq[i];
      }
    }
    return str;
  }
  
  
}
```
[Name on billboard](https://www.codewars.com/kata/570e8ec4127ad143660001fd/train/javascript)
```javascript
function billboard(name, price = 30){
  let result = 0;
  for(let i = 0; i < name.length; i++){
    result += price;
  }
  return result;
}
```
[Mirror, mirror, on the wall...](https://www.codewars.com/kata/5f55ecd770692e001484af7d/train/javascript)
```javascript
function mirror(data) {
    let arr1 = data.slice();
    let arr = arr1.sort((a,b) => a - b);
    let arr2 = arr.slice();
    let rever = arr2.reverse().slice(1);
    return arr.concat(rever);
}
```
[Quarter of the year 1](https://www.codewars.com/kata/5ce9c1000bab0b001134f5af/train/javascript)
```javascript
const quarterOf = (month) => {
  if(month === 1 || month === 2 || month === 3){
      return 1; 
  } else if(month === 4 || month === 5 || month === 6){
    return 2;
  } else if(month === 7 || month === 8 || month === 9){
    return 3;
  } else{
    return 4;
  }  
}
```
[Quarter of the year 2](https://www.codewars.com/kata/5ce9c1000bab0b001134f5af/train/javascript)
```javascript
const quarterOf = (month) => {
  if(month > 0 && month < 4){
    return 1;
  } else if(month > 3 && month < 7){
    return 2;
  } else if(month > 6 && month < 10){
    return 3;
  } else {
    return 4;
  }
  
}
```
[Re-open class](https://www.codewars.com/kata/53d628de83db278fb1000710/train/javascript)
```javascript
//Re-open the class String and add the "myNewMethod" method.
String.prototype.myNewMethod = function() {    
    return this.toUpperCase();
};

```
[Thinking & Testing : Uniq or not Uniq](https://www.codewars.com/kata/56d949281b5fdc7666000004/train/javascript)
```javascript
function testit(a,b){
    let setA = new Set(a);
    let setB = new Set(b);
    return [...setA].concat([...setB]).sort((a,b) => a - b);
}
```
[FIXME: Get Full Name](https://www.codewars.com/kata/597c684822bc9388f600010f/train/javascript)
```javascript
class Dinglemouse{  

  constructor( firstName, lastName ){
    this.firstName = firstName;
    this.lastName = lastName;
  }
  
  getFullName(){    
    if(typeof this.firstName === 'string' && this.firstName.length && 
       typeof this.lastName === 'string' && this.lastName.length){
      return this.firstName + " " + this.lastName;
    } else if(typeof this.firstName === 'string' && this.firstName.length) {
      return this.firstName;
    } else if(typeof this.lastName === 'string' && this.lastName.length) {
      return this.lastName;
    } else{
      return '';
    }
  }
  
}
```
[The reject() function](https://www.codewars.com/kata/52988f3f7edba9839c00037d/train/javascript)
```javascript
function reject(array, predicate) {
  let result =[];
  return array.filter(el => !predicate(el));
}
```
[Simple array product](https://www.codewars.com/kata/5d0365accfd09600130a00c9/train/javascript)
```javascript
var maxEl;
function solve_rec(prod, idx, arr) {
    if (idx < arr.length) {
        let rowData = arr[idx++];
        rowData.forEach(element => {
            solve_rec(prod * element, idx, arr);
        });
    } else {
        maxEl = Math.max(maxEl, prod);
    }
}

function solve(arr) {
    maxEl = Number.NEGATIVE_INFINITY;
    solve_rec(1, 0, arr);
    return maxEl;
}
```
[pick a set of first elements](https://www.codewars.com/kata/572b77262bedd351e9000076/train/javascript)
```javascript
function first(arr, n) {
  let l = 1;  
  if(arguments.length > 1){
    l = Math.min(arr.length, n);
  }  
  return arr.slice(0, l);  
}
```
[Grasshopper - Combine strings](https://www.codewars.com/kata/55f73f66d160f1f1db000059/train/javascript)
```javascript
function combineNames (first, last){
  return first + ' ' + last;
}

```
[Heads and Legs](https://www.codewars.com/kata/574c5075d27783851800169e/train/javascript)
```javascript
function animals(heads, legs){
    let cows = (legs - 2 * heads) / 2;
    let chicks = heads - cows;
    if( Number.isInteger(cows) && Number.isInteger(chicks) && cows >= 0 && chicks >= 0){
      return [chicks, cows];
    }
    if (!Number.isInteger(cows) || !Number.isInteger(chicks) || heads <= 0 || legs <= 0 ){
        return "No solutions";
    }
    return "No solutions";  
}
```
[Calculate String Rotation](https://www.codewars.com/kata/5596f6e9529e9ab6fb000014/train/javascript)
```javascript
function shiftedDiff(first,second){
    let count = 0;
    if(first === second){
        return 0;
    }
    let secondArr = second.split('');
    for(let i = 0; i < secondArr.length; i++){
        let  letter = secondArr.shift();
        secondArr.push(letter);
        let str = secondArr.join('');
        count++;
        if(first === str){
            return count;
        } 
    }
    return -1;
}
```
[Number to digit tiers](https://www.codewars.com/kata/586bca7fa44cfc833e00005c/train/javascript)
```javascript
function createArrayOfTiers(num) {
    let str = num.toString();
    let stringNum = '';
    let result = [];
    for(let i = 0; i < str.length; i++){
        stringNum += str[i];
        result.push(stringNum);
    }
    return result;
}
```
[Backspaces in string](https://www.codewars.com/kata/5727bb0fe81185ae62000ae3/train/javascript)
```javascript
function cleanString(s) {
  console.log(s);
    let arr = s.split('');
    for(let i = 0; i < arr.length; i++){
       if( i === 0 && arr[i] === "#") {
            arr.splice(i,1);
            i = i -2;
        }
        if(arr[i] ===  '#' && i > 0){
           arr.splice(i-1,2);
           i = i - 2;
        } 
       
    }
    return arr.join('');
};
```
[Multiplication table](https://www.codewars.com/kata/534d2f5b5371ecf8d2000a08/train/javascript)
```javascript
multiplicationTable = function(size) {
  let result = [];
  let row = [];
  for(let i = 1; i <= size; i++){
    for(let j = 1; j <= size; j++){
      row.push(i*j); 
      
    }    
    result.push(row);
    row = [];
  }
  return result;
}
```
[BASIC: Making Six Toast.](https://www.codewars.com/kata/5834fec22fb0ba7d080000e8/train/javascript)
```javascript
function sixToast(num) {
  return Math.abs(num - 6);
}
```
[Divisible by previous digit?](https://www.codewars.com/kata/5a2809dbe1ce0e07f800004d/train/javascript)
```javascript
function divisibleByLast(n) {
  let result = [];
  let num = n.toString();
  result.push(false);
  for(let i = 1; i < num.length; i++){
    if(Number.isInteger(num[i] / num[i-1]) ){
      result.push(true);
    } else {
      result.push(false);
    }
  }
  return result;
}
```
[Stones on the Table](https://www.codewars.com/kata/5f70e4cce10f9e0001c8995a/train/javascript)
```javascript
function solve(stones) {
    let lengthBefore = stones.length;
    let lengthAfter = stones.replace(/(.)\1+/gi, "$1").length;
    return lengthBefore - lengthAfter;
}
```
[Find the calculation type](https://www.codewars.com/kata/5aca48db188ab3558e0030fa/train/javascript)
```javascript
function calcType(a, b, res) {
  if ( a + b === res){
    return 'addition';
  }
  if ( a - b === res){
    return 'subtraction';
  }
  if( a * b === res){
    return 'multiplication';
  }
  if( a / b === res){
    return 'division';
  }
}

```
[up AND down](https://www.codewars.com/kata/56cac350145912e68b0006f0/train/javascript)
```javascript
function arrange(strng) {
    let arr = strng.split(' ');
    let word = '';
    for(let i = 0; i < arr.length-1; i++){
      if( (i % 2 === 0 && arr[i].length > arr[i+1].length) || (i % 2 != 0 && arr[i].length < arr[i+1].length) ) {      
        word = arr[i];
        arr[i] = arr[i+1];
        arr[i+1] = word;  
        word = ''; 
      }    
    }
    for(let i = 0; i < arr.length; i++){
        if (i % 2 === 0 ){
            arr[i] = arr[i].toLowerCase();
        } else {
            arr[i] = arr[i].toUpperCase();
        }
    }
    return arr.join(' ');
}
```
[Matrix Transpose](https://www.codewars.com/kata/52fba2a9adcd10b34300094c/train/javascript)
```javascript
function transpose(matrix) {
    let result = [];
    let lengthR = matrix[0].length;
    for (let i = 0; i < lengthR; i++) {
        let tmp = [];
        for (let j = 0; j < matrix.length; j++) {
            tmp.push(matrix[j][i]);
        }
        result.push(tmp);
    }
    return result;
}
```
[heggeleggleggo](https://www.codewars.com/kata/55ea5304685da2fb40000018/train/javascript)
```javascript
function heggeleggleggo(word){
  let result = '';
  let conson = /[BCDFGHJKLMNPQRSTVWXZY]/i;
  for(let i = 0; i < word.length; i++){
    if(conson.test(word[i])){
      result += word[i] + 'egg';
    } else{
      result += word[i];
    }
  }
  return result;
}
```
[Boiled Eggs](https://www.codewars.com/kata/52b5247074ea613a09000164/train/javascript)
```javascript
function cookingTime(eggs) {
  if(eggs === 0){
    return 0;
  }
  if(eggs <= 8) {
    return 5;
  } else{
    return (Math.ceil(eggs / 8) * 5);
  }
}
```
[Simple Jeringonza](https://www.codewars.com/kata/5aba0a08379d20026e0000be/train/javascript)
```javascript
function jeringonza() {
    let result = [];
    let word = '';
    let array = arguments[0].split(' ');
    let upperCase = /[AEIOU]/;
    let lowerCase = /[aeiou]/;
    for(let i = 0; i < array.length; i++){
        for(let j = 0; j < array[i].length; j++){
            if(upperCase.test(array[i][j])){
                word += (array[i][j] + 'P' + array[i][j]).toUpperCase();
            } else if(lowerCase.test(array[i][j])){
                word += (array[i][j] + 'P' + array[i][j]).toLowerCase();
            } else{
                word += array[i][j];
            }            
        }
        result.push(word);
        word = '';
    }
    return result.join(' ');
}
```
[Pair of gloves](https://www.codewars.com/kata/58235a167a8cb37e1a0000db/train/javascript)
```javascript
function numberOfPairs(gloves)
{
  console.log(gloves);
    let obj = {};
    let result = 0;
    gloves.forEach(el => el in obj ? obj[el]++ : obj[el] = 1);
    for(let key in obj){
        if( Math.floor(obj[key] / 2  >= 1)){
            result += Math.floor(obj[key] / 2 );
        }
    }   
    return result;
}
```
[String Breakers](https://www.codewars.com/kata/59d398bb86a6fdf100000031/train/javascript)
```javascript
function stringBreakers(n, string){
   let all = string.split(' ').join('');
    let count = 0;
    let result = '';
    for(let i = 0; i <all.length; i++){
        if(count < n){
            result += all[i];
            count++;
        } else {
            result += '\n';
            count = 0;
            i--;
        }          
    }
    return result;
}
```
[Ce*s*r*d Strings](https://www.codewars.com/kata/5ff6060ed14f4100106d8e6f/train/javascript)
```javascript
function uncensor(infected, discovered) {
  let str = infected.split(' ');
  let arrDisc = discovered.split('');
  let result = [];
  let temp = [];
  for(let i = 0; i< str.length; i++){
      for(let j = 0; j < str[i].length; j++){
          if(str[i][j] === '*'){              
              temp.push(arrDisc.shift());
          } else{
            temp.push(str[i][j]);
          }
      }
      result.push(temp.join(''));
      temp = [];
  }
  return result.join(' ');
}
```
[Equalize the array!](https://www.codewars.com/kata/580a1a4af195dbc9ed00006c/train/javascript)
```javascript
function equalize(array){
    let str = '';
    let result = [];
    for(let i = 0; i < array.length; i++){
      if(array[0] > array[i]){
         str += "-";
         str += Math.abs(array[0] - array[i]);         
         result.push(str);
         str = '';
      } else{
        str += "+";
        str += Math.abs(array[0] - array[i]);
        result.push(str);
        str = '';
      }      
    }
    return result;
}

```
[Number Manipulation I (Easy)](https://www.codewars.com/kata/5890579a34a7d44f3b00009e/train/javascript)
```javascript
function manipulate(num) { 
    let strNum = num + '';
    let result = '';
    let addZ;
    if( strNum.length % 2 === 0){
        addZ = strNum.length/2;
       for(let i = 0; i < strNum.length/2; i++){
           result += strNum[i];
       }
       return +(result + '0'.repeat(addZ));
    } else{
        addZ = (strNum.length-1) / 2 + 1;
        for(let i = 0; i < (strNum.length-1)/2; i++){
            result += strNum[i];
        }
        return +(result + '0'.repeat(addZ));
    }
} 
```
[String matchup](https://www.codewars.com/kata/59ca8e8e1a68b7de740001f4/train/javascript)
```javascript
function solve(a,b){
  let result = [];
  let count = 0;
  for(let i = 0; i < b.length; i++){
    for(let j = 0; j < a.length; j++){
      if(a[j] === b[i]){
        count++;
      }
    }
    result.push(count);
    count = 0;
  }
  return result;
}
```
[Coding 3min : Parallel circuit](https://www.codewars.com/kata/571654c3347e6533fa00186b/train/javascript)
```javascript
function resistance(arr){
  let result = [];
  let sum = 0;
  for(let i = 0; i < arr.length; i++){
    for(let j = 0; j < arr[i].length; j++){
      sum += arr[i][j];
    }
    result.push(sum);
    sum = 0;
  }
  let out = 0;
  for(let i = 0; i < result.length; i++){
    out += 1 / result[i];
  }
  return +(1 / out).toFixed(2);
}

```
