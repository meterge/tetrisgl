# TetrisGL - 3D Tetris Game with OpenGL

## Overview

TetrisGL is a 3D Tetris-like game developed in C++ using OpenGL and GLSL shaders.

This project was implemented for the CENG 477 Introduction to Computer Graphics course at Middle East Technical University. The goal of the project was to build a hardware-accelerated 3D game while practicing real-time rendering, shader programming, camera transformations, lighting, collision handling, and basic game logic.

## Features

* 3D Tetris-like gameplay
* 9x9 game board
* Falling 3x3 cube block
* Step-by-step block falling motion
* Block movement relative to the current camera view
* Smooth camera rotation around the game area
* Speed control for the falling block
* Collision handling between blocks and the board
* Prevention of movement outside the game area
* Level collapse when a complete layer is filled
* Score tracking
* Game over detection
* Real-time rendering with OpenGL
* GLSL shader-based lighting
* Ambient, diffuse, and Blinn-Phong shading
* Grid-like visual structure with visible block borders

## Technologies Used

* C++
* OpenGL
* GLSL
* GLFW
* GLEW
* GLM
* Makefile

## Controls

| Key | Action                                            |
| --- | ------------------------------------------------- |
| `A` | Move the block left relative to the current view  |
| `D` | Move the block right relative to the current view |
| `S` | Speed up the falling block                        |
| `W` | Slow down the falling block                       |
| `H` | Rotate the camera/view to the left                |
| `K` | Rotate the camera/view to the right               |

## Build and Run

Clone the repository:

```bash
git clone https://github.com/meterge/tetrisgl.git
cd tetrisgl
```

Compile the project:

```bash
make
```

Run the game:

```bash
./tetrisGL
```

## Project Structure

```text
tetrisgl/
├── main.cpp
├── Makefile
├── vert.glsl
├── frag.glsl
├── vert_text.glsl
├── frag_text.glsl
├── vert2.glsl
├── frag2.glsl
├── tetrisGL_demo.mp4
└── README.md
```

## Demo

A gameplay demo video is included in the repository:

```text
tetrisGL_demo.mp4
```

## Rendering Details

The scene is rendered in real time using OpenGL. The rendering pipeline uses GLSL shaders for vertex transformations and fragment-level lighting calculations.

The lighting model includes:

* Ambient lighting
* Diffuse lighting
* Blinn-Phong specular reflection
* Point light source

The game board and blocks are rendered with a grid-like structure and visible borders to make the 3D layout easier to understand.

## Gameplay Logic

The game starts with a falling 3D block generated from the upper part of the scene. The player can move the block left and right according to the current camera view. By rotating the camera, the player can control the block movement in different directions.

When the falling block reaches the board or lands on another block, it becomes fixed and a new block is generated. If a complete layer is filled, that layer collapses and the blocks above it move down. The score is updated according to the collapsed pieces.

The game ends when a new block cannot be generated because the spawn area is already occupied.

## What I Learned

Through this project, I practiced:

* Developing a real-time 3D graphics application
* Writing GLSL vertex and fragment shaders
* Using OpenGL for rendering
* Applying model, view, and projection transformations
* Implementing camera movement and smooth view rotation
* Handling keyboard input with GLFW
* Implementing basic collision detection
* Managing game objects in a rendering loop
* Applying ambient, diffuse, and Blinn-Phong lighting models

## Notes

This project was developed for educational purposes as part of a computer graphics assignment.
