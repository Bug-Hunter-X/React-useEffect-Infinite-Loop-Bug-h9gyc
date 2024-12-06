# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The component renders infinitely due to a missing dependency in the `useEffect` hook.  The solution shows how to fix this by correctly specifying dependencies.

## Bug Description

The `useEffect` hook in the initial `MyComponent` causes an infinite loop because the `count` variable is not included in the dependency array.  This means the effect runs after every render, causing a continuous update cycle.

## Solution

Adding `count` to the dependency array solves the issue. Now, the effect only runs when `count` changes.