# Image-Segmentation

I presume you have downloaded the Massachusetts Road databasedataset from https://www.cs.toronto.edu/~vmnih/data/.  I place my dataset in the directory ~/fastai/data/roads/mass_roads.

The original images in the dataset are 1500x1500.  

### Step 1: Convert the images to .PNG format.

The files as supplied are in .tiff format.  Use ConvertTIFF2PNG.ipynb to convert all the images to .png

### Step 2: Resize the dataset.

Use Resize-512x512.ipynb to resize the images to 512x512.  No filtering of these images takes place (i.e., I don't check to see if the images will be useful or if they contain rubbish - and some do! Also I didn't worry about the pixels that were missed on the righthand side - 2x512 != 1500.  We can sort this out later if we have time.

### Step 3: Tile time images

Use Tile-128x128.ipynb to produce resized images of 128X128

### Step 4: Run the image segmentation notebook and have a play around

Use Roads Detection - Image Segmentation.ipynb. This is the basic carvana code.

### Step 5: Run the u-net like code.

Use Roads Detection - unet.ipynb.  This works well up to image sizes 1024x1024, but generates a PyTorch error at 1500x1500.

NOTE: No use of augmentations at this stage.  We just want it to run. The last run was at 97% on 1024x102 images. The best Minh got was 90.06%, the best from U-Net was 90.53 and the best from ResUnet was 91.87%.  Something is working for us here.
