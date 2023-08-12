Maximum Intensity Projection and Montage Generation for Microscopy Images

This repository contains a set of scripts for image processing and analysis of microscopy images using the ImageJ software. The code is designed to perform two main tasks: generating maximum intensity projections (MIPs) and creating montages of multi-channel images.

Overview:
Microscopy images often consist of multiple layers, each representing a different focal plane or channel. Maximum intensity projections provide a way to visualize the most intense pixel values across all layers, enhancing the visibility of structures within the image. Additionally, the code can create montages of multi-channel images, which arrange and display the channels in a grid pattern for easier comparison and analysis.

Features:

Maximum Intensity Projection (MIP) Generation:

The code starts by prompting the user to select an input directory containing microscopy image files.
For each image file in the directory, the code opens the image and generates a maximum intensity projection using the "Z Project..." command in ImageJ.
The resulting MIP is saved as a TIFF image in a new directory named "MAX" located alongside the input directory.
After processing all images, the code closes the opened images.
Multi-Channel Montage Generation:

After MIP generation, the code prompts the user to select the "MAX" directory containing the generated MIPs.
For each MIP image in the directory, the code performs the following steps:
Opens the MIP image and splits it into individual channels using the "Split Channels" command.
Merges the channels back together using the "Merge Channels..." command.
Flattens the image to a single layer.
Converts the image to a stack using the "Images to Stack" command.
Generates a montage of the stack with customizable parameters such as columns, rows, scale, and border using the "Make Montage..." command.
Copies the resulting montage image to the system clipboard.
Saves the montage image as a TIFF file in a subdirectory named "Montage" within the "MAX" directory.
Usage:

Install ImageJ on your system.
Place your microscopy images in a directory.
Run the provided scripts in ImageJ's script editor or macro runner.
Follow the prompts to select the input directory and view the processed images.
Note:
This code assumes that you have ImageJ installed and that your microscopy images are in standard image formats such as JPEG, PNG, TIFF, or LIF. Adjustments may be needed based on your specific use case and image formats.

Feel free to customize and extend the code to suit your specific microscopy image processing needs.
