# trigonometric-function-visualizer

Compile with `$ g++ source.cpp -std=c++11 -o tfv` and execute with `$ ./tfv`. You'll be prompted for number of graduations (dimension of square aspect output) and number of frames (how many frames to render). Output will be that many .PGM images. Convert with ImageMagick `$ convert -delay 1 anim*.pgm animation.gif`.
