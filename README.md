# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook:  forgetting to include state variables in the dependency array.  This can lead to infinite loops and unexpected behavior.

## Bug Description
The `MyComponent` component uses `useState` to track a counter. The `useEffect` hook logs the current count.  However, the `count` variable is missing from the dependency array, causing the effect to run on every render, leading to an infinite loop and excessive console logging.

## Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` value changes.