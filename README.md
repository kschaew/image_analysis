# Image Processing: Color Space Transformation and Flower Segmentation

## Overview

This project demonstrates classical image processing techniques using Python. It consists of two notebooks: the first focuses on RGB-HSV color space transformation, channel-level histogram analysis, Hue-channel histogram equalization, RGB reconstruction, and Gaussian image smoothing. The second focuses on flower image segmentation, object counting, color replacement, and bounding box-based object detection.

The project uses traditional image processing methods rather than deep learning or AI-powered background removal tools. The main goal is to understand how pixel-level transformations, color spaces, thresholding, morphological operations, and connected component analysis can be used to manipulate and analyze images.

## Business Problem / Practical Application

Image processing techniques are widely used in business contexts where visual data needs to be analyzed automatically. For example, flower segmentation and object detection can be applied in retail, inventory monitoring, product quality inspection, and automated visual counting systems. 

Although this project uses flower images as an example, the same techniques can be adapted to other domains where object color, shape, size, and location are important.

## Methods

This project applies classical image processing techniques to analyze, transform, and segment images.

The main methods used in this project are:

- **Color space transformation**: RGB images were converted to HSV to separate color information into Hue, Saturation, and Value channels.
- **Channel-level analysis**: RGB and HSV channels were separated and visualized with intensity histograms to compare their distributions.
- **Histogram equalization**: Histogram equalization was applied to the Hue channel to modify color information and reconstruct new RGB images.
- **Gaussian smoothing**: Gaussian blur was applied with different sigma values to examine the effect of smoothing strength on image appearance and processing time.
- **Color-based segmentation**: HSV-based thresholding was used to segment white flowers and red, orange, and yellow flowers from the background.
- **Morphological processing**: Binary masks were cleaned using operations such as hole filling and mask refinement.
- **Connected component analysis**: Segmented flower regions were labeled to count flowers, estimate object diameters, and extract bounding boxes.
- **Object detection visualization**: Bounding boxes were overlaid on the original flower images to show automatically detected flower regions.

## Results

The generated outputs are stored in the `output/` folder.

| Output File | Description |
|---|---|
| `new_rgb1.jpg` | Reconstructed RGB image created after applying histogram equalization to the Hue channel of the first RGB-HSV image while keeping the original Saturation and Value channels. |
| `new_rgb2.jpg` | Reconstructed RGB image created after applying histogram equalization to the Hue channel of the second RGB-HSV image while keeping the original Saturation and Value channels. |
| `segmented_images_bw.png` | Binary segmentation result for white flowers. Pixels belonging to the segmented white flowers are shown as foreground, while the background is removed. |
| `im1_fandango.jpg` | First flower image where segmented white flowers were recolored to the Fandango shade with RGB values `(181, 51, 138)`. |
| `im2_fandango.jpg` | Second flower image where segmented white flowers were recolored to the Fandango shade with RGB values `(181, 51, 138)`. |
| `segmented_by_color_image1.png` | Segmentation result for red, orange, and yellow flowers in the first flower image. |
| `segmented_by_color_image2.png` | Segmentation result for red, orange, and yellow flowers in the second flower image. |
| `object_detection_image1.png` | First flower image with automatically detected individual red, orange, and yellow flowers shown using bounding box overlays. |
| `object_detection_image2.png` | Second flower image with automatically detected individual red, orange, and yellow flowers shown using bounding box overlays. |

## Tools

This project was implemented in Python using Jupyter Notebook.

Main libraries used:

- **NumPy**: Array manipulation and pixel-level image operations
- **Matplotlib**: Image visualization, subplots, histograms, and result plots
- **scikit-image**: Color space conversion, histogram equalization, Gaussian filtering, segmentation, labeling, and region property extraction
- **SciPy**: Hole filling and additional image processing operations

## Repository Structure

```text
.
├── README.md
├── data/
│   ├── rgbimage1.jpg
│   ├── rgbimage2.jpg
│   └── flower image files
├── notebooks/
│   ├── 01_image_processing_rgb_hsv_smoothing.ipynb
│   └── 02_image_segmentation_object_detection.ipynb
└── output/
    ├── new_rgb1.jpg
    ├── new_rgb2.jpg
    ├── segmented_images_bw.png
    ├── color_filled_image.png
    ├── im1_fandango.jpg
    ├── im2_fandango.jpg
    ├── segmented_by_color_image1.png
    ├── segmented_by_color_image2.png
    ├── object_detection_image1.png
    └── object_detection_image2.png