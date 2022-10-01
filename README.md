# AI Art Ressources

Stable diffusion and latent diffusion notebooks. Text2img, img2img, etc...  
:warning: Use at your own risk, this is only a public backup of my experiments.  :warning:

# Notebooks

`Loulou_version_BatchMode_clip_interrogator.ipynb` is a image2text notebook that will return a caption for a given image.  
It can generate prompts using Vit-L14 and approximate a stable_diffusion prompt by brute-forcing on prompt modifier lists (list of styles, artists, mediums, etc..). 

## Stable Diffusion

Notebook to run stable diffusion on a prompt list and save to gDrive. 

### text2image

The most vanilla version provided is: 

`Loulou_version_2_NSFW_OFF_Stable_Diffusion_with_🧨_diffusers.ipynb`  

Roughly the same code to ask for generations of images for a given prompt list. 

### image2image

In the image2image category: 
*  BatchMode runs a single prompt to many images. `Loulou_version_2_BatchMode_image_2_image_using_diffusers.ipynb`
*  UltraBatchMode runs many prompts to many images. `Loulou_version_3_UltraBatchMode_image_2_image_using_diffusers.ipynb`

### Mobile Version

Same stable diffusion notebook optimized for Google Colab mobile version.  
`mobile_version_stable_diffusion.ipynb`  

## Restoration and Upscaling

###  Face Restoration GFP-GAN  
The notebook `Loulou_version_Face_Restore_GFPGAN_inference.ipynb` allows the restoration of faces and backgrounds. 

### Real-ESRGAN
The notebook `Loulou_version_Real_ESRGAN_Sber.ipynb` allows upscaling 2x-8x thanks to Real-ESRGAN. 

### Super-ESRGAN - BatchMode [OLD]
The notebook `Loulou_version_SuperRes_Batch_Mode.ipynb` allows upscaling 2x-8x thanks to Real-ESRGAN. 

### Super-ESRGAN [OLD]
The notebook `Loulou_version_SuperRes_ESRGAN.ipynb` allows upscaling 2x-8x thanks to Real-ESRGAN. 

## Animation and Frame Extraction  
Use `Create_a_gif_from_images.ipynb` to create a GIF from JPG or PNG files.  
Can be optimized (but with a really low final quality) to be 30% lighter thanks to pyGifcycle.  

Use `FFMPEG_conversion_from_PNG_JPG_to_MP4.ipynb` to convert JPG or PNG files to a MP4 video.  

## OLDER Diffusions

### Disco Diffusion 5.4

Light modifications from the original notebook to allow a list of init images as input.  
`Loulou_version_2_Disco_Diffusion_v5_4_[Now_with_Warp].ipynb`

### Latent Diffusion LAION-400M

To generate the init images used in Disco Diffusion. 
`Loulou_version_Latent_Diffusion_LAION_400M_model_text_to_image.ipynb`  