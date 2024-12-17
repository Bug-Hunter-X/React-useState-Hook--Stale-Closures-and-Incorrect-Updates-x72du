# React useState Hook Bug: Stale Closures

This repository demonstrates a common error when using the `useState` hook in React:  incorrectly modifying the state variable directly within the state update function. This leads to stale closures and unexpected behavior.

## The Bug
The `bug.js` file showcases the incorrect usage of `useState`. The `incrementCount` function attempts to update the state by directly adding 1 to `count`.  This fails to trigger a re-render with the updated value due to the stale closure problem.

## The Solution
The `bugSolution.js` file provides the correct implementation. It uses a functional update pattern:  `setCount(prevCount => prevCount + 1)`. This ensures that the update uses the latest value of the state variable.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server. You can then observe the correct and incorrect behavior in your browser.