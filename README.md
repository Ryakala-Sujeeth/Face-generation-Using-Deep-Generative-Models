# Face Generation Using Deep Generative Models

## Project Description

This project focuses on generating realistic human face images using a progression of deep generative models. The work systematically explores multiple architectures, starting from basic reconstruction-based models and advancing toward state-of-the-art generative techniques.

The primary objective is to understand how different generative models learn data distributions and how their performance varies in terms of image quality, diversity, and training stability. The models implemented in this project include Autoencoders (AE), Variational Autoencoders (VAE), Generative Adversarial Networks (GAN), Wasserstein GAN (WGAN), and Denoising Diffusion Probabilistic Models (DDPM).

All models are trained on the CelebA dataset, which contains a large number of face images with diverse attributes. The project includes qualitative comparisons of generated images and analysis of training behavior through loss curves.

---

## Objectives

- Understand the progression of generative models from AE to Diffusion Models  
- Compare reconstruction quality and generative capability  
- Analyze training stability across different architectures  
- Generate realistic face images from learned latent representations  

---

## Models Implemented

### Autoencoder (AE)

Autoencoders are used as a baseline model. They learn to reconstruct input images by compressing them into a latent representation and then decoding them back. While they capture overall structure, the generated outputs tend to be blurry and lack diversity.

### Variational Autoencoder (VAE)

VAEs introduce a probabilistic latent space, allowing the model to generate new samples by sampling from a learned distribution. This improves diversity but results in smoother and blurrier images due to latent space regularization.

### Generative Adversarial Network (GAN)

GANs consist of a generator and a discriminator trained in an adversarial setup. The generator learns to produce realistic images, while the discriminator distinguishes real from fake samples. This leads to sharp and realistic outputs but introduces training instability.

### Wasserstein GAN (WGAN)

WGAN improves upon traditional GANs by using the Wasserstein distance as the loss function. This results in more stable training and reduces issues such as mode collapse, leading to more consistent outputs.

### Diffusion Model (DDPM)

Diffusion models generate images by iteratively denoising random noise. They follow a forward process of adding noise and a reverse process of removing it. These models achieve high-quality, realistic outputs with stable training behavior.

---

## Dataset

- **CelebA Dataset**
- Over 200,000 face images with diverse attributes  

### Preprocessing

- Resizing images to 64 × 64 resolution  
- Normalizing pixel values to the range [-1, 1]  

---

## Results

The models were evaluated qualitatively based on generated images and training behavior.

- Autoencoders produce blurry reconstructions with limited diversity  
- VAEs generate more diverse samples but remain blurry  
- GANs produce sharper and more realistic images but are unstable  
- WGAN improves stability and consistency compared to GAN  
- Diffusion models generate the most realistic and detailed images  

---

## Project Structure
```text
├── ae_results.png
├── vae_results.png
├── gan_results.png
├── diffusion_results.png
├── ae_loss.png
├── vae_loss.png
├── gan_loss.png
├── diffusion_loss.png
├── report.pdf
├── face_generation.ipynb
└── README.md
```

## Future Work

- Incorporate quantitative evaluation metrics such as FID  
- Improve efficiency of diffusion models  
- Explore hybrid generative architectures  

---

## Author

R. Sujeeth Kumar  
B.Tech Electrical Engineering  
Indian Institute of Technology Indore  
