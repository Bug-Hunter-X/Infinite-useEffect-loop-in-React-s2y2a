# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite useEffect loop caused by incorrectly specifying the dependency array.  The bug causes the component to re-render continuously, leading to performance degradation and excessive console output. The solution shows how to fix this by correctly defining the dependencies.

## Bug Description:
The `useEffect` hook in the provided `MyComponent` runs after every render because it does not specify any dependencies. This creates an infinite loop as the component constantly updates itself, triggering the `useEffect` again. 

## Solution:
The solution correctly specifies the `count` variable in the dependency array (`[count]`). This ensures that the effect only runs when the `count` value changes.