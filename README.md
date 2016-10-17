Instructions:

- Add your answers inline to the markdown file.
- Use your own words.
- Come up with an answer from memory. Write it down, even if the answer is "I don't know."
- Then, we will go over the answers in class. Write down your revised answer below your original answer.

---
### Part 1: Control Flow - 15 minutes

1. Draw a diagram of an if statement. Name each of the components and how they work together.

 if (this condition is true) {
    execute this code
  } else if (this second condition is true) {
    execute this code
  } else {
    execute this code
  }

2. Draw a diagram of a for loop. Describe each of its components. Indicate the order in which they are executed / evaluated.

 for (variable declaration; until this condition is not true ;increment) {
   execute this code
 }

3. Functions
 - 3a. Draw a diagram of a function. Describe each of its components and what each component does. Specify which of them are optional.

var myFunction = function(parameter1, parameter2){
  execute code on parameters
  return something from the parameters//
}

 - 3b. Draw a diagram of a function being called, showing the instruction execution order.

myFunction(3,4);

var myFunction = function(parameter1, parameter2){
  execute code on parameters
  return something from the parameters (function exits after return, unless hoisting occurs)
}

---
### Part 2: Data Types - 10 minutes

4. Primitive Data Types
 - 4a. Give an example of an empty string and a non-empty string.

var emptyString = "";

var nonEmptyString = "word";


 - 4b. Give an example of a boolean.

true
false

 - 4c. Give an example of a Number.

2

5. Arrays
 - 5a. Give an example of an empty array.

var myArray = [];

 - 5b. Give an example of an array with three elements in it.

 var myArray = [3, 4, 1];


 - 5c. How do you add another element to this array?

myArray.push(5);

 - 5d. How do you get the length of this array?

myArray.length;

 - 5e. Show how to iterate through the array using a loop.

6. Objects
 - 6e. Give an example of an empty object.

var myObject = {};

 - 6b. Give an example of an object with three keys and three values.

 var myObject = {
   hair-color: "brown",
   eye-color: "hazel",
   height: 158
 };

 - 6c. Give an example of an object with two keys and two functions as values.

 var myObject = {
   hair-color: "brown",
   eye-color: "hazel",
   findBMI: function(height, weight) {
     return height*weight;
   },
   convertWeightToKg: function(weightInLbs) {
     return (1/2.2) * weightInLbs;
   },
 };


 - 6d. Describe one way of adding a key to an object.

dot notation:

 myObject.noseSize = "medium";

 - 6e. Describe the other way of adding a key to an object.

bracket notation:

 myObject["noseSize"] = "medium";


 - 6f. Explain the difference between these two ways, and when it is appropriate to use each way.
 - 6g. Describe how to iterate though an object using a loop.



---
### Part 3: Algorithms - 20 minutes

7. What is an algorithm?

 A mathematical formula

8. For the following problem, first write down how exactly to solve the problem in English. Once you are able to describe it in English, translate it into code.

```js
 Given an array of values, write a function that finds the index of where the value is located, and if nothing is found, returns -1.
 Do not use the indexOf function.
 example: for ['apple', 'orange', 'pineapple']
	 'orange' returns '1'
	 'durian' returns '-1'
```

1. create a for loop to loop through the array
2. if the element in the array matches the value, return the index
3. otherwise, continue the loop
4. If the value is not found, return -1
5. It's an if statement within a forloop. declare var result to -1, then return it at the end.

var myValues = ['apple', 'orange', 'pineapple']

var result = -1;

var findIndex = function(array, value){
  for (var i = 0; array.length ;i ++) {
    if (array[i] === value) {
      array[i] = result
    }
  }
  return result;
};

console.log(findIndex(myValues,"apple"));

console.log(findIndex(myValues,"peach"));


9. Again, for the following problem, first write down how exactly to solve the problem in English. Once you are able to describe it in English, translate it into code.

```js
 Write a function that finds all the indexes of where the value is located and returns them in an array, and if nothing is found, returns -1
 example: ['apple', 'orange', 'orange', 'pineapple']
	 'orange' returns [1,2]
```

1. declare an empty array
2. loop through the array,
3. if the value is found, add index to array
4. retun the array
5. if nothing is pushed to the array, return -1


var myFruits = ['apple', 'orange', 'pineapple']

var indexes = []

var findIndex = function(array, value){
  for (var i = 0; array.length ;i ++) {
    if (array[i] === value) {
      array.push(i);
    }

  }
if (indexes.length === 0) {
  return -1;
} else {
  return indexes;
}

};

console.log(findIndex(myFruits,"apple"));

console.log(findIndex(myFruits,"peach"));
