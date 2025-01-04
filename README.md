# React Unexpected State Update Bug

This repository demonstrates a common React bug related to batched state updates.  In React, multiple state updates within a single event handler are batched together.  This can lead to unexpected behavior if you're not aware of this optimization.

## The Bug
The `bug.js` file shows a component where clicking the button is supposed to increment the count by 2. However, due to React's batching, only the last state update (`setCount(count + 1)`) is applied, resulting in an increment of only 1.

## The Solution
The `bugSolution.js` file demonstrates how to resolve this issue using the functional update form of `setCount`. This ensures that the update always uses the latest state value.

## How to reproduce the bug
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the behavior of the increment button in the browser.
