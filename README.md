# image - Official Wyn Package

Image utilities for Wyn: format detection, buffer math, and metadata helpers.
Pure Wyn, no system dependency. (Decode/encode/resize via C bindings is future
work.)

## Install

```bash
wyn pkg install github.com/wynlang/image
```

## Usage

```wyn
import image

// Format detection from file extension
print(image.image_format("photo.png"))           // png
print(image.image_format("scan.jpeg"))           // jpg
print(image.image_is_supported("photo.bmp"))     // true
print(image.image_is_supported("doc.pdf"))       // false

// Buffer math: RGBA buffer for an 800x600 image
print(image.image_buffer_size(800, 600, 4))      // 1920000

// Format dimensions for display
print(image.image_dimensions_str(1920, 1080))    // 1920x1080
```

## API

| Function | Description |
|----------|-------------|
| `image_format(path)` | Detect format from extension: `png`, `jpg`, `bmp`, `gif`, or `unknown` |
| `image_is_supported(path)` | True if the extension is a known image format |
| `image_buffer_size(width, height, channels)` | Raw pixel buffer size in bytes |
| `image_dimensions_str(w, h)` | Format as `"WxH"`, e.g. `"1920x1080"` |
