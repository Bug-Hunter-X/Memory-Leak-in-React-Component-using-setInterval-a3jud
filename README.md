# React setInterval Memory Leak

This repository demonstrates a common mistake in React components using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks a cleanup function to stop the interval when the component unmounts. This causes the interval to continue running even after the component is removed from the DOM, leading to a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`. It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, preventing memory leaks.

## How to Run
1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.