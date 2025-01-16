# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common issue in React applications: an `useEffect` hook that runs after every render, causing unnecessary re-renders and potentially performance problems.  The example shows how to fix this by adding a dependency array to the `useEffect` hook.

## Problem

The original `MyComponent` uses `useEffect` without a dependency array. This means the effect runs after every render, logging the current count to the console. While this might be harmless in a simple example, it can lead to performance issues and unexpected behavior in more complex applications.

## Solution

The solution involves adding a dependency array to the `useEffect` hook. In this case, the dependency array is `[count]`, which means the effect will only run when the value of `count` changes.