# 📌 Piecewise Affine Transformation for Digital Image Processing

## 📖 Overview

This project implements **Piecewise Affine Transformation (PAT)**, a geometric transformation technique widely used in **digital image processing** for image warping, alignment, and morphing.

Unlike global transformations, piecewise affine works by dividing an image into smaller regions (typically triangles) and applying affine transformations locally, resulting in more flexible and accurate mappings.

---

## 🎯 Objectives

* Implement piecewise affine transformation from scratch
* Perform image warping using control points
* Visualize transformed outputs
* Understand local vs global geometric transformations

---

## 🧠 Concept

Piecewise affine transformation works in three main steps:

1. **Control Point Selection**
   Define corresponding key points between source and target images.

2. **Triangulation**
   Apply Delaunay triangulation to divide the image into triangles.

3. **Local Affine Transformation**
   Each triangle is transformed independently using affine mapping.

---

## ⚙️ Pipeline

```
Input Image
     ↓
Select Control Points
     ↓
Delaunay Triangulation
     ↓
Compute Affine Transform (per triangle)
     ↓
Warp Each Triangle
     ↓
Merge Output Image
```

---

## 🛠️ Technologies Used

* Python 🐍
* NumPy
* OpenCV
* Matplotlib

---

## 📂 Project Structure

```
├── piecewise-affine-transformation.ipynb   # Main implementation notebook
├── images/                                # Input/output images (optional)
├── README.md                              # Project documentation
```

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/piecewise-affine-transformation.git
```

2. Install dependencies:

```bash
pip install numpy opencv-python matplotlib
```

3. Run the notebook:

```bash
jupyter notebook piecewise-affine-transformation.ipynb
```

---

## 📊 Results

* Smooth image warping using local transformations
* Better accuracy compared to global affine transformation
* Useful for face morphing, medical imaging, and object alignment

---

## 📸 Example Use Cases

* Face morphing
* Image registration
* Animation effects
* Medical image alignment

---

## 🔮 Future Work

* Automate control point detection using feature matching
* Extend to real-time video transformation
* Integrate deep learning-based landmark detection
* Optimize performance for large images

---

## 🤝 Contribution

Feel free to fork this repository and submit pull requests for improvements.

---

## 📜 License

This project is for academic and educational purposes.
