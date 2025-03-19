# Simple Video Recorder

A modern, browser-based video recorder application that allows users to easily record, save, and manage video recordings directly in their browser. The application provides a clean, intuitive interface for video recording with features like duration tracking, local storage management, and download capabilities.

## Features

- **Live Video Recording**: Capture video with audio using your device's camera and microphone
- **Real-time Duration Display**: Track recording duration with a built-in timer
- **Local Storage**: Automatically saves recordings using IndexedDB for persistent storage
- **Recording Management**: View, play, download, and delete saved recordings
- **Storage Monitoring**: Track storage usage and available space
- **Modern UI**: Clean and responsive interface with smooth animations
- **Download Support**: Export recordings in WebM format
- **Confirmation Dialogs**: Prevent accidental deletion of recordings

## Technologies Used

- **HTML5 Media APIs**: Utilizing `getUserMedia` for camera/microphone access and `MediaRecorder` for video capture
- **IndexedDB**: Browser-based database for efficient local storage of video recordings
- **Modern CSS**: 
  - Flexbox for responsive layouts
  - CSS Grid for structured content
  - CSS Animations for smooth visual feedback
  - Linear gradients for modern aesthetics
- **JavaScript ES6+**: 
  - Promises for async operations
  - Blob API for video data handling
  - Modern event handling

## Why These Technologies?

- **HTML5 Media APIs**: Provides native browser support for media capture without requiring external plugins
- **IndexedDB**: Offers robust local storage solution for large video files with better performance than localStorage
- **Modern CSS**: Ensures responsive design and smooth user experience across devices
- **Vanilla JavaScript**: Keeps the application lightweight and fast without external dependencies


## Browser Support

This application works best in modern browsers that support the following features:
- MediaRecorder API
- IndexedDB
- getUserMedia API
- WebM video format

## Demo

Try the live demo: [Simple Video Recorder Demo](https://jakcal.github.io/simple-video-recorder)
