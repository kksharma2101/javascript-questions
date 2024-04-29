There is javascript interview quetions.

1.  Write a program to take a number input from user and print multiplication table 12 times for that number.

    function multiplication(num) {
    let result = [];
    for (let i = 1; i <= 12; i++) {
    result.push(num \* i);
    }
    return result;
    }
    console.log(multiplication(2));

2.  Write a program to return a Fibonacci series : 0,1,1,2,3,5,8,13,21....

    function FibonacciSeries(num) {
    const result = [];
    let a = 0;
    let b = 1;
    for (let i = 0; i < num; i++) {
    if (i === 0) {
    result.push(a);
    } else if (i === 1) {
    result.push(b);
    } else {
    result.push(i - 1 + i);
    }
    }
    return result;
    }
    console.log(FibonacciSeries(9));

3.  Write a program to take an input from a user and find its Factorial. Example: Factorial of 5 is 120.

    function factorial(num) {
    if (num == 0) {
    return 1;
    }
    return num \* factorial(num - 1);
    }
    console.log(factorial(5));

4.  Write a Program to take a number input from user and find if the number is Prime or not.

    function isPrime(num) {
    if (num <= 1) {
    return false;
    } else if (num <= 3) {
    return true;
    } else if (num % 2 === 0 || num % 3 === 0) {
    return false;
    }
    let i = 5;
    while (i \* i <= num) {
    if (num % i === 0 || num % (i + 2) === 0) {
    return false;
    }
    i += 6;
    }
    return true;
    }
    console.log(isPrime(24));

5.  Write a program to take a day as an input and determine whether it is a weekday or weekend. Example: Tuesday is weekday.

    function determineDay(day) {
    let result = null;
    const value = day.toLowerCase();
    if (value !== "sunday") {
    result = "weekday";
    } else {
    result = "weekend";
    }
    return result;
    }
    console.log(determineDay("SundAY"));

6.  Given a and b, your function should return the value of ab.
    Example: Input: power(2,3) ––> Output: 8

    function squareRoot(a, b) {
    return 4 \*\* 3;
    }
    console.log(squareRoot(4, 3));

7.  Given length of a regular hexagon, your function should return area of the hexagon. Example: Input: areaOfHexagon(10) ––> Output: 259.80
    <!-- 3✓3 / 2 \_ pow(a,2); -->

    function areaOfHexagon(val) {
    let area = (3 \_ Math.sqrt(3) \* Math.pow(val, 2)) / 2;
    return area;
    }
    console.log(areaOfHexagon(10));

8.  Given a sentence, your functions should return the number of words in the sentence. Example: Input: noOfWords(We are neoGrammers) ––> Output: 3

    function numberOfWord(data) {
    let words = data.split(" ");
    return words.length;
    }
    console.log(numberOfWord("we all in one"));

9.  Given n numbers, your function should return the minimum of them all. The number of parameters won't be accepted from user.
    Example:
    Input: findMin(3,5) ––> Output: 3
    Input: findMin(3,5,9,1) ––> Output: 1
    (Hint: Lookup rest parameters in JavaScript)

    function returnMinimum(...data) {
    for (let i = 0; i < data.length; i++) {
    for (let j = 0; j < data.length; j++) {
    if (data[j] > data[j + 1]) {
    let temp = data[j];
    data[i] = data[j + 1];
    data[j + 1] = temp;
    }
    }
    }
    return data[0];

    <!-- second way -->

    if (data.length === 0) {
    return data;
    }
    let min = data[0];
    for (let i = 1; i < data.length; i++) {
    if (data[i] < min) {
    return data[i]; Update min if the current argument is smaller
    }
    }
    }
    console.log(returnMinimum(2, 3, 1, 4, 5, 6, 45));
    console.log(returnMinimum(210, 542, 362, 78, 425, 536, 35));

10. Given three angles of a triange, your function should return if it is a scalene, isosceles, equilateral triangle or not a triangle at all.
    Example:
    Input: typeOfTriangle(30, 60, 90) ––> Output: Scalene Triangle

    function findTringle(...data) {
    let triangle = null;
    if (data[0] === data[1] && data[2]) {
    return (triangle = "Equilateral");
    } else if (
    data[0] === data[1] ||
    data[1] === data[2] ||
    data[0] === data[2]
    ) {
    return (triangle = "Isosceles");
    } else if (data[0] !== data[1] || data[1] !== data[2] || data[2] || data[0]) {
    return (triangle = "scalene");
    }
    return triangle;
    }
    console.log(findTringle(202, 21, 20));

11. Given an array and an item, your function should return the index at which the item is present.
    Example:
    Input: indexOf([1,6,3,5,8,9], 3) ––> Output: 2

    function findIndex(item, num) {
    for (let i = 0; i < item.length; i++) {
    if (item[i] == num) {
    return i;
    }
    }
    }
    console.log(findIndex([1, 6, 3, 5, 8, 9], 8));

