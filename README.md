### Assignment 02

As of right now, the assignment is completed. Some things to note:

* When originally starting this assignment, I looked and saw that the load/write code for HDR images would be from third party code, and assumed it would be easier to handle most of the HDR specific functions and work in the main file instead of altering my PPM object code. This was probably a mistake, and there are a few functions in main that should probably be in ppm. Nonetheless, I tried to make it as modular as possible otherwise.

* Usage is: prog02 input output filetype. I didn't make it very clear the last assignment whether to exclude the file extension or not. In that assignment, the user needed to exclude the file extension, but due to the fact that multiple file formats are being used here, the user must *include* the file extension. filetype is either "ppm" or "hdr", based on what you're loading.

* You can alter gamma settings by hitting left and right on the keyboard to decrease and increase gamma by 0.1, respectively. Default gamma is at 1.0.

* You can toggle the bilinear filter by hitting 'b'.

* For the convolution boundary condition, it is handled by boundary padding through image reflection.

## References

I used https://homepages.inf.ed.ac.uk/rbf/HIPR2/gsmooth.htm for the 5x5 gaussian fliter kernel and http://dev.theomader.com/gaussian-kernel-calculator/ with a sigma of 10(?) for the 21x21, but I ended up not using the 21x21 kernel due to performance overhead.
