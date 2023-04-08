# AI Art Resources

A collection of notebooks and resources for AI-generated art, including stable diffusion, latent diffusion, text-to-image, image-to-image, and more. Please note that these are experimental projects, and you should use them at your own risk.

# Notebooks

## Sound

**`wav_concat.ipynb`**: Concatenate wav files into a single wav file. Please ensure that the bitrate matches between files.

## CLIP Interrogation

**`Loulou_version_BatchMode_clip_interrogator.ipynb`**: An image-to-text notebook that generates a caption for a given image. It can create prompts using Vit-L14 and approximate a stable_diffusion prompt by brute-forcing on prompt modifier lists (e.g., list of styles, artists, mediums, etc.).

**`Get_best_matching_male_actor_face_for_a_given_input_picture.ipynb`**: Finds the best match between a male face picture and a list of male actors from the 20th century (9k+ names) using CLIP. It employs fragmentation in small batches to achieve high confidence scores.

**`separate_framed_and_unframed_paintings_using_CLIP.ipynb`**: Sorts paintings into "framed" and "unframed" folders, useful for sorting a large number of paintings generated using the `oil on canvas` or `oil on wood` tokens. The dataset can be found [here](https://github.com/louispaulet/sort_framed_and_unframed_paintings).

## Stable Diffusion

**`Stable_Diffusion_Prompt_List_to_gDrive.ipynb`**: Runs stable diffusion on a prompt list and saves the results to Google Drive.

## Large Resolution Tests

This section contains notebooks for handling output resolutions higher than 512x512 using two techniques:

1. Superscale the image, then split and assemble paintings for a pixel art look.
2. Stitch the images by fusing the edges for a singular image look.

**`Loulou_version_2_BatchMode_image_2_image_using_diffusers.ipynb`**: Use this notebook with method 1 by providing a list of images. The image list should consist of all squares resulting from a large image cut into a grid (done manually in an image editor).

**`GoBig_and_Embiggen_Large_Resolution_Notebooks`**: Notebooks for method 2 will be available soon via GoBig or Embiggen.

## DreamBooth

Notebooks for training and inference on Stable Diffusion 1.4. Train a model checkpoint with a custom dataset (12-20 images) to create new tokens (e.g., `sks man`).

- **`Loulou_version_DreamBooth_Stable_Diffusion.ipynb`**
- **`Loulou_version_Inference_DreamBooth.ipynb`**

The following notebook performs fine-tuning on stable diffusion:
**`Loulou_version_Vast_ai_dreambooth_runpod_joepenna.ipynb`** (requires 24GB VRAM, run on Vast.ai)

Use this notebook to perform inference from a Google Drive checkpoint:
**`MVP_Inference_from_DreamBooth_finetuned_model.ipynb`**

### Text-to-Image

The most basic version provided is:
**`Loulou_version_2_NSFW_OFF_Stable_Diffusion_with_🧨_diffusers.ipynb`**

Use this notebook to generate images for a given prompt list.

### Image-to-Image

In the image-to-image category:

- **`Loulou_version_2_BatchMode_image_2_image_using_diffusers.ipynb`**:
BatchMode runs a single prompt to many images.
- **`Loulou_version_3_UltraBatchMode_image_2_image_using_diffusers.ipynb`**: UltraBatchMode runs many prompts to many images.

### Mobile Version

**`mobile_version_stable_diffusion.ipynb`**: Same stable diffusion notebook optimized for Google Colab mobile version.

## Restoration and Upscaling

### Face Restoration GFP-GAN  
**`Loulou_version_Face_Restore_GFPGAN_inference.ipynb`**: Allows the restoration of faces and backgrounds.

### Real-ESRGAN
**`Loulou_version_Real_ESRGAN_Sber.ipynb`**: Allows upscaling 2x-8x thanks to Real-ESRGAN.

### Super-ESRGAN - BatchMode [OLD]
**`Loulou_version_SuperRes_Batch_Mode.ipynb`**: Allows upscaling 2x-8x thanks to Real-ESRGAN.

### Super-ESRGAN [OLD]
**`Loulou_version_SuperRes_ESRGAN.ipynb`**: Allows upscaling 2x-8x thanks to Real-ESRGAN.

## Animation and Frame Extraction  
**`Create_a_gif_from_images.ipynb`**: Create a GIF from JPG or PNG files. Can be optimized (but with a low final quality) to be 30% lighter thanks to pyGifcycle.

**`FFMPEG_conversion_from_PNG_JPG_to_MP4.ipynb`**: Convert JPG or PNG files to an MP4 video.

## Older Diffusions

### Disco Diffusion 5.4

**`Loulou_version_2_Disco_Diffusion_v5_4_[Now_with_Warp].ipynb`**: Light modifications from the original notebook to allow a list of init images as input.

### Latent Diffusion LAION-400M

**`Loulou_version_Latent_Diffusion_LAION_400M_model_text_to_image.ipynb`**: To generate the init images used in Disco Diffusion.
