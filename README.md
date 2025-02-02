# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array. This can lead to infinite loops or incorrect updates.

## Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the count to the console. However, the dependency array is empty (`[]`). This means the effect runs after every render, causing an infinite loop because the `setCount` function changes the count in every render cycle and the component re-renders again and again.

## Solution
The `bugSolution.js` file corrects this by adding `count` to the dependency array. This ensures the effect only runs when the `count` variable changes.