# React Native useEffect Stale Closure Bug

This repository demonstrates a common bug encountered when using the `useEffect` hook in React Native.  The issue arises from directly modifying component state within the `useEffect` callback without using functional updates, resulting in stale closures and unexpected behavior.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides the corrected version.  The core problem is accessing and modifying state values directly, without considering that state updates in React are asynchronous.  This can lead to incorrect updates, especially when dealing with timers or asynchronous operations.

The solution uses the functional update pattern to ensure the component always uses the latest state value when performing updates.