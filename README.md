# React 19 useEffect Unexpected Behavior

This repository demonstrates a subtle bug encountered in React 19 where a `useEffect` hook, despite having a properly defined dependency array, fires on every render instead of only when the specified dependency changes.  The issue is particularly relevant when dealing with state updates that might indirectly trigger re-renders.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs – you will see the message 'Component rendered with count:' printed more frequently than expected.

## Solution

The provided solution addresses this issue using techniques to ensure the effect is called only when needed, improving performance and preventing unnecessary side effects. Review `bugSolution.js` for the fix.  This might involve more sophisticated state management or optimization techniques based on the specific application context.