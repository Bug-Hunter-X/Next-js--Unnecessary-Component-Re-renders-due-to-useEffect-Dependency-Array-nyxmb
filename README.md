# Next.js: Unnecessary Component Re-renders due to useEffect Dependency Array

This repository demonstrates a common performance issue in Next.js applications where unnecessary re-renders occur due to improper usage of the `useEffect` hook's dependency array.

## Problem

The `MyComponent` uses `useEffect` to update a counter every second. However, because the dependency array is empty `[]`, the effect runs on every render, even though it doesn't depend on any props or state. This leads to excessive re-renders and performance degradation.

## Solution

The solution is to properly specify the dependencies for `useEffect`. In this case, as the counter is only updated based on the interval, we can remove the dependency array entirely. This ensures the effect only runs after the initial mount, solving the unnecessary re-renders.

## How to run

1. Clone the repository.
2. Install the dependencies: `npm install`
3. Run the development server: `npm run dev`