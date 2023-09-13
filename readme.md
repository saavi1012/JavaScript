# This repo contains the notes for the javascript.

## Word vs Keyword

Word doesn't contain any sematic in js, while key word conatins semantics

hello ---> word
for ---> keyword

##JavaScript Versions

es5 ---> old version (it includes var)
es6 ---> new version (it includes let and const)

## variable & constants

variable ---> stores changing values. 
constant ---> stores immortal values that can't be changed

## var, const & let

var ---> Variable is function scoped, that is we can use it anywhere inside the parent function.
    example: function abcd(){
                  for(var i=1;i<10;i++){
                     console.log(i);
                  }
               console.log(i);
              }
Here var is defined in the for loop but loop lies inside the abcd function, thus it can be used anywhere in that function.
Also, var adds itself to the window object.

let ---> let is braces scoped(curly braces scoped), that is it can only be used inside the curly braces. let doesn't adds itself to the window object.

const ---> I t is also braces scoped. const also doesn't adds itself to the window object.


## Hoisting

a variable or function can be used before it declaration.

console.log(a); // valid command
var a = 100;

when the interpreter encounters line number 21 it basically breaks it into two commands
var a; & then the acutall command i.e console.log(a);

## Types in Javascript

- Primitive : number, boolean, string, etc
- Reference : [], {}, () :: when these values are copied then real values aren't copied but the refernce value is passed. Changes made to these data type are affected in the main variable.

## Conditionals (if, else, else-if )

if(condition){
// statement
}
else if(condition){
// statement : if (if) condition is false
}
else{
// if above conditions are not met then else is executed.
}

## Loops (for, while, do-while)

for(var i =0; i<10;i++){

}

while(condition){

}

## Functions

function function_name(parameters){ // defination
//statements
}

function_name(arguements); // function call

## Arrays

group of similar data types values stored in a linear fashion in memory.

var arr = [1,2,3,4,5,6,7,8,9];

### Push Pop Shift Unshift Splice

arr.pop(); ---> removes the last value from the array
arr.push(10) ---> adds the given arrguement at the end of array  
 arr.shift() ---> removes the first value from the array
arr.unshift(0) ---> adds the given arguement at the beginning of the array

arr.splice(start_index, no. of elements) ---> remove elements from the middle of array

arr.splice(2,5) ---> remove from 2 index and 5 elemnets i.e (3,4,5,6,7)

## Object

1. Blank object : var a = {};
2. Filled object :
   var a= {
   name : "Shreya",
   age = 20,
   email : "workspaceshreya1210@gmail.com"
   role : function_name() {}
   }

   a.name ---> To access the property of an object

   a.name = "Shreya"; ---> to update the value of any property of an object

### Property VS Method

Any property of an object whose value is a fuction is known as Method.

### Heap Memory

It is used to store all the variables or data we create.

### Execution Context

Whenever we run or call a function, function creates its own imaginary container, where the function's code is executed, this container includes:
1. variables inside that function
2. function inside that parent function
3. lexical environment for that function.
And this imaginary container is called execution context.

### Lexical Environment

It's a chart that explains which elements can be accessed by our function and which cannot. It holds its scope and scope chain.

### Spread Operator

JavaScript spread operator (...) allows us to quickly copy all or part of an existing array or object into another array or object. It helps in copying refrence values.
 
      example:
               var a = [1,2,3,4,5];
               var b = [...a]; 

Here, by the use of (...) all values of array a are copied into b and array operation applied to b will not affect the original values of array a.

### Truthy & Falsy

Truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy. That is, all values are truthy except false, 0, -0, 0n, "", null, undefined, and NaN.

### Switch

It is used to perform different actions based on different conditions.

      example: switch(expression) {
                  case x:
                     // code 
                   break;
                   case y:
                     // code 
                   break;
                   default:
                     // code 
}

### forEach loop

It only works on array. It doesn't change your array by default, it just makes changes in the temporary copy of array and thus the original array remains same.

      example: var a = [1,2,3,4,5]
                
               a.forEach(function(val){
                     console.log(val+2);
               })

### forin loop

Here obj[key] is used to access the value of key.

example:  var obj = {
              name: "shreya"
              age: 20;
              city: "noida"
          }

          for (var key in obj){
              console.log(key, obj[key]);
          }

### do-while loop

It executes a specified statement until the test condition evaluates to false. The condition is checked after executing the statement, thus the statement executes atleast once.

### Callback functions

A callback function is a function that is passed as an argument to another function, to be “called back” at a later time. A function that accepts other functions as arguments is called a higher-order function, which contains the logic for when the callback function gets executed. 

### First Class Functions

We can use function as a value in JS.

          example: function abcd(a){
                          a();
                   } 
               
                   abcd(function(){console.log("hello");})



