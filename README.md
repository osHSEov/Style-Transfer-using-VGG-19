# Neural Style Transfer with PyTorch

This project demonstrates an implementation of Neural Style Transfer (NST) using PyTorch and a pre-trained VGG-19 model.
It allows you to upload a content image and a style image, then generate a new image that combines the content of the first with the artistic style of the second.

Inspired by the original work of Gatys et al. (2016).

# 📖 References

[L. Gatys, A. Ecker and M. Bethge, Image style transfer using convolutional neural networks, CVPR 2016](https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Gatys_Image_Style_Transfer_CVPR_2016_paper.html)

[PyTorch official tutorial on Neural Style Transfer](https://docs.pytorch.org/tutorials/advanced/neural_style_tutorial.html)

# How it works

* Content Representation: Extracted from deeper layers of VGG-19 to preserve the structure and objects.

* Style Representation: Captured via Gram matrices of feature correlations in multiple layers to represent textures and brush strokes.

* Loss Function:

   * Content Loss: Difference between content features of generated and original image.

   * Style Loss: Difference between Gram matrices of generated and style image.

* Optimization: Starting from the content image (or noise), we iteratively update it via gradient descent to minimize the total loss.
