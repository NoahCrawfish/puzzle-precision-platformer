# Puzzle-Precision Platformer Prototype

A **Unity (C#)** prototype for a precision platformer with puzzle mechanics. You control two characters simultaneously, one red and one blue. Each character can only interact with blocks of their own color, but stepping on a block toggles its color, forcing coordinated movement to clear each level.

All physics was implimented manually, rather than using Unity's built-in physics engine. This allowed for more granular control of the player's movement.

## Implementation Details

- Player Movement & Physics
  - Snappy turnarounds on the ground
  - A stronger "falling gravity" for short-hop support
  - Jump force derived from kinematic equations using target jump height + airtime
  - Velocity Verlet integration for stable movement
  - Coyote time
  - Input buffering
  - Wall sticking & wall jumping

- Custom Collision System
  - Pixel-perfect collision resolution
  - Corner correction to avoid catching edges
  - Helper utilities:
    - Get adjacent tile types
    - Measure distance to a tile type

## Demo

https://user-images.githubusercontent.com/82133480/156235180-b01d4b80-6a6a-427b-9157-7afa55b63764.mov

A playable build of the level is included.

## Controls

- **Red Character:** `WASD`  
- **Blue Character:** Arrow Keys
