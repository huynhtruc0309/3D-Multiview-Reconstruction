# 3D Multiview Reconstruction

This repository implements multiple approaches for 3D reconstruction of a static scene using multi-view images. It explores traditional stereo vision, trifocal methods, and the state-of-the-art deep learning model, DUSt3R.

## 🚀 Project Overview

This project demonstrates three distinct methods for reconstructing 3D point clouds from static images:

- **Stereo Vision**: Depth reconstruction using disparity maps derived from image pairs.
- **Trifocal Method**: Improved depth estimation using three camera viewpoints and template matching techniques.
- **DUSt3R**: A modern deep-learning model that reconstructs depth from images without requiring explicit camera calibration.

## 🛠️ Tools and Technologies

- Python
- OpenCV
- Open3D
- NumPy
- PyTorch (for DUSt3R)
- ChArUco calibration boards

## 📂 Repository Structure

- `calibration.py`: Camera calibration and intrinsic parameter estimation.
- `stereo.py`, `stereo.ipynb`: Stereo reconstruction and disparity map generation.
- `dense.py`: Dense 3D point cloud reconstruction from stereo vision.
- `multiv.py`, `multiview.ipynb`: Trifocal reconstruction using multi-view images and template matching.
- `duster.py`: Implementation of the DUSt3R deep-learning model.
- `visualization.py`: Visualization tools for 3D reconstruction results.
- `utils.py`: Utility functions for data management and preprocessing.

## 💻 How to Use

### Camera Calibration

1. Capture images of the ChArUco calibration board from various angles.
2. Run the calibration script:

```bash
python calibration.py
```
## 🖥️ Stereo Reconstruction

Compute disparity maps from stereo image pairs:

```bash
python stereo.py
```
Generate dense 3D point clouds:

```bash
python dense.py
```

## 📷 Trifocal Reconstruction
Estimate relative poses between three camera views:

```bash
python multiv.py
```
Perform template matching to find point correspondences and reconstruct point clouds.

## 🤖 DUSt3R Reconstruction
Execute the DUSt3R model on single or multiple images:

```bash
python duster.py
```
Evaluate and compare the reconstruction quality.

## 📊 Results & Comparisons

This project highlights the effectiveness and limitations of each reconstruction method:

- **Stereo Vision**:  
  Quick and effective for scenes with minor viewpoint variations. Best suited for structured setups and rapid processing.

- **Trifocal Methods**:  
  Enhanced accuracy by incorporating additional viewpoints. However, precise feature matching is crucial for achieving high-quality results.

- **DUSt3R**:  
  Flexible, robust, and suitable for diverse imaging conditions. This method requires minimal calibration, making it ideal for unstructured scenarios.

For detailed methodology, experiments, and further analysis, please refer to the provided [Report](Report.pdf).


## 📚 Citation
If you find this repository useful, please cite:

bibtex
```bibtex
@misc{huynh2024multiview,
  author = {Dinh Minh NGUYEN, Luong Phuong Truc HUYNH},
  title = {3D reconstruction of a static scene from multi-view},
  year = {2024},
  howpublished = {GitHub repository},
  url = {https://github.com/huynhtruc0309}
}
```
## 📄 License
This project is licensed under the MIT License.
