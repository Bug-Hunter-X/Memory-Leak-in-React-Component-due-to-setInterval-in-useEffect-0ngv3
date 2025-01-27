# React UseEffect setInterval Memory Leak
This example demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without providing a cleanup function. This leads to memory leaks and unexpected behavior.

## Problem
The `setInterval` function continues to run even after the component is unmounted. This can cause memory leaks, particularly if the component is frequently mounted and unmounted.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook. This function clears the interval before the component is unmounted. This ensures that resources are released correctly.