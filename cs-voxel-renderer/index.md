# Custom Voxel Engine & Renderer

### Project Overview
This project challenges you to build a 3D engine from the ground up using a low-level graphics API. Rather than using a pre-built environment, you will develop the systems necessary to manage volumetric data, procedural world generation, and lighting computation.


---

### What You Will Learn

This project provides a deep dive into the "under the hood" mechanics of modern graphics and world-building:

* **Writing Render Code:** You will learn to communicate directly with the GPU, managing **Vertex Buffer Objects (VBOs)** and writing **GLSL/HLSL shaders** to control the final color of every pixel.
* **Understanding Light Physics:** By implementing **Directional Lighting** and **Ambient Occlusion**, you will gain a mathematical intuition for how light interacts with geometry to create a sense of depth and realism.
* **Procedural Terrain Generation:** You will explore how to use **Perlin Noise** or **Simplex Noise** to move beyond random blocks and create natural-looking landscapes, hills, and caves.

* **The Graphics Pipeline:** You will master the transformation of data from simple 3D coordinates into a fully rasterized image, managing world, view, and projection matrices along the way.


---

### The Requirements
* **Platform:** You must use a graphics API such as **OpenGL**, **DirectX**, **Vulkan**, or **Metal**.
* **The "No Engine" Rule:** The use of game engines like **Unity**, **Unreal**, or **Godot** is strictly prohibited. You are responsible for managing your own vertex buffers, shaders, and coordinate transformations.
* **Core Components:**
    1.  **Map Generation:** Implement a procedural algorithm to generate a 3D voxel map.
    2.  **Lighting & Shading:** Write custom shaders to handle **Directional Lighting** and **Ambient Occlusion** (simulating soft shadows in the crevices where blocks meet). Ideally, combining preprocessed and real-time lighting.
    3.  **Face Culling:** Implement logic to identify and discard "internal" faces, ensuring the GPU only renders surfaces visible to the camera.


---

### Key Technical Concepts & Resources

* **Vertex Shading:** Learn how to bake AO values into vertex data to create high-performance "soft" shadows.
* **Procedural Logic:** Watch [The Coding Train: Perlin Noise](https://www.youtube.com/watch?v=8ZEMLC4u9nU) for a primer on generating organic-looking noise.
* **Shadow Theory:** Read up on [0fps - Ambient Occlusion for Voxels](https://0fps.net/2013/07/03/ambient-occlusion-for-minecraft-like-worlds/) to understand the geometric tricks used in voxel rendering.


> **Note on Implementation:** While you may use a math library (like GLM) for matrix operations, the logic for mesh generation, noise implementation, and the shading model must be your own original work.

## Sample Result (uses Java & OpenGL)
<img src="anim.gif" width="600" style="border: 4px solid #ffffff; border-radius: 8px;" alt="Voxel Renderer Animation">