12. Given an array and two numbers, your function should replace all entries of first number in an array with the second number.
    Example:
    Input: replace([1,5,3,5,6,8], 5, 10) ––> Output: [1,10,3,10,6,8]

    function replaceNumber(data, num1, num2) {
    for (let i = 0; i < data.length; i++) {
    if (data[i] == num1) {
    data[i] = num2;
    }
    }
    console.log(data);
    }
    console.log(replaceNumber([1, 5, 3, 5, 6, 8], 5, 10));

13. Given two arrays, your function should return single merged array.
    Example: Input: mergeArray([1,3,5], [2,4,6]) ––> Output: [1,3,5,2,4,6]

    function mergeArray(data1, data2) {
    return data1.concat(data2);
    }
    console.log(mergeArray([1, 3, 5], [2, 4, 6]));

14. Given a string and an index, your function should return the character present at that index in the string.
    Example:
    Input: charAt("neoGcamp", 4) ––> Output: c

    function charAt(value, index) {

    for (const key in value) {
    if (key == index) {
    return value[key];
    }
    }
    }
    console.log(charAt("neoGcamp", 4));

15. Given two dates, your function should return which one comes before the other.
    Example:
    Input: minDate('02/05/2021', '24/01/2021') ––> Output: 24/01/2021.

    function minDate(date1, date2) {
    const [day1, month1, year1] = date1.split("/").map(Number);
    const [day2, month2, year2] = date2.split("/").map(Number);

    if (year1 <= year2 && month1 <= month2 && day1 < day2) {
    return date1;
    } else if (year1 == year2 && month1 == month2 && day1 == day2) {
    return "Both are same";
    } else {
    return date2;
    }
    }
    console.log(minDate("03/05/2021", "02/05/2021"));

16. Write a function which generates a secret code from a given string, by shifting characters of alphabet by N places. Example:
    Input: encodeString("neogcamp", 2) ––> Output: pgqiecor
    Explanation: 2 represents shifting alphabets by 2 places. a –> c, b –> d, c –> e and so on.

17. Given a sentence, return a sentence with first letter of all words as capital.
    Example:
    Input: toSentenceCase('we are neoGrammers') ––> Output: We Are NeoGrammers

    function toCapitalize(tense) {
    return tense
    .split(" ")
    .map((pre) => pre.charAt(0).toUpperCase() + pre.slice(1))
    .join(" ");
    }
    console.log(toCapitalize("we are neoGrammers"));

18. Given an array of numbers, your function should return an array in the ascending order.
    Example:
    Input: sortArray([100,83,32,9,45,61]) ––> Output: [9,32,45,61,83,100]

        function numAscendeing(data) {

    return data.sort((a, b) => a - b);
    }
    console.log(numAscendeing([100, 83, 32, 9, 45, 61]));

19. Given a sentence, your function should reverse the order of characters in each word, keeping same sequence of words.
    Example:
    Input: reverseCharactersOfWord('we are neoGrammers') –––> Output: ew era sremmarGoen.

    function reverseString(str) {
    return str
    .split(" ")
    .map((pre) => pre.split("").reverse().join(""))
    .join(" ");
    }
    console.log(reverseString("we are neoGrammers"));

20. Write a JavaScript program to calculate the simple interest given P,R,T with the given formula. Formula: SI = (P _ T _ R) / 100 Where: P = principal amount T = time R = rate SI = simple interest

    function simpleInterest(val) {
    let data = val;
    let si = (data.amount _ data.rate _ data.time) / 100;
    return si;
    }
    console.log(simpleInterest({ amount: 100, rate: 6, time: 2 }));

21. Write a program to calculate the kinetic energy of a body with mass 'm' and volume 'v'.
    Formula : 0.5 _ m _ v \_ v

    function calculateKE(m, v) {
    let kineticEnergy = 0.5 _ m _ v \_ v;
    return kineticEnergy;
    }
    console.log(calculateKE(8, 6));

22. Write a program to convert Fahrenheit to Celsius. For Fahrenheit to Celsius conversion use: C = (F - 32) \_ 5/9 'F' and 'C' are the temperatures on the Fahrenheit scale and Celsius scale respectively.
    // input: 56 output: 13.3333

    function convertTem(F) {
    let result = ((F - 32) \_ 5) / 9;
    return result;
    }
    console.log(convertTem(56));

23. Calculate the area, perimeter of a square of side 'a'. Also, calculate the surface area and the volume of a cube of side 'a'.
    // Formula : Area: a*a ,Perimeter: 4*a ,Surface Area: 6*a*a ,Volume: a*a*a

    function calculateArea(a) {
    let area = a _ a;
    let perimeter = 4 _ a;
    let surfaceArea = 6 _ a _ a;
    let volume = a _ a _ a;
    return `area : ${area}, perimeter : ${perimeter}, surface area : ${surfaceArea}, Volume : ${volume}`;
    }
    console.log(calculateArea(4));

