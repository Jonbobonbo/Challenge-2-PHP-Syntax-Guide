# Challenge 2: PHP Syntax Guide
## 1. PHP Comments
Creating comments in PHP allows you to make annotations that are only viewable when looking at the source code. Single line comments are represented by // or #, while multi line comments should be inside /* and */.  
This is handy to explain what parts of your code do so you don't forget, or so that anyone else who is looking can understand what your code is meant to do. 

For example:
```php
<?php

    // This is what a single line comment looks like

    # This can also represent a single line comment

    /* This comment can span
    multiple lines */

?>
```
## 2. PHP Variables
Variables in PHP are represented by the $ sign followed by the variable name. They must begin with either a letter or an underscore sign and may contain numbers, letters, and underscores. They are case sensitive and may not contain any spaces. The = sign, also called the assignment operator, is used to assign a value to a variable.   
Values as strings must be inside quotations, while numbers do not need them. Remember that semi-colon at the end of each line!   

For example:
```php
<?php

    $var1 = 22;

    $var2 = "twenty-two";

?>
```

## 3. PHP Echo/Print
Echo and print are both commands in php that display information. You can display all kinds of information this way, including strings, variables and even HTML code and they work pretty much the same with only a couple small differences. An echo command can output many different parameters while a print command can only ouput one. Print also always returns 1, which makes it slightly slower than the echo command.   

String:
```php
<?php

    echo "This is an echo";

    print "This is a print statement";

?>
```
Variable:
```php
<?php

    echo $var1;

    print $var2;

?>
```
HTML:
```php
<?php

    echo "<h1>This is an HTML header</h1>";

    print "<p>This is an HTML paragraph</p>";

?>
```
## 4. PHP Data Types
There are eight different data types supported by PHP. These data types are: integers, float (or floating point numbers), strings, booleans, arrays, objects, resources, and NULL.

### Integers:
Integers in PHP are always whole numbers and cane be expressed in several supported formats including decimal, negative numbers, hexidecimal format, and octal format.

