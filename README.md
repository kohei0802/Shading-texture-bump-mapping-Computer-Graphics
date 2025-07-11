# Rasterizer. Converting 3D model to 2D images with texture and height map support (resulting images available in directory 'Resulting Images')
My solution to Games101 HW3

It takes the 3D model (a cow) and a texture map/bump map to create a high quality rendered image, with different shading options provided through command line.
<img width="700" height="700" alt="output1" src="https://github.com/user-attachments/assets/584c9052-fbf9-4108-a178-7bee9f5dde86" />
<img width="700" height="700" alt="output3" src="https://github.com/user-attachments/assets/abcc0508-b481-440a-bcb5-3eeadc533d2f" />
<img width="700" height="700" alt="output4" src="https://github.com/user-attachments/assets/acc09bee-8bcf-41d9-a536-596de717920a" />
<img width="700" height="700" alt="output5" src="https://github.com/user-attachments/assets/4a12af79-463b-4399-90e6-a375238dc3f6" />
<img width="700" height="700" alt="output2" src="https://github.com/user-attachments/assets/cd2d0228-9ee9-409f-a157-1eeae4152935" />

The main task
1. Write different shader, e.g. Phong fragment shader with or without texture, bump mapping shader, displacement mapping shader.
2. implement rasterizer::rasterize_triangle() to draw each triangle by calling the shaders and doing zbuffering & MSAA.
3. Perspective correct interpolation is done for color, texture, positions, normals for accuracy.

# Build
You need OpenCV and Eigen library locally to build this project. 

If you're on Ubuntu, run 
1. sudo apt install libeigen3-dev
2. sudo apt install libopencv-dev

then, go into ./build/ directory or create one if it's not there, then execute
1. cmake ..
2. make

Different ways to run the build
1. ./Rasterizer output1.png texture
2. ./Rasterizer output2.png normal
3. ./Rasterizer output3.png phong
4. ./Rasterizer output4.png bump
5. ./Rasterizer output5.png displacement

