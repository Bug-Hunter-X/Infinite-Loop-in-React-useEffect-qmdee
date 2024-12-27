# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite render loop due to an incorrectly configured dependency array.

## Bug Description

The `useEffect` hook is designed to perform side effects, but if it's not correctly managed, it can lead to infinite loops.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe that the console continuously logs the count value, indicating an infinite loop.

## Solution

The solution involves correctly specifying the dependency array in `useEffect`.  The dependency array determines when the effect runs.  If the array is empty (`[]`), the effect runs only after the initial render. If it includes a specific value, it runs whenever that value changes.
