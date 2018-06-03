# Image-Segmentation

I presume you have downloaded the Massachusetts Road databasedataset from https://www.cs.toronto.edu/~vmnih/data/.  I place my dataset in the directory ~/fastai/data/roads/mass_roads.

The original images in the dataset are 1500x1500.  

### Convert the images to .PNG format.

The files as supplied are in .tiff format.  Use ConvertTIFF2PNG.ipynb to convert all the images to .png

### Step 1: Resize the dataset.

Use Resize-512x512.ipynb to resize the images to 512x512.  No filtering of these images takes place (i.e., I don't check to see if the images will be useful or if they contain rubbish - and some do! Also I didn't worry about the pixels that were missed on the righthand side - 2x512 != 1500.  We can sort this out later if we have time.

### Tile time images

Use Tile-128x128.ipynb to produce resized images of 128X128

### Run the image segmentation notebook and have a play around

Use Roads Detection - Image Segmentation.ipynb.
