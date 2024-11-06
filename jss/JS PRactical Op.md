Exp no:1 

/\*HTML CODE\*/ 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<title>Area Computation</title>

<script type="text/javascript" src="exp1.js"></script>

</head> 

<body> 

<h2>Area of rectangle</h2>

<label for="length">Enter Length</label>

<input type="number" name="length" id="rectLen">

<label for="breadth">Enter Breadth</label>

<input type="number" name="breadth" id="rectBre">

<button type="submit" onclick="areaOfRectangle()">calculateArea</button> <h4 id="rectarea" style="color: red">Area of rectangle is: ?</h4>

<h2>Area of triangle</h2>

<label for="base">Enter Base</label>

<input type="number" name="base" id="triBase">

<label for="height">Enter Height</label>

<input type="number" name="height" id="triHei">

<button type="submit" onclick="areaOfTriangle()">computeArea</button> <h4 id="triarea" style="color: red">Area of triangle is: ?</h4>

<h2>Area of Circle</h2>

<label>Enter radius</label>

<input type="number" id="radius">

<button type="submit" onclick="areaOfCircle()">computeArea</button> <h4 id="circlearea" style="color: red">Area of circle is: ?</h4>

</body> 

</html> 

//JS CODE 

function areaOfRectangle() { 

var a = parseFloat(document.getElementById('rectLen').value); 

var b = parseFloat(document.getElementById('rectBre').value); 

var area = a \* b; 

document.getElementById("rectarea").innerHTML = "Area of rectangle is: " + area; } 

function areaOfTriangle() { 

var a = parseFloat(document.getElementById('triBase').value); 

var b = parseFloat(document.getElementById('triHei').value); 

var area = 0.5 \* a \* b;

document.getElementById("triarea").innerHTML = "Area of triangle is: " + area;

} 

function areaOfCircle() { 

var r = parseFloat(document.getElementById('radius').value); 

var area = Math.PI \* r \* r;

document.getElementById("circlearea").innerHTML = "Area of circle is: " + area;

} Output 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.001.jpeg)

EXP NO 2: 

//CODE 

<!DOCTYPE html> 

<html> 

<head> 

<title>First multiplication table</title>

<script type="text/javascript"> 

function mul(abc) { 

for (var i = 1; i <= 10; i++) { 

var pqr = i \* abc; 

console.log(i + " X " + abc + " = " + pqr); document.write("<br>");

document.write(i + " X " + abc + " = " + pqr);

} 

} 

</script> 

</head> 

<body> 

<label for="text">Enter the no:</label><br>

<input type="number" id="no1"><br>

<button onclick="mul(no1.value)">multiplication table</button> </body> 

</html> 

Output: 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.002.jpeg)


![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.003.jpeg)

EXP NO: 3 

//CODE : 

<!DOCTYPE html> 

<lang="en"> 

<head> 

<title>String Operations</title>

</head> 

<h1>String Operations</h1>

<br> 

<label for="str">Enter the string </label>

<input type="text" name="str" id="str"/>

<h2>String Reversal using FOR Loop</h2>

<button type="submit" onclick="revStrUsingFor()">Reverse String</button> <h4 style="color:red" id="revfor">Reverse string is? </h4>

<br> 

<h2>String Reversal using recursive function</h2>

<button type="submit" onclick="var x = revStrRecursive(); document.getElementById('revrec').innerHTML = 'Reverse string is: ' + x;">Reverse String</button> 

<h4 style="color:red" id="revrec">Reverse string is? </h4>

<br> 

<h2>String Reversal using in-built functions</h2>

<button type="submit" onclick="revStrInbuiltFunc()">Reverse String</button> <h4 style="color:red" id="revinbuilt">Reverse string is? </h4>

<br> 

<h2>String Palindrome</h2>

<button type="submit" onclick="strPalindrome()">Check String</button> <h4 style="color:red" id="strPalin">Given string is? </h4>

<br> 

<h2>Replace characters of string</h2>


<label for="match">Enter match/characters to be replaced from string:</label> <input type="text" name="match" id="match"/>

<br> 

<br> 

<label for="pattern">Enter pattern/characters to be added into string:</label>

<input type="text" name="pattern" id="pattern"/>

