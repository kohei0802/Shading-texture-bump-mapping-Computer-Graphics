# Rasterization-occlusion-anti-aliasing (computer graphics) 
My solution to Games101 HW3

It takes the 3D model (a cow) and a texture map/bump map to create a high quality rendered image, with different rasterization options provided through command line.

The resulting images are placed on the top directory for you to look at!

The main task
1. Write different shader, e.g. Phong fragment shader with or without texture, bump mapping shader, displacement mapping shader.
2. implement rasterizer::rasterize_triangle() to do draw each triangle by calling the shaders and doing zbuffering & MMSA.
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
