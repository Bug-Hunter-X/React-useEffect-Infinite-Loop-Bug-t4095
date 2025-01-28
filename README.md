# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by modifying state within the effect without proper dependency management.

## The Bug
The `bug.js` file contains a component that attempts to increment a counter within the `useEffect` hook.  Because the effect runs on every render and modifies the state (`count`), it creates an infinite loop, causing the application to crash or become unresponsive.

## The Solution
The `bugSolution.js` file demonstrates the correct approach. By adding `count` to the dependency array, `useEffect` only runs when `count` changes. We also ensure we don't update state on every render. This prevents the infinite loop, and the counter updates correctly.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the behavior in the browser.  The initial file should cause a crash while the solution file functions correctly.