<input type="text" name="pattern" id="pattern"/>

<br> 

<br> 

<button type="submit" onclick="strReplace()">Replace</button>

<h4 style="color:red" id="strrep">String replacement using replace() method: ? </h4>

<h4 style="color:red" id="strrepall">String replacement using replaceall() method: ? </h4> 

<Script type="text/javascript"> 

function revStrUsingFor() { 

var str = document.getElementById('str').value; 

var revStr = ""; 

for (var i = str.length - 1; i >= 0; i--) { 

revStr += str[i]; 

} 

document.getElementById('revfor').innerHTML = "Reverse string is: " + revStr; } 

function strRevRecursive(str) { 

if (str === '') { 

return null; 

} else if (str.length === 1) { 

return str; 

} else { 

return strRevRecursive(str.substr(1)) + str.charAt(0);

} 

} 

function revStrRecursive() { 

var str = document.getElementById('str').value; 

var revStr = strRevRecursive(str);

document.getElementById("revrec").innerHTML = "Reverse string is: " + revStr;

} 

function revStrInbuiltFunc() { 

var str = document.getElementById('str').value; 

var splitString = str.split("");

var reverseArray = splitString.reverse(); 

var joinArray = reverseArray.join("");

//str.split("").reverse().join(""); //all in single line

document.getElementById("revinbuilt").innerHTML = "Reverse string is: " + joinArray; } 

function strReplace() { 

var str = document.getElementById('str').value;

var match = document.getElementById('match').value; 

var pattern = document.getElementById('pattern').value; 

var newStr1 = str.replace(match, pattern);

var newStr2 = str.replaceAll(match, pattern);

document.getElementById("strrep").innerHTML = "String replacement using replace() method: " + newStr1; 

document.getElementById("strrepall").innerHTML = "String replacement using replaceAll() method: " + newStr2;

} 

function strPalindrome() { 

var str = document.getElementById('str').value; 

var revStr = str.split("").reverse().join("");

if (str === revStr) { 

document.getElementById("strPalin").innerHTML = "Given string is Palindrome";

} else { 

document.getElementById("strPalin").innerHTML = "Sorry! Given string is not palindrome"; 

EXP NO:4 

} </Script> </body> </html> 

//OUTPUT: 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.004.jpeg)

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.005.jpeg)

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>String Comparison</title>

</head> 

<body> 

<h1>String Comparison Using Various Methods</h1>

<p>Open the browser console to see the results of the string comparison.</p> <script> 

// Method 1: Using toUpperCase()

console.log("Method 1: Using toUpperCase()"); 

const string1a = 'JavaScript Program';

const string2a = 'javascript program';

const result1 = string1a.toUpperCase() === string2a.toUpperCase(); if(result1) { 

console.log('The strings are similar.');

} else { 

console.log('The strings are not similar.');

} 

// Method 2: JS String Comparison Using RegEx 

console.log("\nMethod 2: Using RegEx");

const string1b = 'JavaScript Program'; 

const string2b = 'javascript program';

const pattern = new RegExp(string1b, "gi"); 

const result2 = pattern.test(string2b);

if(result2) { 

console.log('The strings are similar.');

} else { 


console.log('The strings are not similar.');

} 

// Method 3: Using localeCompare() [Recommended Method] console.log("\nMethod 3: Using localeCompare()");

const string1c = 'JavaScript Program'; 

const string2c = 'javascript program';

const result3 = string1c.localeCompare(string2c, undefined, {sensitivity: 'base'}); if(result3 == 0) { 

console.log('The strings are similar.');

} else { 

console.log('The strings are not similar.');

} 

</script> 

</body> 

</html> 

OUTPUT : 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.006.jpeg)

EXP NO: 5 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Countdown Timer</title>

</head> 

<body> 

<h1>Countdown Timer</h1>

<p id="demo"></p>

<script> 

// time to countdown from (in milliseconds) 

let countDownDate = new Date().getTime() + 24 \* 60 \* 60 \* 1000;

// countdown timer 

