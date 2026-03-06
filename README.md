# Structural-Damage-Segmentation-with-Nested-UNet

I built a full crack detection and structural restoration pipeline. I started with segmentation as a baseline, carefully evaluated class imbalance effects using crack IoU vs mIoU, optimized thresholding and post-processing for thin-structure stability, and integrated LaMa for inpainting to automate structural crack removal. I also analyzed why my UNet++ outperformed a DeepLab baseline reported in the paper.




## Models / Architectures used:
### Nested UNet++
U-Net++, is an advanced deep learning segmentation architecture that improves upon standard U-Net by using nested, dense skip pathways. It bridges the semantic gap between encoder and decoder feature maps, resulting in more accurate, detailed segmentation, usually  for medical images.

[Paper link for Nested UNet](https://arxiv.org/abs/1807.10165)

### Lama (Large Mask Inpainting)
Lama is a specialized model designed to remove objects and "fill in" missing parts of images, particularly when the areas to be fixed are large or complex. Unlike standard tools that might get blurry or messy on big gaps, LaMa is built to handle high-resolution photos and maintain consistent patterns like bricks or windows by using Fast-Fourier Convolutions (FFC).

[Paper link for Lama](https://arxiv.org/abs/2109.07161)




## Data
For training the UNet++, I utilized the CrackSeg9k dataset, which is a comprehensive benchmark and collection of datasets specifically designed for semantic segmentation of cracks in various materials, such as concrete and pavement.
