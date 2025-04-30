Task 1:
When you run the line console.log(mysteryVariable);
before declaring the variable with let, it results in a ReferenceError.
This is because let and const declarations are hoisted to the top of their block, but unlike var, they are not assigned a value during hoisting.
Until the line where the variable is actually declared and initialized, it exists in a special state called the Temporal Dead Zone (TDZ). 
Accessing it during this time is not allowed and will throw an error.
Inside the revealMystery() function, the same issue occurs. 
Although mysteryVariable is declared later in the block with let, trying to access it before that point results in a ReferenceError due to the TDZ. 
Only after the declaration can it be used safely.


Task 2 Explanation:
Hoisting in JavaScript refers to the behavior where function and variable declarations are conceptually moved to the top of their containing scope during the compilation phase.
However, only the declaration is hoisted—not the assignment.
Variables declared with var are function-scoped and get initialized to undefined when hoisted. 
This is why you can reference them before the actual line of declaration without throwing an error, even though the value will be undefined.
On the other hand, let and const are block-scoped. 
Although their declarations are also hoisted, they are not automatically initialized.
Until the interpreter reaches the line where they are declared, these variables remain in the Temporal Dead Zone.
Accessing them before this point results in a ReferenceError.