let x = setInterval(function() {

// get today's date and time in milliseconds 

let now = new Date().getTime();

// find the interval between now and the countdown time 

let timeLeft = countDownDate - now;

// time calculations for days, hours, minutes and seconds 

const days = Math.floor( timeLeft/(1000\*60\*60\*24) ); 

const hours = Math.floor( (timeLeft/(1000\*60\*60)) % 24 ); 

const minutes = Math.floor( (timeLeft/1000/60) % 60 ); 

const seconds = Math.floor( (timeLeft/1000) % 60 );

// display the result in the element with id="demo" document.getElementById("demo").innerHTML = days + "d " + hours + "h " + minutes + "m " + seconds + "s "; // clearing countdown when complete 

if (timeLeft < 0) { 

clearInterval(x); 


document.getElementById("demo").innerHTML = "Countdown Finished"; } 

}, 1000); // update every second (1000 milliseconds)

</script> 

</body> 

</html> 

//OUTPUT: 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.007.jpeg)

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.008.jpeg)

Exp No:8 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Set Operations</title>

</head> 

<body> 

<h1>Set Operations</h1>

<!-- Section for Union --> 

<h3>Union of two sets</h3>

<p id="unionResult"></p>

<!-- Section for Intersection -->

<h3>Intersection of two sets</h3>

<p id="intersectionResult"></p>

<!-- Section for Difference -->

<h3> Difference of two sets</h3>

<p id="differenceResult"></p>

<script> 

// Exp 8a: Perform union operation 

function union(a, b) { 

let unionSet = new Set(a); 

for (let i of b) { 

unionSet.add(i); 

} 

return unionSet; 

} 

// Exp 8b: Perform intersection operation 

function intersection(setA, setB) {

let intersectionSet = new Set();

for (let i of setB) { 

if (setA.has(i)) { 

intersectionSet.add(i); 

} 

} 

return intersectionSet; 

} 

// Exp 8c: Perform difference operation 

function difference(setA, setB) {

let differenceSet = new Set(setA); 

for (let i of setB) { 

differenceSet.delete(i); 

} 

return differenceSet; 

} 

// Two sets of fruits 

const setA = new Set(['apple', 'mango', 'orange']); 

const setB = new Set(['grapes', 'apple', 'banana']);

// Display union result 

const unionResult = union(setA, setB);

document.getElementById('unionResult').innerText  =  `Union: 

${Array.from(unionResult).join(', ')}`;

// Display intersection result 

const intersectionResult = intersection(setA, setB);

document.getElementById('intersectionResult').innerText  =  `Intersection: ${Array.from(intersectionResult).join(', ')}`;

// Display difference result 

const differenceResult = difference(setA, setB);

document.getElementById('differenceResult').innerText  =  `Difference: ${Array.from(differenceResult).join(', ')}`;

</script></body> </html> 

Output: 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.009.jpeg)

Exp no: 7b 

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Add Element to Array using Splice Method</title>

<style> 

body { 

text-align: center; 

font-family: Arial, sans-serif; 

} 

h1 { 

color: green; 

} 

</style> 

</head> 

<body> 

<h1>GeeksforGeeks</h1> 

<p>Click the button to add new elements to the array.</p>

<!-- Button to trigger spliceFunction -->

<button onclick="spliceFunction()">Add Elements</button>

<!-- Display array here -->

<p id="geeks"></p>

<script> 

// Initial array 

var list = ["HTML", "CSS", "JavaScript"] 

// Display the initial array document.getElementById("geeks").innerHTML = list;


// Function to add new elements using splice 

function spliceFunction() { 

list.splice(2, 0, "Angular", "SǪL"); // Add elements at index 2

document.getElementById("geeks").innerHTML = list; // Update display } 

</script> 

</body> 

</html> 

Output: 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.010.jpeg)

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Append Object to Array and Check if Object is an Array</title>

<style> 

body { 

font-family: Arial, sans-serif; 

text-align: center; 

} 

h1 { 

color: blue; 

} 

p { 

font-size: 16px; 

} 

</style> 

</head> 

<body> 

<h1>Append Object to Array and Check if Object is an Array</h1>

<!-- Sections to display results -->

<p><strong>Check  if  object  is  an  array:</strong>  <span id="checkObject"></span></p> 

<p><strong>Array  after  inserting  object:</strong>  <span id="arrayResult"></span></p> 

<script> 

