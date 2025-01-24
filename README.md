# JavaScript Loose Equality Pitfall: Handling Null and Undefined

This repository demonstrates a common error in JavaScript related to loose equality (==) when dealing with null and undefined values.

The `bug.js` file contains code that incorrectly uses loose equality to check for null, leading to unexpected behavior.  The `bugSolution.js` file provides the corrected version using strict equality (===) to avoid this pitfall.

## Problem

JavaScript's loose equality operator (==) performs type coercion before comparison, which can lead to unexpected results when checking for null or undefined. In the example, `0 == null` evaluates to `true`, which causes the function to return 0 even when the input is not null, but 0.

## Solution

The solution involves using strict equality (===) instead of loose equality. Strict equality checks for both value and type equality, preventing the type coercion that can lead to incorrect comparisons with null, undefined, and 0.