## Problem 1: The Persistent Counter
We want to create a counter generator function, createCounter, that returns a new counter function each time it's called. This returned function should increment and return its own private count, every time it's invoked.
Each call to createCounter() creates a new count variable inside a new execution context.
The returned incrementCounter() function forms a closure over that specific count.
This means counterA and counterB are completely independent. They don't share the same count.