// Function to append an object to an array function insertObject(arr, obj) { arr.push(obj); // Append object


document.getElementById('arrayResult').innerText = JSON.stringify(arr); // Display updated array 

console.log(arr); 

} 

// Function to check if a variable is an array 

function checkObject(obj) { 

const result = Array.isArray(obj); // Check if obj is an array if (result) { 

document.getElementById('checkObject').innerText = `[${JSON.stringify(obj)}] is an array.`; // Display result 

console.log(`[${obj}] is an array.`); } else { 

document.getElementById('checkObject').innerText = `${JSON.stringify(obj)} is not an array.`; // Display result 

console.log(`${obj} is not an array.`); } 

} 

// Original  array 

let array = [1, 2, 3];

// Object to add 

let object = {x: 12, y: 8};

// Check if object is an array checkObject(object); 

// Append object to array

insertObject(array, object);

</script> 

</body> 

</html> 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.011.png)

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Remove Array Element</title>

</head> 

<body> 

<h1>Remove Array Element Example</h1>

<p><strong>Original Array:</strong> [1, 2, 3, 4, 5]</p>

<p><strong>After removing 2:</strong> <span id="result1"></span></p> <p><strong>Original Array:</strong> [2, 5, 9, 6]</p>

<p><strong>After removing 5:</strong> <span id="result2"></span></p> <script> 

// Function to remove an element by modifying the original array function remove\_array\_element(array, n) {

var index = array.indexOf(n); 

if (index > -1) { 

array.splice(index, 1); // Remove element at index

} 

return array; 

} 

// Function to remove an element and return a new array 

function removeItemFromArray(array, n) {

const newArray = []; 

for (let i = 0; i < array.length; i++) { 

if (array[i] !== n) { 

newArray.push(array[i]); // Push element if it's not equal to n

} 


return newArray; 

} 

// Testing the functions and displaying the result

const result1 = removeItemFromArray([1, 2, 3, 4, 5], 2); // Using second method const result2 = remove\_array\_element([2, 5, 9, 6], 5); // Using first method

// Display the results in the HTML document.getElementById("result1").innerText = result1; document.getElementById("result2").innerText = result2;

</script> 

</body> 

</html> 

Output : 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.012.jpeg)

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Array Manipulation</title>

</head> 

<body> 

<h1>Array Manipulation Experiments</h1>

<h2>Checking if an array contains a specified value</h2>

<p id="arrayCheckResult"></p>

<h2>Emptying an array using three methods</h2>

<p>Original array: [1, 2, 3]</p>

<p><strong>Method 1 (Substitution):</strong> <span id="method1Result"></span></p> 

<p><strong>Method 2 (Splice):</strong> <span id="method2Result"></span></p>

<p><strong>Method 3 (Set length to 0):</strong> <span id="method3Result"></span></p> 

<script> 

// Exp 6b: Program to check if an array contains a specified value 

const array1 = ['you', 'will', 'learn', 'javascript'];

const hasValue = array1.includes('javascript');

const  arrayCheckResult  = document.getElementById('arrayCheckResult'); if (hasValue) { 

arrayCheckResult.textContent = 'Array contains the value: "javascript".';

} else { 

arrayCheckResult.textContent = 'Array does not contain the value.';

} 

// Exp 6c: Program to empty an array using three methods


// Method 1: Substituting new array 

function emptyArrayBySubstitution(arr) {

arr = []; 

return arr; 

} 

// Method 2: Using splice to remove all elements function emptyArrayBySplice(arr) { 

arr.splice(0, arr.length); 

return arr; 

} 

// Method 3: Setting array length to 0 

function emptyArrayByLength(arr) { 

arr.length = 0; 

return arr; 

} 

const originalArray = [1, 2, 3];

// Method 1 

const method1Array = [...originalArray]; // Clone the array to avoid modifying the original 

const result1 = emptyArrayBySubstitution(method1Array); document.getElementById('method1Result').textContent = `[${result1}]`; // Method 2 

const method2Array = [...originalArray];

const result2 = emptyArrayBySplice(method2Array); document.getElementById('method2Result').textContent = `[${result2}]`; // Method 3 

const method3Array = [...originalArray];

