# Java-3D-Renderer
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/tetrahedron.gif)

## The Java code is a simple 3D graphics renderer using Java Swing. Here's a concise explanation of the code:
### 1. GUI Setup

- Initializes a `JFrame` with sliders for horizontal and vertical rotation.
- Uses a `JPanel` (`renderPanel`) as the main rendering area.
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/wrapper-setup.png)

### 2. `Triangle` and `Vertex` Classes

- `Triangle` class represents a 3D triangle with three vertices and a color.
- `Vertex` class represents a point in 3D space.

### 3. `Matrix3` Class

- Represents a 3x3 matrix with methods for matrix multiplication and vertex transformation.
- We can observe the formulae for rotation matrices in the below image:
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/rotation.png)
- At this point wireframe of our shape is completed and it looks like this(both rotations work and combine together nicely):
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/skeleton.png)



### 4. `Render` Class

- Initializes GUI components and rendering panel.
- Defines `getShade` method for shading colors based on a given shade factor.
- Implements `inflate` method to subdivide triangles, adding detail to the scene.
- Handles the rendering logic, including rotation transformations and hidden surface removal.

### 5. Rendering Logic

- Populates a list of triangles with initial vertices and colors.
- Applies rotation transformations based on slider values.
- Uses a z-buffer for hidden surface removal during rendering.
- Paints each pixel in the rendering panel based on transformed vertices and shading.

### 6. Listeners

- Adds change listeners to sliders to trigger panel repaints when slider values change.

### 7. Main Method

- Initializes the JFrame, sets its size, and makes it visible.
- And the final result is :
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/final.png)


