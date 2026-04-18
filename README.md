Piecewise Affine Transformation — Digital Image Processing

This repository contains a complete pipeline for performing Piecewise Affine Transformation on digital images. Unlike global affine transformations that apply a single mathematical mapping to an entire image, piecewise affine transformation handles local, non-linear deformations. It achieves this by splitting the image into a triangular mesh (using Delaunay triangulation) and applying a unique affine matrix to each specific triangle.

This is a verified Kaggle notebook implementation, referencing concepts from MDPI Remote Sensing 2019 (DOI:10.3390/rs11192235).

✨ Features

Control Point Generation: Creates a uniform grid of source control points and applies a sine-wave distortion to destination points to simulate a smooth, local deformation.

Delaunay Triangulation: Computes and visualizes the source and destination triangular meshes using scipy.spatial.Delaunay.

Manual Inverse Warping Algorithm: A from-scratch implementation of the transformation calculating per-triangle affine matrices, barycentric point-in-triangle testing, and bilinear interpolation to avoid aliasing artifacts.

Optimized scikit-image Pipeline: Demonstrates a significantly faster, built-in approach using skimage.transform.PiecewiseAffineTransform.

Global Affine Baseline: Compares the piecewise approach against a standard 3-point global affine transformation using OpenCV (cv2.getAffineTransform).

Quantitative Evaluation: Calculates image quality metrics, including Mean Squared Error (MSE) and Structural Similarity Index (SSIM).

Advanced Visualizations: Generates a comprehensive 2x3 comparison figure and transformation interpolation frames to visualize how the deformation builds up gradually.

🛠️ Prerequisites & Installation

The code is written in Python 3. To run this notebook locally, you will need the following libraries:

pip install numpy opencv-python-headless matplotlib scipy scikit-image


(Note: If you are running this on Kaggle, these packages are pre-installed).

🚀 Usage

Simply open the piecewise-affine-transformation.ipynb notebook and run the cells from top to bottom.

By default, the script uses the built-in astronaut image from skimage.data, meaning no external dataset downloads are required. If you want to use your own image, replace the load_image() function in Block 2 with:

image = cv2.imread('path/to/your/image.jpg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)


📊 Pipeline Overview

The notebook is structured into logical, reproducible blocks:

Install & Import Libraries

Load Image: Prepares the 256x256 input image.

Generate Control Points: Maps source grid coordinates to sinusoidally distorted destination coordinates.

Delaunay Triangulation & Mesh Visualization 5. Per-Triangle Affine Matrix Computation: Uses least-squares for numerical stability.

Manual Inverse Warping 7. scikit-image Implementation: The fast pipeline.

Global Affine Transformation: Establishes a fixed baseline using 3 non-collinear interior points.

Evaluation: Computes MSE and SSIM.

Final Comparison Figure: Exports piecewise_affine_results.png.

Transformation Interpolation Frames: Exports interpolation_frames.png showing t=0 to t=1 gradual warping.

📈 Results

The notebook generates local image outputs demonstrating that the piecewise affine method easily handles local deformations better than a single global affine transform, proven by both visual difference maps and structural metrics (lower MSE, higher SSIM).

Generated Output Files:

piecewise_affine_results.png — A 2x3 summary figure showing original, meshes, global vs. piecewise results, and a difference map.

interpolation_frames.png — A 1x6 plot showing the transition of the warp from $t=0.0$ to $t=1.0$.

📚 References

MDPI Remote Sensing 2019: DOI: 10.3390/rs11192235
