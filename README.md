# Height Fields
- The goal of this is to demonstrate how complex landscapes can be created by interpreting grayscale images, where each pixel's intensity represents the elevation at that point.
- The [Height Field](https://en.wikipedia.org/wiki/Heightmap#:~:text=In%20computer%20graphics%2C%20a%20heightmap,display%20in%203D%20computer%20graphics.) is rendered in real-time, allowing for various interactive visual effects and transformations such as zooming, rotating, and panning across the terrain.

**Note**: The code is not disclosed as it was implemented as a part of CSCI 420 Computer Graphics course at the University of Southern California.

## Technological Stack
`C++ • OpenGL • GLSL`

## Features
- Core features
  ```
  +--------------------------------------------------------------------+
  | Key bindings | Features                                            |
  +--------------------------------------------------------------------+
  | 1            | Point mode (Default mode)                           |
  | 2            | Line mode                                           |
  | 3            | Triangle mode                                       |
  | 4            | Smooth Triangle mode (Averages surrounding pixels)  |
  +--------------------------------------------------------------------+
  ```
- Transformations (MB - Mouse Button, L/R - Left / Right)
  ```
  +-----------------------------------------------------------------------+
  | Key bindings | Features                                               |
  +-----------------------------------------------------------------------+
  | t            | Translate mode                                         |
  | s            | Scale mode                                             |
  | r            | Rotate mode (Default mode)                             |
  | LMB          | Scales/Translates/Rotates (in current mode) in x and y |
  | RMB          | Scales/Translates/Rotates (in current mode) in z       |
  +-----------------------------------------------------------------------+
  ```
- Extras
    - Used `glDrawelements` and `GL_TRIANGLE_STRIP` to render terrain in mode 4 (Smooth Triangle mode)
    - Rendered wireframe over the terrain in mode 3 (Triangle mode).
        - The wireframe is of `black` color so it might not be seen if viewed from distance. Go closer to the terrain to see the wireframe.
    - Used `JetColorMap` for mode 4.
    - Added terrain rotation around it's center.
    - Added `reset` feature to reset the terrain to original transform.
    - Added `Toggle Record` functionality which takes screenshots once the recording is `ON` and automatically stops once 300 screenshots are taken.
    - Automated the filenames for screenshots taken.

  ```
  +----------------------------------------------------------------+
  | Key bindings | Features                                        |
  |----------------------------------------------------------------+
  | m            | Toggles wireframe in only Triangle mode (Key 3) |
  | e            | Resets the terrain to starting transform        |
  | x            | Toggle recording (Auto stops at 300 frames)     |
  +----------------------------------------------------------------+
  ```

## Demo
The application runs at 60 FPS but the below animation is shown at 15 FPS created from recorded screenshots.

https://github.com/user-attachments/assets/3450a9f6-7f3f-430e-8c1b-cf1c6035b97e

## Screenshots
- Image used in the demo:

![Heightmap](https://github.com/user-attachments/assets/d4529fbf-1df4-4bf2-8d6a-7022181926dd)

- Top view of the height field:

<img width="1343" alt="HeightFieldTopView" src="https://github.com/user-attachments/assets/ddca3000-0ace-4318-a844-ec8dcdde618e">





