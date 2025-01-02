# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common error in React Native: attempting to access component state or props before the component has fully mounted.  This often leads to undefined values and unexpected behavior.

The `bug.js` file showcases the problematic code. The `bugSolution.js` file provides the corrected implementation.

## Problem
Accessing `this.props` or `this.state` within the constructor or before `componentDidMount` can cause issues because the component's properties might not yet be initialized.

## Solution
Ensure all state and prop accesses happen after the component has mounted, ideally within `componentDidMount` or within the render method after checking for null or undefined values.  Using default values in the component's state definition can also prevent errors.