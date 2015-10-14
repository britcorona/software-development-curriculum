# Closures
Closures are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created.
## Example
A closure is a function having access to the parent scope, even after the parent function has closed.

```
var add = (function () { 
    var counter = 0;
    return function () {return counter += 1;}
})();

add();
add();
add();

 //the counter is now 3 
```
* The variable add is assigned the return value of a self-invoking function.
* The self-invoking function only runs once. It sets the counter to zero (0), and returns a function expression.
* This way add becomes a function. The "wonderful" part is that it can access the counter in the parent scope.
* This is called a JavaScript closure. It makes it possible for a function to have "private" variables.
* The counter is protected by the scope of the anonymous function, and can only be changed using the add function.



## Sources and Further Reading
* http://www.w3schools.com/js/js_function_closures.asp
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
