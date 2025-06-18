# Interpolation from mostly scratch
This repo contains the construction of stable diffusion from its main components of the autoencoder, scheduler, text_embedding, and unet.

After completing this, I decided to explore image interpolation by moving from the latent space of one image to another using linear, cosine, and slerp techniques.

**Please use nbsanity to view my notebook!** [nbsanity.com/melaksenay/link to file.](http://nbsanity.com/melaksenay/interpolation/blob/main/diffusion_to_interpolation.ipynb)


# An explanation:
I think the most important methods in the notebook are **pil_to_latent(input_image)** and **latent_to_pil(latent)** as they describe the encoding and decoding function of the autoencoder used in stable diffusion.

During the process of image generation, we only need to decoding function to retrieve the rgb image after we denoise the latent image, but for the process of interpolation, it is important to be able to encode the pictures we want to interpolate between.


