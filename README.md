# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common error in React Native applications: attempting to access component state or props before the component has fully mounted. This often leads to unexpected behavior or crashes.

## The Problem

The `bug.js` file shows how trying to access `this.props` within the constructor can cause an error.  React's lifecycle methods ensure that `this.props` is populated *after* the constructor, making this approach problematic.

## The Solution

The `bugSolution.js` file presents a corrected version. It demonstrates the proper way to handle initialization: setting the initial state to a default value and fetching/processing data within `componentDidMount` which guarantees the component has been fully rendered.