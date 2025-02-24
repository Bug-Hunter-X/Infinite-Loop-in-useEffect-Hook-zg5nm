# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by an empty dependency array. 

The `bug.js` file contains the erroneous code. The `bugSolution.js` file shows the corrected code.

## Description

The problem arises because the `useEffect` hook is called every time the component renders. With an empty dependency array (`[]`), the effect runs only once after the initial render. However, the effect function itself includes a `console.log` statement, which will continue to log values to the console, resulting in an apparent infinite loop.