# image — Official Wyn Package

Load PNG/JPG/BMP images. Wraps stb_image (single-header C library).

## Install

```bash
wyn pkg install github.com/wynlang/image
```

## Usage

```wyn
var img = Image_load("photo.png")
var width = Image_width(img)
var height = Image_height(img)
Image_free(img)
```

No system dependency — stb_image is bundled.
