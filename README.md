# 🧠 Piecewise Affine Transformation for Digital Image Processing

## 📌 Overview

This project implements **Piecewise Affine Transformation**, a powerful technique used in **Digital Image Processing (DIP)** to geometrically transform images by dividing them into smaller regions and applying affine transformations individually.

It is especially useful for:

* Image warping
* Image morphing
* Local geometric corrections
* Face alignment and transformation

---

## ⚙️ What is Piecewise Affine Transformation?

Piecewise Affine Transformation divides an image into multiple **triangular regions** and applies an **affine transformation** to each triangle separately.

Unlike global affine transformation, this allows **local control**, making transformations more flexible and accurate.

---

## 🧪 Features of this Project

* Image loading and preprocessing
* Landmark/point selection
* Triangle mesh generation
* Affine transformation per triangle
* Image warping output
* Visualization of intermediate steps

---

## 🗂️ Project Structure

```
piecewise-affine-transformation-for-dip.ipynb   # Main notebook
```

---

## 🚀 How It Works (Pipeline)

1. Load input image
2. Define control points (source & destination)
3. Perform Delaunay triangulation
4. Compute affine transform for each triangle
5. Warp each triangle
6. Combine results into final image

---

## 🛠️ Technologies Used

* Python 🐍
* NumPy
* OpenCV
* Matplotlib
* SciPy (for triangulation)

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/piecewise-affine-transformation.git
cd piecewise-affine-transformation
```

2. Install dependencies:

```bash
pip install numpy opencv-python matplotlib scipy
```

3. Run the notebook:

```bash
jupyter notebook
```

---

## 📊 Output

The model produces:

* Transformed image
* Triangle mesh visualization
* Warped intermediate patches

---

## 📚 Use Cases

* Face morphing applications
* Medical image alignment
* Animation and graphics
* Augmented reality

---

## 🔥 Future Improvements

* GUI for interactive point selection
* Real-time transformation
* Integration with deep learning models
* Support for video transformation

---

## 👨‍💻 Author

**Ayon Adhikary**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share with others!
