# Rain Removal in Images: A Comprehensive Evaluation of Classical and Deep Learning Techniques #

Rain removal from images is a challenging computer vision problem that impacts tasks like object detection and autonomous driving. This project evaluates classical (L0 smoothing, dictionary learning) and deep learning (DerainNet CNN) methods on synthetic rain datasets, achieving strong PSNR/SSIM results with DerainNet.
​

**Project Overview**

   This report compares model-driven and data-driven deraining techniques for single-image rain removal (SID). Key methods include guided L0 filters, bilateral filter + sparse dictionary decomposition, and a custom DerainNet encoder-decoder CNN trained on high-frequency detail layers.

​

**Methods Evaluated**
| Technique | PSNR | SSIM |
|-----------|------|------|
| Guided L0 Filter | 22.03| 0.73 |
| DerainNet | 16.50| 0.77 |
| Image Decomposition (Binary/RGB) | ~22dB | ~0.71 |
| Hybrid ( Guassian + Multi-loss) | 13.60 dB | 0.2060 |
​

**Key Contributions**

* Implemented and benchmarked 4+ deraining pipelines with custom PyTorch datasets and processors.
* Explored hybrid approaches but found specialized CNNs more effective.
* Used 80/20 splits on 15K synthetic images for robust eval.
​

**Tech Stack**

* Languages: Python
* Libs: PyTorch, OpenCV, scikit-learn/image, NumPy, skimage
* Models: Custom DerainNet (encoder-decoder), VGG16 perceptual loss
* Metrics: PSNR, SSIM
