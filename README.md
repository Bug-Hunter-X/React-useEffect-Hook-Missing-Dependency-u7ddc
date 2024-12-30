# React useEffect Hook Missing Dependency

This repository demonstrates a common bug in React applications: a missing dependency in the `useEffect` hook.  This can lead to unexpected behavior and difficult-to-debug issues. 

## The Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count.  However, `count` is missing from the dependency array. This causes the effect to run after every render, regardless of changes to the `count` state, leading to an infinite loop of console messages and potentially performance issues.  The cleanup function is also called unnecessarily.

## The Solution
The `bugSolution.js` file corrects this by adding `count` to the dependency array. Now, the effect only runs when the `count` state changes.