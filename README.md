# Line Detection by Hough Transform

A Python implementation of the Hough Transform algorithm for line detection in images, built from scratch without using OpenCV's built-in Hough functions.

## Repository Structure
```
Line-Detection-by-Hough-Transform/
├── images/                  # Test images
├── LICENSE
├── Line-Detection-by-Hough-Transform.py    # Main script
├── Line-Detection-by-Hough-Transform.ipynb # Jupyter notebook
└── README.md
```

## Installation
```bash
pip install numpy opencv-python matplotlib
```

## Usage
### Python Script
```bash
python Line-Detection-by-Hough-Transform.py
```

### Jupyter Notebook
```bash
jupyter notebook Line-Detection-by-Hough-Transform.ipynb
```

## 🔧 Parameters

The algorithm accepts the following configurable parameters:

```python
def hough_line_transform(
    image_path, 
    edge_threshold1=400,     # Lower threshold for Canny edge detection
    edge_threshold2=500,     # Upper threshold for Canny edge detection  
    rho_resolution=2,        # Resolution for ρ (distance parameter)
    theta_resolution=2,      # Resolution for θ (angle parameter in degrees)
    threshold=120            # Voting threshold for line detection
)
```

### Parameter Guidelines:
- **Edge Thresholds**: Higher values result in fewer but stronger edges
- **Rho Resolution**: Smaller values increase precision but computational cost
- **Theta Resolution**: Smaller values increase angular precision
- **Threshold**: Higher values detect only prominent lines, lower values detect more lines (including noise)

## Algorithm Overview
1. Image preprocessing and Canny edge detection
2. Hough Transform setup with parameter space
3. Voting process using vectorized computation
4. Line detection through thresholding
5. Visualization of edge map, accumulator space, and detected lines

## Output
The algorithm produces three visualizations for each processed image:
- Edge Map
- Accumulator Space (heatmap)
- Original image with detected lines overlaid in red

## License
MIT License
