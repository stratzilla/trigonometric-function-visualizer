# trigonometric-function-visualizer

Compile with `$ g++ source.cpp -std=c++11 -o tfv` and execute with `$ ./tfv`. You'll be prompted for number of graduations (dimension of square aspect output) and number of frames (how many frames to render). Output will be that many .PGM images. Convert with ImageMagick `$ convert -delay 1 anim*.pgm animation.gif`.

A simple C++ program to visualize trigonometric functions. Along the x and y axes, the boundaries are clamped to `-4..6` and `-12..5` respectively. The z axis is used for animation and is clamped to `0..2*PI`. The program will create an image frame of the function field over the xy plane using a z value of 0, then another using a z value of `2*PI / frames`, where `frames` is the number of frames as user defined, then another frame using a z value of `2 * (2*PI / frames)` and so on up until `frames * (2*PI / frames)` or just `2*PI`. Ultimately, these frames can be packed into a .GIF using ImageMagick.

The function visualized is `(cos(z) * ((0.5)*sin(x) + (0.5)*cos(y)))` but this can be edited by the user.
