# Colorization of Grayscale Images using Autoencoders  

*A deep learning project applying convolutional autoencoders to restore color in grayscale images.*  

---

## Introduction  
This project explores the use of **deep convolutional autoencoders** for **image colorization**.  
The encoder compresses grayscale inputs into lower-dimensional representations, while the decoder reconstructs them into colored images.  
The approach demonstrates how unsupervised feature learning can bring life to black and white photos.  

---

## Dataset  
- **Source**: [Kaggle – Image Colorization using GANs dataset](https://www.kaggle.com/datasets/mykeysid10/image-colorization-using-gans)  
- **Size**: Thousands of paired grayscale and colored images.  
- **Preprocessing**:  
  - Conversion of images into LAB color space.  
  - Resizing and normalization.  
  - Splitting into training/validation sets.  

---

## Methodology  

### Data Preprocessing  
- Extract grayscale (L channel) and color (ab channels).  
- Normalize values to range [-1, 1].  

### Model Architecture  
- **Encoder**: Convolutional + MaxPooling layers to compress grayscale images.  
- **Decoder**: Convolutional + UpSampling layers to reconstruct the color channels.  
- Implemented with **Keras & TensorFlow**.  

### Training  
- Loss function: Mean Squared Error (MSE).  
- Optimizer: Adam.  
- Epochs: Configurable (default = 50).  

---

## Results  

- The autoencoder successfully colorized grayscale inputs into realistic outputs.  
- Qualitative evaluation shows effective reconstruction of natural colors for objects, backgrounds, and faces.  
- Visualization: Side-by-side comparison of grayscale input, ground truth, and colorized output.  

---

## Conclusion  

- Autoencoders can **learn meaningful color mappings** from grayscale inputs.  
- While not perfect (occasional artifacts), results demonstrate the feasibility of **deep learning in image restoration**.  
- Future improvements:  
  - Experimenting with **GANs** for sharper results.  
  - Using **larger datasets** for better generalization.  
  - Exploring **transfer learning** with pretrained CNNs.  

---

## References  
- [Kaggle Dataset – Image Colorization using GANs](https://www.kaggle.com/datasets/mykeysid10/image-colorization-using-gans)  
- Kingma, D. P., & Welling, M. (2013). *Auto-Encoding Variational Bayes*.  
- Chollet, F. (2017). *Deep Learning with Python*.  