```php
<?php

    // decimal
    $vardec = 22;

    // negative
    $varneg = -22;

    // hexidecimal
    $varhex = 0x8F;

    // octal
    $varoct = 0343
    
?>
```
### Floating Point Numbers:
A float is a number that contains a decimal point and they are generally precise up to 14 digits. The function **is_float()** can be used to determine whether a number is a float.
```php
<?php

    $float = 7.6781;
    
?>
```
### Strings:
Strings are a datatype supported by PHP, which are expressed inside quotations:
```php
<?php

    $see = "My value is a string!";
    
?>
```
### Booleans:
Booleans represent the values 1 and 0 and are most often used as true and false in PHP.
```php
<?php

    if (file_exists == true) {echo "It's true!";}
    
?>
```
### Arrays:
Arrays are variables that have multiple values, represented by key/value pairs.
```php
<?php

    $a = array("Name" => "Charles", "Age" => 74, "Occupation" => "Retired");

?>
```
### Objects;
Objects are data types that store self-contained data and processes inside them. Objects have properties and methods independant of other objects and variables.
```php
<?php

    class myobject {

        $say = "This is an object property";

        function myfunction() {

            $do = "This is an object method";

        }

    }
    
?>
```
### Resources:
A PHP resource is a type of variable that has special importance in referencing a resource outside of the script itself. This is often used to interact with files in a database or server
```php
<?php

    // the handler to open a file with read and append permissions
    $handle = fopen($file, "a+");
    
?>
```
### NULL:
NULL is an interesting data type as it represents an empty variable, meaning that it is both the data type and the only value that data type can have.
```php
<?php

    $mywealth = NULL;

?>
```
## 5. PHP Strings
PHP supports the use of strings. Strings are combinations of letters, numbers, and special characters enclosed within quotations:
```php
<?php

    echo "This is a string";

    echo 'This is also a string';

?>
```
There are also some pre-built functions you can use to manipulate strings in PHP including:
### Calculating a string's length with **strlen()**
This will tell you how many characters are in the string (including spaces):
```php
<?php

    echo strlen("How many characters are in this string?");

?>
```
### Calculating the number of words in a string with **str_word_count()**
This will output 7:
```php
<?php

    $countme = "How many words are in this string?";

    echo str_word_count($countme);

?>
```
### Replacing occurrences in a string with **str_replace()**
This example will replace the string inside the variable to read "This is an example of a party":
```php
<?php

    $varstr = "This is an example of a string";

    echo str_replace("string", "party", $varstr);

?>
```
### You can also reverse a string with **strrev()**
This example would now read "!sdrawkcab em daer t'nod esaelP":
```php
<?php

    $reverse = "Please don't read me backwards";

    echo strrev($reverse);

?>
```
## 6. PHP Numbers
The types of numbers that are available in PHP, some of which have been referenced above in data types, are integers, float, infinity, NaN, and numerical strings. The nice thing is that PHP converts to the correct data type automatically. 
```php
<?php

   // integer
   $sixteen = 16;

   // float
   $floaty = 2.490;

   // infinity: numbers that are larger than the maximum that php supports for float are considered to be infinite
   $infinite = 2.9e577;

   // NaN (not a number), usually returned when making an invalid calculation
   $what = "nine" * 8;

   // numerical string
    $realnumber = "335566";
   
?>
```
## 7. PHP Constants
Constants are created using the **define()** function. Once they are defined they cannot be changed while the script is executing but can be accessed from any scope. They differ from variables in that they do not begin with the $ sign and can only store simple values:
```php
<?php

    define('CONST', "This string is the constant's value");

    echo CONST;

?>
```
### There also some pre-defined functions in PHP that work with constants including **constant()** and **defined().**
The **constant()** function allows you to find the value of a constant even if you are unsure of its name. This may come up if are unsure of where it is initially defined but know it is being stored in a variable or used in a function. In this example it is used to call the variable that the constant is stored inside:
```php
<?php

    define('YES', 1);

    $answer = 'YES';

    echo constant($answer);

?>
```
The **defined()** function allows you to determine whether a constant has been defined or not. It returns either true or false, depending on whether that constant has been defined:
```php
<?php

    define('STARS', 190042);

    if (defined('STARS')) {

        echo "STARS is defined!";

    } else {

        echo "Sorry, STARS is not defined as a constant";

?>
```
## 8. PHP Operators
There are a *lot* of operators that are supported by PHP. There are operators for arithmetic, assigment, comparison, incrementing/decrementing, logic, strings, arrays, and comparing expressions.
### Arithmetic Operators
These operators are used for completing basic equations within php:
```php
<?php

    echo (10 + 5);  // addition
    echo (10 - 5);  // subtraction
    echo (10 * 5);  // multiplication
    echo (10 / 5);  // division
    echo (10 % 5);  // modulus (remainder)

?>
```
### Assignment Operators
These operators are what we use when assigning a value to a variable:
```php
<?php

    $five = 5; // assigns a value of 5

    $one = 1;
    $one += 2; // adds 2 to original value and and assigns new value of 3

    $ten = 10;
    $ten -= 4;  // subtracts 4 from original value and assigns new value of 6

    $seven = 7;
    $seven *= 2;  // multiplies original value by 2 and assigns new value of 14

    $eight = 8;
    $eight /= 4;  // divides original value by 4 and assigns new value of 2

    $twenty = 20;
    $twenty %= 6; // divides original value by 6 and assigns the REMAINDER as new value of 2

?>
```
### Comparison Operators
These are commonly used operators that compare values to each other. Often used in if/else statements or functions that require meeting certain conditions:
```php
<?php

  if ($a == $b) {echo "Yes";}  // if $a is equal to $b

  if ($a === $b) {echo "Yes";}  // if $a is equal to AND the same data type as $b

  if ($a != $b) {echo "No";}  // if $a is not equal to $b

  if ($a !== $b) {echo "No";}  // if $a is not equal to OR the same data type as $b

  if ($a <> $b) {echo "No";}  // if $a is not equal to $b

  if ($a < $b) {echo $a . " is greater";}  // if $a is greater than $b

  if ($a > $b) {echo $a . " is lesser";}  // if $a is lesser than $b

  if ($a >= $b) {echo $a . " is equal or greater";} // if $a is greater than or equal to $b

  if ($a <= $b) {echo $a . " us equal or lesser";}  // if $a is lesser than or equal to $b

?>
```
### Incrementing and Decrementing Operators
Sometimes you may need to increment or decrement a variable's value. That's what these are for:
```php
<?php

    $i = 1;
    echo ++$i; // pre-increment: increments the value of $i to 2 and displays 2 on the screen
    echo --$i; // pre-decrement: decrements the value of $i back to 1 and displays 1 on the screen

    $j = 1;
    echo $j++; // post-increment: displays 1 on the screen then increments the value to 2
    echo $j--; // post-decrement: displays 2 on the screen and then decrements value back to 1
   
?>
```
### Logical Operators
These operators are most often used when combining multiple conditions. This can happen in an if statement where more than one condition must be met in order to perform a specific action:
```php
<?php

    if (file_exists and user_exists) {echo "OK";} // and: if both statements are true

    if file_exists && user_exists) {echo "OK";}  // &&: if both statements are true

    if (file_exists or user_exists) {echo "OK";} // or: if either statement is true

    if (file_exists || user_exists) {echo "OK";} // ||: if either statement is true

    if (file_exists xor user_exists) {echo "OK";} // xor: if either statement is true but not both

    if (!file_exists) {echo "OK";} // !: if statement is not true

?>
```
### String Operators
There are two operators for strings in PHP and they both return concatentation:
```php
<?php

    $string = "Thank you";

    echo $string . " for coming to visit!"; // concatenates both strings

    $string .= " for coming to visit!"; // concatenates the two strings and assigns new value of $string as the concatenated version: "Thank you for coming to visit!"

?>
```
### Array Operators
These are the operators that are used with PHP arrays. 
```php
<?php

    $a = array("Name" => "Charles", "Age" => 74, "Occupation" => "Retired");
    $b = array("Chicken" => "poultry", "Steak" => "beef", "Mashed Potatoes" => "vegetable"); 

    $c = $a + $b;  // the Union operator (+) combines two arrays

    if ($a == $b) {echo "Yes";}  // the Equality operator (==) compares whether two arrays have the same key and value pairs

    if ($a === $b) {echo "Yay";}  // the Indentity operator (===) compares whether two arrays are completely identical to each other in value pairs and data type

    if ($a != $b) {echo "Sorry!";)  // the Inequality operator (!=) compares whether two arrays are not equal to each other

    if ($a <> $b) {echo "Sorry!"}  // this is also an Inequality operator (<>). Same as above

    if ($a !== $b) {echo "Not even close!"}  // the Non-Identity operator compares wether two arrays are not completely identical to each other

?>
```
### Spaceship Operator
This operator is used to compare two expressions. The actual name for it is the combined comparison operator. It does a 3 way comparison using a scale of -1, 0, or 1. If the expressions are equal it will return 0, if the left expression is greater it will return 1, and if the right expression is greater it will return -1.
```php
<?php

    echo 10 <=> 1;  // displays 1

    echo "Hey" <=> "Hey";  // displays 0

    echo 10 <=> 11;  // displays -1

?>
```

