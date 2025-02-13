# Expo ImagePicker Crash on Android

This repository demonstrates a bug in the Expo ImagePicker library where the application crashes on Android devices when selecting multiple images. The crash happens without providing any specific error message, making debugging particularly challenging.

## Bug Description

When using ImagePicker to select multiple images on an Android device, the application crashes. No errors are logged to the console, making it difficult to pinpoint the root cause. This behavior is not consistent on iOS devices.

## Steps to Reproduce

1. Run the project on an Android emulator or device.
2. Open the ImagePicker using the provided button.
3. Select multiple images.
4. Observe the application crash without any error message.

## Solution

A solution has been implemented in `bugSolution.js` that addresses this issue. The key change is to handle the potential `null` value that can be returned from ImagePicker when the selection is cancelled.  This check prevents the crash by ensuring that the image data is valid before further processing.