24. Write a program to calculate sum of N natural digits, as input by the users?
    // Enter a positive integer: 100, Sum = 5050

    function sumOfNaturalNum(num) {
    let res = (num \* (num + 1)) / 2;
    return res;
    }
    console.log(sumOfNaturalNum(100));

25. Write a Program to Print N Odd Number in Descending Order.
    // Input: 4; Output: 7; 5; 3; 1;

    function printOddNum(num) {
    let count = num;
    let oddNumber = 2 \* num - 1; // The first odd number to start from
    while (count > 0) {
    console.log(oddNumber);
    oddNumber -= 2;
    count--;
    }
    }
    console.log(printOddNum(4));

26. Write a JavaScript program to compute the sum of all digits that occur in a given string.
    // Input: 1234, Output: 1+2+3+4 = 10

    function sumOfAllDigits(num) {
    let sum = 0;
    for (let i = 0; i <= num.length; i++) {
    sum += i;
    }
    return sum;
    }
    console.log(sumOfAllDigits(1234));

27. Find square

    function SquareFind(num) {
    const integerSquares = [];
    console.log(num);
    for (let i = 0; i <= num; i++) {
    let square = i \* i;
    if (square <= num) {
    integerSquares.push(square);
    }
    }
    return integerSquares;
    }
    console.log(SquareFind(50));

28. Write a JavaScript program that reverses a number.
    // Input: 32243; Output: 34223;

    function reverseNum(num) {
    let rev = num.toString().split("").reverse().join("");
    return rev;
    }
    console.log(reverseNum(32243));

29. Write a Program to cyclically Rotate a Number by X positions in the left direction, as provided by the user.
    // Enter a Number : 1234; Enter the Number of Rotations : 2; Output : 3412

    function numRotate(val) {
    let newVal = val.toString().split("");
    let res = [];
    let x = 4;
    for (let i = x; i <= newVal.length - 1; i++) {
    let temp = newVal[i];
    res.push(temp);
    }
    for (let i = 0; i < x; i++) {
    res.push(newVal[i]);
    }
    return res.toString();
    }
    console.log(numRotate(123495708));

30. Write a Program to convert Decimal to Binary.
    // Example: 5; Binary number of 5 = 101;

    function decimalToBinary(val) {
    if (val == 0) {
    return 0;
    }
    let binary = "";
    while (val > 0) {
    binary = (val % 2) + binary;
    val = Math.floor(val / 2);
    }
    return binary;
    }
    console.log(decimalToBinary(57));

31. Write a program that reads two strings and append first string to the second. So if first string is Good second string is Morning , the program should print MorningGood;

    function appentString(str1, str2) {
    // let res1 = str2 + str1;
    let res2 = str2.concat(str1);
    return res2;
    }
    console.log(appentString("Good", "Morning"));

32. Write a program to delete all vowels from a string. Assume string is not more than 80 characters long.

    function removeVowels(str) {
    let res = str.toString().split("");
    let result = "";
    for (let i = 0; i < res.length; i++) {
    if (res[i] !== "a" && "e" && "i" && "o" && "u") {
    result += res[i];
    }
    }
    return result.toString().split("");
    }
    console.log(removeVowels("abcdefghijklmnopqrstuvwxyz"));

33. A program that counts number of vowels and consonants in a String?

    function countVowelsAndConsonants(str) {
    let vowels = "aeiouAEIOU";
    let vCount = 0;
    let cCount = 0;
    for (let i = 0; i < str.length; i++) {
    let char = str[i];
    if (char.match(/[a-zA-Z]/)) {
    if (vowels.includes(char)) {
    vCount += 1;
    } else {
    cCount += 1;
    }
    }
    }
    return `vowels: ${vCount} and consonants: ${cCount}`;
    }
    console.log(countVowelsAndConsonants("he is developer"));

34. Given a string, determine if it is a palindrome, considering only alphanumeric characters.

    function checkPalindrome(str) {
    let updateStr = str.replace(/[^a-z]/g, "");
    let start = 0;
    let end = updateStr.length - 1;
    while (start <= end) {
    if (updateStr[start] !== updateStr[end]) {
    return false;
    }
    start++;
    end--;
    }
    return true;
    }
    console.log(checkPalindrome("kamal574 1 23am ak "));

35. For a given input string(str), write a function to print all the possible substrings.Without using substr method.

        function printSubstrings(str) {
        // Loop through each character in the string

        for (let start = 0; start < str.length; start++) {
        for (let end = start + 1; end <= str.length; end++) {

        // Print substring from start index to end index
        console.log(str.slice(start, end));
        }
        }
        }

    const inputString = "hello";
    printSubstrings(inputString);

36.
