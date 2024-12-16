# React useEffect Hook: Missing Dependency Bug

This repository demonstrates a common error in React's `useEffect` hook:  forgetting to include dependencies in the dependency array.  This can lead to unexpected behavior, often an infinite rendering loop.

## The Bug

The `bug.js` file contains a `MyComponent` that uses the `useEffect` hook to log the current `count`.  However, the `count` variable is missing from the dependency array.  This means that the effect runs after *every* render, causing the `count` to constantly update and triggering another render, creating an infinite loop.

## The Solution

The `bugSolution.js` file corrects the issue by including `count` in the dependency array.  Now, the effect only runs when the `count` value changes.