# Spatial Mask - AR Face Filter Project

## Project Overview

Spatial Mask is an Augmented Reality (AR) web application that allows users to try on different superhero masks in real-time using their device's camera. The project uses face tracking technology to create an immersive AR experience.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Technical Architecture](#technical-architecture)
4. [Implementation Details](#implementation-details)
5. [User Guide](#user-guide)
6. [Future Enhancements](#future-enhancements)
7. [Conclusion](#conclusion)

## Introduction

Spatial Mask is a web-based AR application that enables users to experience different superhero masks through their device's camera. The project combines computer vision, face tracking, and web technologies to create an interactive and engaging user experience.

### Problem Statement

Traditional photo filters are static and limited in their interaction. Users want a more immersive and interactive way to experience different character masks in real-time.

### Solution

Spatial Mask provides a real-time AR experience where users can:

- Try on different superhero masks
- See the masks track their facial movements
- Capture photos with the masks
- Switch between different masks seamlessly

## Features

### 1. Real-time Face Tracking

- Uses MediaPipe Face Mesh for accurate face detection
- Tracks 468 facial landmarks
- Provides smooth mask alignment with facial features

### 2. Multiple Mask Options

- Iron Man Mask
  - Red and gold color scheme
  - Glowing arc reactor
  - Angular eye design
- Batman Mask
  - Black base with bat ears
  - White eye holes
  - Yellow bat symbol
- Spider-Man Mask
  - Red base with web pattern
  - White eye holes with web design
  - Dynamic web lines
- Shakthi Man Mask
  - Blue base design
  - White eye holes
  - Glowing lightning bolt symbol

### 3. Interactive Controls

- Camera toggle (front/back)
- Music control
- Photo capture
- Mask selection buttons

### 4. Audio Integration

- Background music support
- Music toggle functionality
- Volume control

## Technical Architecture

### Frontend Technologies

1. HTML5

   - Structure and layout
   - Canvas for AR rendering
   - Audio elements

2. CSS3

   - Responsive design
   - Animations and transitions
   - UI component styling

3. JavaScript
   - Face tracking implementation
   - Canvas drawing
   - Event handling
   - Audio control

### External Libraries

1. MediaPipe Face Mesh

   - Face detection
   - Landmark tracking
   - Real-time processing

2. Camera Utils
   - Camera access
   - Stream handling
   - Device compatibility

## Implementation Details

### Face Tracking System

```javascript
// Face mesh initialization
faceMesh = new FaceMesh({
  locateFile: (file) => {
    return `https://cdn.jsdelivr.net/npm/@mediapipe/face_mesh/${file}`;
  },
});

// Configuration
faceMesh.setOptions({
  maxNumFaces: 1,
  refineLandmarks: true,
  minDetectionConfidence: 0.5,
  minTrackingConfidence: 0.5,
});
```

### Mask Rendering

Each mask is implemented using Canvas 2D API:

- Dynamic scaling based on face size
- Real-time position updates
- Custom effects and animations

### Audio System

```javascript
// Audio control implementation
function toggleMusic() {
  if (isMusicPlaying) {
    bgMusic.pause();
    musicButton.textContent = '🔊';
  } else {
    bgMusic.play();
    musicButton.textContent = '🔇';
  }
  isMusicPlaying = !isMusicPlaying;
}
```

## User Guide

### Getting Started

1. Open the application in a modern web browser
2. Click "Start AR Experience"
3. Grant camera permissions when prompted
4. Select a mask using the buttons at the bottom
5. Use the control buttons for additional features

### Controls

- 🔊 Music Toggle: Play/pause background music
- 📸 Photo: Capture current view
- 🔄 Camera: Switch between front and back cameras
- Mask Buttons: Switch between different masks

### Best Practices

1. Ensure good lighting for better face tracking
2. Keep face within camera frame
3. Maintain a stable internet connection
4. Use modern browsers for best performance

## Future Enhancements

### Planned Features

1. Additional Mask Designs

   - More superhero options
   - Custom mask creation
   - Seasonal themes

2. Enhanced Effects

   - Particle effects
   - Sound effects
   - Voice modulation

3. Social Features

   - Share photos
   - Save to gallery
   - Social media integration

4. Performance Optimizations
   - Improved face tracking
   - Better mask rendering
   - Reduced latency

## Conclusion

Spatial Mask demonstrates the potential of web-based AR applications in creating engaging user experiences. The project successfully combines face tracking technology with creative mask designs to provide an interactive and fun platform for users to experience different character masks in real-time.

### Project Impact

- Educational value in AR technology
- Entertainment and engagement
- Showcase of web-based AR capabilities

### Learning Outcomes

- Face tracking implementation
- Canvas-based graphics
- Real-time audio-video processing
- Web AR development

---

_This documentation is part of the Spatial Mask AR project, created for educational purposes._
