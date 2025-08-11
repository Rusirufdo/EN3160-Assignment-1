# EN3160 - Image Processing and Machine Vision
## Assignment 1 - Intensity Transformations and Neighborhood Filtering

**Author:** A.A.H. Pramuditha  
**Index No.:** 200476P  
**Course:** EN3160 - Image Processing and Machine Vision

---

## 📝 Overview

This repository contains the implementation of various image processing techniques focusing on intensity transformations and neighborhood filtering. The assignment covers fundamental concepts in digital image processing including histogram manipulation, filtering operations, and image enhancement techniques.

## 🎯 Assignment Objectives

- Implement and analyze various intensity transformation techniques
- Apply neighborhood filtering operations
- Understand histogram equalization and manipulation
- Perform image segmentation and enhancement
- Compare different interpolation methods for image zooming

---

## 📂 Project Structure

```
├── src/
│   ├── question_1_intensity_transformation.py
│   ├── question_2_brain_image_processing.py
│   ├── question_3_gamma_correction.py
│   ├── question_4_vibrance_enhancement.py
│   ├── question_5_histogram_equalization.py
│   ├── question_6_foreground_equalization.py
│   ├── question_7_sobel_filtering.py
│   ├── question_8_image_zooming.py
│   └── question_9_image_segmentation.py
├── data/
│   ├── input_images/
│   └── output_images/
├── docs/
│   └── assignment_report.pdf
└── README.md
```

---

## 🚀 Implemented Techniques

### 1. **Intensity Transformation**
Basic intensity transformation operations to enhance image contrast and brightness.

### 2. **Brain Image Processing** 🧠
- **White Matter Region:** 175 – 255 intensity range
- **Gray Matter Region:** 138 – 180 intensity range
- Linear transformations applied separately to emphasize different tissue types
- Threshold values determined using trial-and-error method

### 3. **Gamma Correction** ✨
- **Optimal Gamma Value:** 0.78
- Applied to L plane for color image enhancement
- Histogram analysis included for visual verification

### 4. **Vibrance Enhancement** 🌈
- **Optimal 'a' Parameter Range:** 0.55 – 0.7
- Intensity transformation for photograph enhancement
- Produces visually pleasing color saturation

### 5. **Histogram Equalization** 📊
- **Custom Implementation:** Manual histogram computation and CDF calculation
- **OpenCV Comparison:** Results compared with `cv.equalizeHist()`
- Intensity mapping to 0-255 range with normalization

### 6. **Selective Histogram Equalization** 🎯
- **Threshold Value:** 160
- Foreground-specific histogram equalization
- Background preservation technique

### 7. **Sobel Filtering** 🔍
- **Custom Sobel Implementation:** Horizontal and vertical gradient computation
- **Kernel Decomposition:** Separable convolution using row and column vectors
- **Gradient Magnitude:** Combined horizontal and vertical gradients
- Utilizes OpenCV's `filter2D()` function with custom kernels

### 8. **Image Zooming** 🔍
Two interpolation methods implemented and compared:

#### (a) Nearest Neighborhood Method
- **SSD Value:** 180,381,523
- Fast computation with pixelated results

#### (b) Bilinear Interpolation Method
- **SSD Value:** 2,031,930,775
- Smoother results with higher computational cost

### 9. **Image Segmentation** 🎨
- **Enhanced Image Creation:** Foreground + Gaussian blurred background
- **Edge Transition Effect:** Gaussian blur creates smooth transitions
- **Visual Enhancement:** Reduced edge distinctness for artistic effect

---

## 🛠️ Requirements

```python
opencv-python>=4.5.0
numpy>=1.20.0
matplotlib>=3.3.0
scipy>=1.7.0
pillow>=8.0.0
```

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/image-processing-assignment.git
cd image-processing-assignment
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Run individual question implementations:
```bash
python src/question_1_intensity_transformation.py
python src/question_2_brain_image_processing.py
# ... and so on
```

---

## 🔧 Usage Examples

### Gamma Correction
```python
from src.question_3_gamma_correction import apply_gamma_correction
corrected_image = apply_gamma_correction(image, gamma=0.78)
```

### Sobel Filtering
```python
from src.question_7_sobel_filtering import sobel_filter
gradient_magnitude = sobel_filter(image)
```

### Image Zooming
```python
from src.question_8_image_zooming import zoom_image
zoomed_nn = zoom_image(image, method='nearest', scale=2)
zoomed_bilinear = zoom_image(image, method='bilinear', scale=2)
```

---

## 📊 Results Summary

| Technique | Key Parameters | Performance Metric |
|-----------|---------------|-------------------|
| Brain Image Processing | White: 175-255, Gray: 138-180 | Visual Enhancement |
| Gamma Correction | γ = 0.78 | Histogram Analysis |
| Vibrance Enhancement | a = 0.55-0.7 | Visual Quality |
| Histogram Equalization | Custom vs OpenCV | Contrast Improvement |
| Sobel Filtering | Horizontal + Vertical | Gradient Magnitude |
| Nearest Neighbor | Fast Processing | SSD: 180,381,523 |
| Bilinear Interpolation | Smooth Results | SSD: 2,031,930,775 |

---

## 📈 Key Insights

1. **Parameter Optimization:** Trial-and-error method proved effective for finding optimal threshold values
2. **Custom vs Built-in:** Custom histogram equalization may yield different results from OpenCV's implementation
3. **Interpolation Trade-offs:** Nearest neighbor offers speed while bilinear provides quality
4. **Segmentation Effects:** Gaussian blur creates natural transition regions in enhanced images
5. **Separable Convolution:** Kernel decomposition improves computational efficiency in Sobel filtering

---

## 📚 Learning Outcomes

- Understanding of fundamental intensity transformation techniques
- Practical implementation of histogram manipulation methods
- Experience with different interpolation algorithms
- Knowledge of edge detection using Sobel operators
- Insight into image segmentation and enhancement strategies

---

## 🤝 Contributing

Feel free to submit issues, create pull requests, or suggest improvements to enhance the implementation.

---

## 📄 License

This project is for academic purposes as part of EN3160 coursework.

---

## 📧 Contact

**Fernando ARD**  
Index No.: 220161N 

---

*This assignment demonstrates practical applications of digital image processing techniques with focus on intensity transformations and neighborhood filtering operations.*