const result3 = emptyArrayByLength(method3Array);

document.getElementById('method3Result').textContent = `[${result3}]`; </script> 

</body></html> 

EXP No:9 

Code : 

//Experiment 9a: JavaScript program to change background color of Webpage On mouse over event

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8"> 

<meta http-equiv="X-UA-Compatible" content="IE=edge"> 

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Experiment-9</title> 

<script src="Exp9.js"> </script> 

</head> <body> 

<h1 id="head1" onmouseover="changeColor1()" onmouseout="changeColor2()"> Experiment-9</h1> 

<h2> JavaScript program to change background color of Webpage On mouse over event</h2> 

<p>We are using mousever Event to Change the Background Color</p> 

</body> </html> 

Js Code: 

function changeColor1() { 

document.body.style.backgroundColor = "red";

} 

function changeColor2() { 

document.body.style.backgroundColor = "yellow";

} 
Output : 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.013.jpeg)


Exp no:9b 

//Experimen-9b: Program to change Background color using onfocus event <!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Experiment-9b</title> 

</head> 

<body> 

<h1>Experimen-9b</h1> 

<p> In this Program we are going to change the Background color of document when onfocus event is occured</p> 

<h2>Student Information Form</h2>

<form id="myForm"> 

<label> Student Name: <input type="text" id="myInput">  </label> </form> 

</body> 

<script src="Exp9b.js"></script>

</html> 

JS code: 

var x = document.getElementById("myForm"); x.addEventListener("focus", myFocusFunction, true); x.addEventListener("blur", myBlurFunction, true); 

function myFocusFunction() { 

document.getElementById("myInput").style.backgroundColor = "yellow";

} 

function myBlurFunction() { 

document.getElementById("myInput").style.backgroundColor = ""; } 

Output : 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.014.png)

Exp no 10 

Html code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Document</title> 

<script src="/Exp10a.js"></script>

</head> 

<body> 

<h1>Experiment-10</h1> 

<h2>Form Validation Example</h2>

<br> 

<h1>Sign Up Form</h1>

<form name="myForm" action="/thankyou.html" onsubmit="return validate()" >

<label for="fname"> First name</label>

<input type="text" id="fname" name="fname" placeholder="Enter First Name" 

required> 

<label for="lname">Last Name</label>

<input type="text" id="lname" name="lname" placeholder="Enter Last Name" > <br> 

<br> 

<label for="usremail">Email</label>

<input type="email" id="usremail" name="usremail" placeholder="Enter Email here"

\> 

<label for="usrpassword">Password</label>

<input type="password" id="usrpassword" name="usrpassword" placeholder="Enter Password" > 

<br> <br> 


<p>Gender ?</p>

<label for="male"> Male</label>

<input type="radio" id="male" name="option"> <label for="female"> Female </label>

<input type="radio" id="female" name="option"> <p></p> 

<label for="usrmobile">Mobile Number</label>

<input type="text" id="usrmobile" name="usrmobile" placeholder="Mobile Number" required> 

<p></p> 

<input type="submit" name="" id="" value="submit"> </form> 

</body> 

</html> 

JS code: 

function validate() { 

var firstName = document.myForm.fname.value; 

var lastName = document.myForm.lname.value;

var userpassword = document.myForm.usrpassword.value; var usrmobile = document.myForm.usrmobile.value; console.log(firstName); 

console.log(lastName); 

console.log(userpassword); 

console.log(usrmobile); 

if (firstName == null || firstName == "" || firstName.length<3 ) { 

alert("First Name can't be blank or Less than 3 Charecter"); document.myForm.fname.focus(); 

return false; 

} 

if (lastName == null || lastName == "") { 

alert("Last Name can't be blank"); document.myForm.lname.focus(); 

return false; 

} 

if (userpassword.length < 6) {

alert("Password must be at least 6 characters long."); document.myForm.usrpassword.focus(); 

return false; 

} 

if (isNaN(usrmobile)) { 

alert("Enter Numeric value only"); document.myForm.usrmobile.focus(); 

return false; 

} 

return true; 

} 

Output : 

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.015.jpeg)

![](Aspose.Words.d3edd3d1-7c2a-4ee6-b01d-60c6cdc303ee.016.png)
