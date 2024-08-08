# Image Analysis Codes, Python
 These are python version of codes that I wrote to analyze images and videos, that I took via fluorescence, in my research in grad school.



 ~ Codes in this repository ~

 1.) Basic Tiff reader and 'movie' player
 2.) Tiff reader and 'movie' player that subtracts noise





 ~ Description of codes ~

 1.) Basic Tiff reader and 'movie' player: This Python code reads a multi-frame TIFF file, stores the pixel data of each frame in a three-dimensional numpy array named "movie," and then plays the frames as a movie using matplotlib. It handles frames of varying sizes by determining the maximum height and width of all frames, allocating the "movie" array based on these dimensions, and padding (adding pixels with zero intensity) smaller frames to fit. The code uses the tifffile library to read the TIFF file and matplotlib to display the frames sequentially, creating a movie effect.

 2.) This Python code processes each frame of a multi-frame TIFF file by subtracting background noise using the average intensity of non-zero pixels, applying a Gaussian filter to smooth the image and reduce noise, and creating a boolean mask to isolate significant features based on a threshold. The masked image highlights only the important areas of the frame, while the rest is suppressed. The code then plays these processed frames as a continuous movie in a single figure window, ensuring smooth playback and clear visualization of the enhanced features. The purpose of this being to better track a particle via particle tracking methods. In the code, enter your own threshold value to adjust the threshold that noise is eliminated (a greater value will subtract more noise, so play around with it), and bool_ex being set to a value of 1 just plays the movie. Set it to 0 if you don't want the movie to play. The noise subtracted matrix, for each k frame, is saved as the variable 'img'.
