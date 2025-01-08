# JavaScript Loose Equality Bug

This repository demonstrates a common JavaScript bug related to the loose equality operator (==) when handling null and undefined values.  The bug arises from the fact that `null == undefined` evaluates to true, leading to unexpected results if you're not careful in your conditional checks.

## The Bug
The `foo` function in `bug.js` intends to handle both `null` and `undefined` values by returning 0 if either is passed as an argument. However, due to the loose equality check (`==`), the function produces NaN when called with `undefined`.

## The Solution
The `bugSolution.js` file demonstrates the corrected function using strict equality (`===`) to accurately distinguish between `null` and `undefined`, ensuring the function returns the intended value for all cases.

## How to Reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run the `bug.js` file using a JavaScript interpreter (e.g., Node.js): `node bug.js`
4. Observe the unexpected output for the undefined input.
5. Then run `node bugSolution.js` to see the corrected behavior.