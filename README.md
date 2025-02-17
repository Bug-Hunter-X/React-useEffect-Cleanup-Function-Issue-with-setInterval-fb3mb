# React useEffect Cleanup Function Issue with setInterval

This repository demonstrates a common issue with the `useEffect` hook in React involving `setInterval` and cleanup functions.  The initial implementation incorrectly manages the interval, leading to potential memory leaks.

The `bug.js` file contains the problematic code. The `bugSolution.js` file provides the corrected version with proper cleanup and explanation.

## Problem:

In the provided code, the `setInterval` function within the `useEffect` hook isn't properly cleaned up when the component unmounts.  This can cause unexpected behavior such as the counter continuing to increment even after the component is removed from the DOM.

## Solution:

The solution ensures that `clearInterval` is called within the cleanup function to properly stop the interval when the component unmounts.

## How to run:

1. Clone the repository
2. Run `npm install`
3. Run `npm start`