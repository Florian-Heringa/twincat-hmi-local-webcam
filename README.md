# TwinCAT HMI - Webcam display

Displaying static video content on the TwinCAT HMI is possible by using a preconfigured `Video` user control. Also, displaying conent from a stream is in some ways possible with an `iFrame`. But directly showing usb webcam data is currently not available.

This repository holds a `Desktop.view` example that adds a video control to the main view and uses `navigator.mediaDevices.getUserMedia` to search for a connected webcam to display in the video control.

## Instructions
Just add the provided `Desktop.view` file to a new HMI project and make sure the `.view` is set as the startup file. Opening the live view should now be able to show the connected camera.

The TwinCAT HMI engineering server is always running in the background, so it can happen that the webcam access is locked by this process. This means that when you open the live view in a browser no video is shown.

If no picture is shown anywhere, check the browser console. The error message is logged there and the documentation page can help you find the error.

## Resources
- [MDN web docs: MediaDevices: getUserMedia()](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)