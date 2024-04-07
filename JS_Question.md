There is javascript interview quetions.

1. Write a program to take a number input from user and print multiplication table 12 times for that number.

   function multiplication(num) {
   let result = [];
   for (let i = 1; i <= 12; i++) {
   result.push(num \* i);
   }
   return result;
   }
   console.log(multiplication(2));

2. Write a program to return a Fibonacci series : 0,1,1,2,3,5,8,13,21....

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

3. Write a program to take an input from a user and find its Factorial. Example: Factorial of 5 is 120.

   function factorial(num) {
   if (num == 0) {
   return 1;
   }
   return num \* factorial(num - 1);
   }
   console.log(factorial(5));

4. Write a Program to take a number input from user and find if the number is Prime or not.

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

5. Write a program to take a day as an input and determine whether it is a weekday or weekend. Example: Tuesday is weekday.

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

6. Given a and b, your function should return the value of ab.
   Example: Input: power(2,3) ––> Output: 8

   function squareRoot(a, b) {
   return 4 \*\* 3;
   }
   console.log(squareRoot(4, 3));

7. Given length of a regular hexagon, your function should return area of the hexagon. Example: Input: areaOfHexagon(10) ––> Output: 259.80
   <!-- 3✓3 / 2 \_ pow(a,2); -->

   function areaOfHexagon(val) {
   let area = (3 \_ Math.sqrt(3) \* Math.pow(val, 2)) / 2;
   return area;
   }
   console.log(areaOfHexagon(10));

8. Given a sentence, your functions should return the number of words in the sentence. Example: Input: noOfWords(We are neoGrammers) ––> Output: 3

   function numberOfWord(data) {
   let words = data.split(" ");
   return words.length;
   }
   console.log(numberOfWord("we all in one"));

9. Given n numbers, your function should return the minimum of them all. The number of parameters won't be accepted from user.
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
    function mergeArray() {}
