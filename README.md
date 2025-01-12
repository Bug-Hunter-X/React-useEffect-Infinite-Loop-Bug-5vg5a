# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by omitting a state variable from the dependency array.

## Bug Description
The `MyComponent` function uses `useState` to track a count.  The `useEffect` hook logs the count to the console after every render. However, the `count` variable is missing from the dependency array, causing the effect to run on every render, leading to an infinite loop and console spam.

## Solution
Adding `count` to the dependency array fixes the issue.  The effect now only runs when the `count` value changes.