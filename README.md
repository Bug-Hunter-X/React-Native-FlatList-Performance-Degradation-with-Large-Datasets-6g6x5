# React Native FlatList Performance Bug

This repository demonstrates a performance issue with React Native's `FlatList` component when dealing with extensive datasets. The problem stems from inefficient rendering and repeated calls to the `renderItem` function, causing slow rendering and potential app crashes.

## Bug Description

The bug is observed with a `FlatList` component rendering a large number of items. The scrolling becomes sluggish, and the app may freeze or crash, especially on lower-end devices. This is due to the excessive computations involved in rendering every item simultaneously.

## Solution

The solution involves using `windowSize` and `maxToRenderPerBatch` props in `FlatList`.  These props control the number of items rendered at a time, significantly improving performance.  Further optimizations using `getItemLayout` can also be explored for even better performance.

## Setup

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to start the app.
