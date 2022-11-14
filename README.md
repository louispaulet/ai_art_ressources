# AI Art Ressources

Stable diffusion and latent diffusion notebooks. Text2img, img2img, etc...  
:warning: Use at your own risk, this is only a public backup of my experiments.  :warning:

# Notebooks

## Clip interrogation

`Loulou_version_BatchMode_clip_interrogator.ipynb` is a image2text notebook that will return a caption for a given image.  
It can generate prompts using Vit-L14 and approximate a stable_diffusion prompt by brute-forcing on prompt modifier lists (list of styles, artists, mediums, etc..). 

`Get_best_matching_male_actor_face_for_a_given_input_picture.ipynb` will find the best match between the picture of a male face and a list of male actors from the 20th century (9k+ names).  
It uses CLIP to find the best matching prompt for a given image out of a list. We use fragmentation in small batches to get high confidence scores.  

`separate_framed_and_unframed_paintings_using_CLIP.ipynb` will sort paintings into "framed" and "unframed" folders.  
Useful to sort a large quantity of paintings generated using the `oil on canvas` or `oil on wood` tokens.  

The dataset is located here:  
https://github.com/louispaulet/sort_framed_and_unframed_paintings  

## Stable Diffusion

Notebook to run stable diffusion on a prompt list and save to gDrive.

## Large_resolution_tests

Contains notebooks that deal with output resolutions higher than 512x512.  
Two techniques:  
1- superscale image then split and assemble paintings for a pixel art look
2- same but stitch the images by fusing the edges for a singular image look 

Method 1 can be accomplished by using the notebook `Loulou_version_2_BatchMode_image_2_image_using_diffusers.ipynb` by supplying a list of images.  
The image list should be all the squares resulting from a large image cut into a grid (done manually in photoshop).  

Method 2 should be soon availiable via either GoBig or Embiggen.  

### GoBig_stable_diffusion

`loulou_version_of_jquesnelle_txt2imghd` is the first try at running txt2imghd in AWS sagemake studio lab. 

`GOBIG_TEST_1_Prog_Rock_Stable.ipynb` is a colab version of Prog Rock Stable  

### InvokeAI_Embiggen 

???

## DREAMBOOTH  

Notebooks for training and inference on Stable Diffusion 1.4.  
Train a model checkpoint with custom (12-20 images) dataset to create new tokens (`sks man`).  

Both these notebooks use the diffusers library to perform Textual Inversion:  
*  `Loulou_version_DreamBooth_Stable_Diffusion.ipynb`  
*  `Loulou_version_Inference_DreamBooth.ipynb`  

The following notebook performs fine-tuning on stable-diffusion:  
`Loulou_version_Vast_ai_dreambooth_runpod_joepenna.ipynb` needs 24go VRAM => Run on Vast.ai  

Use this notebook to perform inference from a GDrive checkpoint:  
`MVP_Inference_from_Dreambooth_finetuned_model.ipynb`  

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