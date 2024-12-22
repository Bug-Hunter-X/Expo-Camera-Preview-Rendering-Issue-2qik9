# Expo Camera Preview Rendering Issue

This repository demonstrates a bug encountered when using the Expo Camera API. The camera preview fails to render on the initial screen load but functions correctly after navigating away and returning. The inconsistency across different devices and Expo SDK versions makes debugging difficult.

## Bug Description

The `Camera` component from Expo fails to display the camera preview upon initial render.  A blank screen is displayed instead.  However, after navigating to another screen and then back to the screen containing the `Camera` component, the preview renders as expected. Permissions are correctly granted.  This problem occurs intermittently, not consistently. 

## Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using Expo Go or a similar method.
4. Observe the blank screen where the camera preview should be.
5. Navigate to another screen and then return to the camera screen.
6. The camera preview should now render correctly. 

## Solution

The solution involves adding a small delay before rendering the camera, giving it time to initialize properly, which fixes the intermittent blank screen issue.   The solution code is in bugSolution.js