## 9. PHP If/Else and Elseif
An if/else statement in PHP is a way to set conditions to tell your code what to do and it follows a fairly simple formula: **if** (*condition*) { *execute script* } **else** {*execute different script*}. You can also use **elseif** to add more if statements, should the first not be fulfilled:
```php
<?php

    if (file_exists) {

        echo "Yes, the file exists!";

    } elseif ($a != 3) {

        echo $a . " does not equal 3!";

    } else {

        echo "ERROR: Sorry, that action could not be performed.";

    }

?>
```

## 10. PHP Functions
PHP has something called functions that are chunks of code that are contained within their own scoping and do not run unless they are activated by **calling** them. There are a number of pre-built functions that are already defined and can be used inside your script to peform different tasks. You can also create your own functions in PHP:
```php
<?php

    // defining a function
    function sayHi() {

        echo "Hi there, you look great.";

    }

    // calling the function then activates the code inside of it
    sayHi();
?>
```
## 11. PHP Arrays
Arrays are a special type of variable that have multiple (or an array of) values. Arrays are unique in the way their values are stored in pairs of **keys** and **values**. When the **key** is not defined when an array is created it defaults to a numbering system called **indexes** to define those keys. These arrays are called **indexed arrays** and each value that is defined has an index number automatically assigned to it, beginning with 0.  

If you want your keys to have a specific value, you can define them when creating the array. These are called **associative arrays** and can be useful when you need you values to be categorized with more than just a number.  

You can also store arrays *inside* other arrays. These are called **multidimensional arrays**.
```php
<?php

    // indexed array
    $fruit = array("apple", "grapes", "pineapple");

    var_dump($fruit); // this returns the array info including index numbers: array(3) { [0]=> string(5) "apple" [1]=> string(6) "grapes" [2]=> string(9) "pineapple" }

    
    // associative array. the keys are the first string in the pair and the values follow the arrow symbol
    $meals = array("breakfast" => "morning", "lunch" => "noon", "supper" => "evening");

?>
```
## 12. PHP Loop
A PHP loop is a portion of script that runs over and over with a set of conditions that tell it how to operate and when to finish. There are four types of loops in PHP:
### The while loop
This loop runs script while the specified conditions inside the circle brackets are met:
```php
<?php

    $j = 99;

    while ($j < 100) {

        $j--;
        echo $j . " bottles of beer on the wall...";

    }

?>
```
### The do...while loop
This is like the while loop but the conditions are evaluated **after** the script has run each time, instead of before:
```php
<?php

    $j = 99;

    do {
        
        $j--;
        echo $j . " bottles of beer on the wall..";

    }
    while ($j > 0);

?>
```
### The for loop
The for loop runs until a condition is met. This is a very powerful tool to automate tasks and takes 3 parameters inside the circle brackets that are separated by semi-colons. 
#### Initialization:
This is the first parameter inside the circle bracket and is most often used to define the variable being used to count with
#### Condition:
This is the second parameter and is a condition that, as long as it remains true, will keep the for loop running.
#### Increment:
The third and final parameter is used to define the increment or decrement of the variable that was defined in the first parameter.
```php
<?php

    // this will continue looping until $i decrements to equal 0
    for ($i=1; $i > 0; $i--) {

        echo $i . " bottles of beer on the wall...";

    }

?>
```
### The foreach loop
The foreach loop is used to loop through data in an array. You can loop through just the values or both the keys and values, depending on the syntax:
```php
<?php

    $a = array("Name" => "Charles", "Age" => 74, "Occupation" => "Retired");

    // loop through values
    foreach ($a as $value) {

        echo $value . "\n";

    }

    // loop through keys and values
    foreach ($a as $key => $value) {

        echo "Key: " . $key . "Value: " . $value . "\n";

    }

?>
```