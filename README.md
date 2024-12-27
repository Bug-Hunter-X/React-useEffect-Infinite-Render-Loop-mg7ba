# React useEffect Infinite Render Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing infinite re-renders. The issue arises from the `useEffect` running after every render without a dependency array, leading to a continuous update cycle.

## Bug Description
The `useEffect` hook in the `MyComponent` component is called after every render because it lacks a dependency array. This leads to an infinite loop as the effect's console log triggers a re-render, which then triggers the effect again, and so on.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. In this case, the dependency array is empty (`[]`), meaning the effect will only run once after the initial render. This prevents the infinite loop.  Alternatively, we can add the `count` variable to the dependencies to trigger only when the count changes.