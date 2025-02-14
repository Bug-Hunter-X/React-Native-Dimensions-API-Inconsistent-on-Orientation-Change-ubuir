# React Native Dimensions API Inconsistency on Orientation Change

This repository demonstrates a bug in React Native where the `Dimensions` API returns incorrect screen dimensions after an orientation change.  The issue is particularly noticeable when the app's layout relies on the accurate dimensions provided by this API.

## Problem

The `Dimensions.get('window')` and `Dimensions.get('screen')` methods might not update immediately after the device's orientation changes. This results in the app using outdated dimensions for rendering, leading to misaligned or cut-off UI elements.

## Solution

The solution involves using the `Dimensions` API in conjunction with the `Dimensions.addEventListener` method to listen for orientation changes and update the dimensions accordingly. This ensures that the app always uses the current, correct screen dimensions.

## Steps to Reproduce

1. Clone the repository
2. Run the app in a simulator or on a physical device.
3. Rotate the device between portrait and landscape mode.
4. Observe how the layout changes, potentially breaking when the dimensions aren't updated correctly.

## How to fix

Use the provided `DimensionsBugSolution.js` file as a reference for implementing the solution.