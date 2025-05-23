# Camera Calibration using OpenCV

This project demonstrates how to perform **camera calibration** using a set of chessboard images and OpenCV. The goal is to compute the intrinsic camera parameters and distortion coefficients required to correct lens distortion in captured images.

## 🧠 Key Concepts

- **Camera Matrix (Intrinsic Parameters)** – Describes the internal characteristics of the camera (focal length, optical center).
- **Distortion Coefficients** – Parameters that account for lens distortion (radial and tangential).
- **Reprojection Error** – Quantifies the difference between observed image points and projected object points.
- **Chessboard Corners Detection** – Used for calibration by matching 3D world coordinates with 2D image coordinates.

## 📂 Project Structure

## 📸 Input Data

Place your chessboard images inside a folder named `calibration_images`. Each image should contain a clear, visible chessboard taken from different angles.

## ⚙️ Requirements

Install the required packages with pip:

```bash
pip install numpy opencv-python matplotlib scipy

"Camera calibration (Zhang’s method) proceeds in stages: detect chessboard corners, compute per-view homographies, estimate the intrinsic matrix A, extract extrinsics (rotation/translation) for each view, and finally refine all parameters (including lens distortion) by nonlinear optimization. In our fixed pipeline, we ensure shapes are consistent and invalid cases avoided at every step to eliminate mismatches or NaNs. For example, 2D point arrays are managed as (N×2) NumPy arrays, and we carefully handle points with non-positive depth (Z≤0) to avoid division-by-zero."

License: MIT
