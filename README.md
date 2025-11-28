# Project 3 - Computer Vision: Feature Extraction

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📚 Course Information

**Subject:** Fundamentals of Computer Vision  
**Degree:** Artificial Intelligence  
**Year:** 2nd Year  
**University:** Universitat Autònoma de Barcelona (UAB)

## 📝 Project Description

This project focuses on implementing two fundamental feature extraction algorithms in computer vision:

1. **Harris Corner Detector** - An algorithm to identify corner features in images
2. **LoG (Laplacian of Gaussian) Blob Detector** - An algorithm to identify blob features in images at multiple scales

These techniques are essential building blocks for many computer vision applications including object recognition, image matching, and motion tracking.

## 🎯 Objectives

### Harris Corner Detector
- Convert images to grayscale with floating-point precision
- Compute image gradients using Sobel filters
- Construct the local structure matrix M
- Calculate eigenvalues and Harris response R
- Threshold and mark detected corners

### LoG Blob Detector
- Generate scale-normalized Laplacian of Gaussian filters at different scales
- Build a scale-space representation by convolving the image with LoG filters
- Find maxima of squared Laplacian response in scale-space
- Visualize detected blobs with circles corresponding to their scale

## 📁 Project Structure

```
Proyecto-3-Vision-Por-Computador/
├── Project3.ipynb          # Main Jupyter Notebook with implementations
├── images/                 # Test images for the algorithms
│   ├── butterfly.jpg       # Image for blob detection
│   ├── chessboard.jpg      # Chessboard pattern image
│   ├── chessboard_perspective.png
│   ├── lenna.png           # Classic test image for corner detection
│   └── sunflowers.jpg      # Additional test image
├── README.md               # Project documentation
└── LICENSE                 # MIT License
```

## 🔧 Requirements

- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib

### Installation

```bash
pip install opencv-python numpy matplotlib
```

## 🚀 Usage

1. Clone the repository:
```bash
git clone https://github.com/EricPrz/Proyecto-3-Vision-Por-Computador.git
cd Proyecto-3-Vision-Por-Computador
```

2. Open and run the Jupyter Notebook:
```bash
jupyter notebook Project3.ipynb
```

3. Execute the cells to run the Harris Corner Detector and LoG Blob Detector implementations.

## 📊 Grading Breakdown

| Component | Points |
|-----------|--------|
| **Harris Corner Detector** | **50 pts** |
| - Code Implementation | 30 pts |
| - Written Answers | 20 pts |
| **LoG Blob Detector** | **50 pts** |
| - Code Implementation | 30 pts |
| - Written Answers | 20 pts |
| **Total** | **100 pts** |

**Minimum required to pass:** 50 points

⚠️ **Important:** Both tasks (Harris Corner Detector and LoG Blob Detector) must be submitted with code and answers; otherwise, the work will be rejected.

## 📖 Algorithms Overview

### Harris Corner Detector

The Harris corner detector uses the local structure matrix to find points in the image where there are significant intensity changes in multiple directions:

$$M = \begin{bmatrix} I_x^2 & I_x I_y \\ I_x I_y & I_y^2 \end{bmatrix}$$

The Harris response is calculated as:

$$R = \lambda_1 \lambda_2 - k (\lambda_1 + \lambda_2)^2$$

Where $\lambda_1$ and $\lambda_2$ are the eigenvalues of the matrix M, and $k$ is a sensitivity parameter (typically 0.04-0.06).

### LoG Blob Detector

The Laplacian of Gaussian detector identifies blob-like structures by:
1. Creating LoG filters at multiple scales (different σ values)
2. Convolving the image with each filter
3. Finding local maxima in scale-space
4. Matching blob size to the corresponding scale

## 👥 Authors

- **Pablo** - [GitHub Profile](https://github.com/Pablo-H-H/)
- **Eric** - [GitHub Profile](https://github.com/EricPrz)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Computer Vision Course - UAB 2024/2025*
