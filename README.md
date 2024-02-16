# Java-3D-Renderer
![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/tetrahedron.gif)

## This is a simple 3D graphics renderer using Java Swing:
### 1. GUI Setup

- Initializes a `JFrame` with sliders for horizontal and vertical rotation.
- Uses a `JPanel` (`renderPanel`) as the main rendering area.
- The resulting window would be resembling this:  
  
    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/frame1.png)

### 2. `Vertex` , `Triangle` , `Matrix3` Classes

- `Vertex` class represents a point in 3D space.
- `Triangle` class represents a 3D triangle with three vertices and a color.
-  `Matrix3` represents a 3x3 matrix with methods for matrix multiplication and vertex transformation.
-  We can observe the formulae for rotation matrices in the below image:

    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/rotation.png)  
- At this point wireframe of our shape is completed and it looks like this:  
    
    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/frame2.png)  
##### both rotations work and combine together nicely



### 3. `Render` Class

- Initializes GUI components and rendering panel.
- The central panel renders colored triangles in 3D space using BufferedImage for improved performance.
- Triangles are transformed based on the combined horizontal and vertical rotation from sliders.
         
    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/frame3.png)

 ### 4. `Z-Buffer` Implementation 
- Implementing a z-buffer for hidden surface removal during rendering.
- The rendering panel uses a z-buffer for depth calculations, enhancing the visual quality of the 3D object.

### 5. Shading Effect
- Shading is applied to colored triangles based on the angle of incidence`(angleCos)` of light source and normal direction.
- Defining `getShade` method for shading colors based on a given shade factor.
    
    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/frame5.png)



### 6. Tetrahedron to Sphere
- Implementing `inflate` method to subdivide triangles, adding detail to the scene.
- The final result is a dynamic 3D rendering of a sphere that responds to user-controlled rotations.

    ![](https://github.com/NikhilKalloli/Java-3D-Renderer/blob/main/assets/frame6.png)



### 7.Recap

- Populates a list of triangles with initial vertices and colors.
- Applies rotation transformations based on slider values.
- Uses a z-buffer for hidden surface removal during rendering.
- Paints each pixel in the rendering panel based on transformed vertices and shading.




