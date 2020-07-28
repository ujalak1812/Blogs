##### <p align="center"><em>***** This blog post is part of the series on *****<br><strong>JavaScript : ES6</strong></em></p>
##### <p align="center"><em>Originally Published at</em> [https://dev.to/ujalak1812](https://dev.to/ujalak1812/the-3-ways-of-declaring-variables-in-javascript-3hoe)

# 3 Ways of Declaring Variables in JavaScript

Till ES5, variables in javascript were declared with the keyword  *var*. From ES6, two new keywords i.e. *let* and *const* were introduced for variable declaration. Now, what's the difference between all three? Well, the difference lies in their scope and whether the value of the variable can be changed later on or not.

## 1. Reassignment

### Variables declared with *var*

Variable declaration with *var* is the old JavaScript method of declaring variables. A variable can be declared with *var* as :
            
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img15.PNG"/>
</p>
            
These variables can be assigned new values later on without any problem.
            
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img16.PNG"/>
</p>

### Variables declared with *let*

Variable declaration with *let* is one of the two new methods of declaring variables that were introduced in ES6. A variable can be declared with *let* as :
        
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img17.PNG"/>
</p>
        
These variables can also be assigned new values later on without any problem.
        
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img18.PNG"/>
</p>

### Variables declared with *const*
	
Variable declaration with *const* is another method of declaring variables that was introduced in ES6. A variable can be declared with *const* as :
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img19.PNG"/>
</p>
	
These variables cannot be assigned new values later on because *const* declares a constant. A constant value is one that never changes so, if we try to reassign a constant variable, we will run into an error, i.e.
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img20.PNG"/>
</p>
	
Note : *const* must be assigned a value at the time of its declaration, for example, this is not allowed
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img21.PNG"/>
</p>
	
But this is not the case with *let* and *var*.
	
## 2. Scope differences
	
Variables declared with *var* in ES5 are function-scoped, but variables declared with *let* and *const* in ES6 are block-scoped. Now, what does that mean? 
	
A variable declared with *var* anywhere in the function is accessible within the whole function. For example, if we declare a variable within an if statement inside a function, that variable is also accessible outside of that if block.
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img22.PNG"/>
</p>
	
Whereas, if the variable is declared with *let*, it is only accessible inside the same block where it is declared. In this case, it is only accessible inside the if block and not accessible anywhere else outside that if block.
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img23.PNG"/>
</p>
	
The same is the case with *const*.
	
## 3. Hoisting

Another difference is hoisting of variables declared with *let* and *var*. When using *var*, variables are set to 'undefined' during hoisting. For example, here the console statement prints undefined because the variable carModel is hoisted and is set to *undefined*.
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img24.PNG"/>
</p>
	
In case of *let* and *const*, this does not happen. For example, here the console statement throws an error.
	
<p align="center">
    <img src="https://raw.githubusercontent.com/ujalak1812/Blogs/master/images/img25.PNG"/>
</p>
	
Does this mean that variables declared with *let* and *const* are not hoisted? No, the variables are hoisted but they are not set to *undefined* and are not available for use until they are declared. This happens because of something called the ***temporal-dead zone***.
	

## So, What to use for the variable Declaration?

If you are working with ES6, the best practice is to use *let* for variables that will change the value over time and *const* for variables that cannot be reassigned.

.

If you have any queries and suggestions, leave them in the comments below.😊
