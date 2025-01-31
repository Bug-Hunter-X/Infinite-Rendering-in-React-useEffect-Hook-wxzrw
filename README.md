# React useEffect Infinite Rendering Bug

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.  The `MyComponent` initially renders correctly, but subsequent state changes cause an infinite loop. 

## Bug Description
The `useEffect` hook, without a dependency array, runs after every render.  This creates a loop where each render triggers the effect, which in turn triggers another render, resulting in an infinite render cycle and potentially browser crashes.