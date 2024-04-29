<h1 align="center">Batch Resize Images</h1>

<p align="center">This tool allows you to resize all images in the selected directory using various operations and conditions.</p>

<p align="center">
  <img src="https://github.com/Nenotriple/batch_resize_images/assets/70049990/e63253d7-5185-464e-92ea-fc985f1aa9ce" alt="app_cover">
</p>


## 📝 Usage

Select a directory containing images, adjust the settings and conditions as desired, and run the program by pressing `Resize!`.

> [!NOTE]
> - Supported input filetypes: `JPG` `JPEG` `PNG` `WEBP` `BMP` `TIF` `TIFF`
> - Supported output filetypes: `AUTO` `JPG` `PNG` `WEBP`


## 💡 Settings Explained

- **Resize to:**
  - Resolution: Resize to a specific width and height, ignoring aspect ratio.
  - Percentage: Resize the image on a percent scale.
  - Width: Target the image width and resize it.
  - Height: Target the image height and resize it.
  - Shorter side: Target the shorter side of the image and resize it.
  - Longer side: Target the longer side of the image and resize it.

- **Condition:**
  - Upscale and Downscale: Resize the image to the new dimensions, regardless of whether they're larger or smaller than the original dimensions.
  - Upscale Only: Resize the image if the new dimensions are larger than the original dimensions.
  - Downscale Only: Resize the image if the new dimensions are smaller than the original dimensions.

- **Checkbuttons:**
  - Use Output Folder: When enabled, a new folder will be created in the image directory called 'Resize Output' where images will be saved.
  - Overwrite Files: When disabled, conflicting files will have a `_#` appended to the filename. If enabled, files with the same basename will be overwritten.
  - Save PNG Info: When enabled, this option will automatically save any PNG chunk info to the resized output if saving as PNG. If converting from PNG to another type, then a text file will be created containing the PNG info.

- **Filetype:**
  - Select 'AUTO' to output with the same filetype as the input image. Alternatively, choose a specific filetype to force all images to be saved with the chosen type.

- **Quality:**
  - Used to control the output quality of `JPG` and `WEBP` images. A higher value results in a higher quality output. (Ignored for `PNG`)


# 🚩 Requirements

> [!TIP]
> You don't need to worry about anything if you're using the [portable/executable](https://github.com/Nenotriple/batch_resize_images/releases?q=executable&expanded=true) version.

**Python 3.10+**

You will need `Pillow` and `PyPNG`

 - To install Pillow: `pip install pillow`
 - To install PyPNG: `pip install pypng` 


# 📜 Version History

[v1.05 changes:](https://github.com/Nenotriple/batch_resize_images/releases/tag/v1.05)

  - New:
      - `Save PNG Info`:
        - `PNG chunk info` is now copied to the resized output if the output is also PNG. Only copies PNG textual data like: `tEXt`, `zTXt`, `iTXt`.
        - If converting from PNG to another type, then a text file will be created containing the PNG info.

<br>

  - Fixed:
    - Fixed error where the `Resize!` button would become disabled after clicking it without a directory selected.
    - Fixed issues where selecting `Resize!` without a valid width/height wouldn't return early.
    - Fixed some typos.

<br>

  - Other changes:
    - Dropped `PyPNG` and instead now use `PngInfo` from Pillow.
