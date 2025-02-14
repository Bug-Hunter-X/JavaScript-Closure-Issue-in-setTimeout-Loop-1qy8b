# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that occurs when using `setTimeout` within a loop.  The problem arises from the way closures capture variables in their surrounding scope.  In this case, the `setTimeout` callbacks do not capture the value of `i` at the time they are created, but rather capture a reference to the variable `i`.  This means that by the time the callbacks execute, the loop has already completed, and `i` is equal to its final value of 10.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js`.
3. Run the code using Node.js or your preferred JavaScript runtime.
4. Observe the unexpected output.