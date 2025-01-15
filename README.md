# React Native useEffect Hook with Function Dependency Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React Native with a function dependency. The problem arises because React compares function references, not their contents, leading to unintended re-renders.

## Problem

The `useEffect` hook is incorrectly configured with a function as a dependency. Each render generates a new function reference, triggering the effect unnecessarily. This often leads to infinite render loops or other unpredictable behavior.

## Solution

Use `useCallback` to memoize the function, ensuring that the reference remains constant unless its dependencies change. This prevents unnecessary re-renders and resolves the issue.