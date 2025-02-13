# React useEffect setInterval Memory Leak
This example demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`.  The issue arises from failing to properly clean up the interval using `clearInterval` when the component unmounts, leading to a memory leak. The counter continues to increment even after the component is removed from the DOM.  The solution demonstrates the correct way to handle cleanup in this scenario.

## Bug
The `bug.js` file contains the faulty implementation.  The `setInterval` function is called without a cleanup function, creating a memory leak.