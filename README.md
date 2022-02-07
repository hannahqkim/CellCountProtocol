# CellCountProtocol

**Image Preparation through Adobe Photoshop and Illustrator**

1. Segment the tissue according to how you would like to characterize cell quantity. Segmentation should include excluding any extraneous tissue or artifacts that should not be included in the cell detection process.For example, during our segmentation, we excluded bubbles, retinal pigmented epithelium, and other segments of tissue that we did not wish to characterize cell populations in. We then divided retinal tissue into ten bins so that we could get an idea of cell populations in different regions of the retina. If the tissue has multiple distinct cell layers, segment the tissue by cell layer to ensure you are counting comparable cells (this is relevant when setting the min/max sizes for Laplacian of Blob detection later). We did this by separating the ganglion cell layer, inner nuclear layer, and outer nuclear layer, each of which have cells with different diameters. For this study, we divided and separated the tissue in Adobe Illustrator and Adobe Photoshop using the pen, wand, and lasso tools. 
2. Export the image. First, check exporting preferences in Adobe and make sure that the ‘transparent background’ setting is not selected. Then, click export as png and save the image to a folder or to your desktop.  If you have chosen to segment the tissue, each segmented portion can be exported simultaneously. 

**Accessing the Pipeline**

3. Launch Jupyter Notebook
4. Download the .ipynb file or copy and paste the contents of the file named “Pipeline_StepByStep_H&E” from either Github or Google Colab. Access and open the .ipynb file after launching Jupyter notebook. Google Colab: https://colab.research.google.com/drive/14p_7B5OBNWr_dpE888clOuyoubSd3aha?usp=sharing

**Importing the Image and Running the Pipeline**

5. Find the destination of the image files and write the path name into io.imread(). This loads one image into the pipeline.
6. For the histogram matching step, find an image that has the desired color scheme. Rename it as your reference and add the path name of that image onto the first line of code of the second box.
7. Click the icon “run” on the top panel of the Jupyter Notebook and wait until the first box finishes running. Repeat until you reach the end of the code.
8. Check to ensure that the size of the blobs marked on the last image of the pipeline match the cell sizes well. If not, personalize min blob sizes based on target cell size. This sets a threshold of what the pipeline will call as a cell based on a minimum size. The min can be changed by the min_sigma number on the 2nd line of code of the last box in the pipeline
