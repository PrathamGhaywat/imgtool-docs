# Convert Command

The `convert` command is the primary tool for all image processing tasks.

```bash
.\imgtool.exe convert [input_path] [output_path] [flags]
```

#### Arguments

- `input_path`: The path to the source image or directory.
- `output_path` (optional): The path for the output file or directory. If omitted for a single file, the output will be saved in the same directory with the new format extension.

#### Flags

- `--to <format>`: The target format (`png`, `jpg`, `gif`, `webp`). Default: `png`.
- `--quality <int>`: Image quality for `jpg`/`webp` (1-100). Default: `80`.
- `--resize <string>`: Resize dimensions (e.g., `"800x600"` or `"50%"`).
- `--watermark <path>`: Path to the watermark image.
- `--watermark-opacity <int>`: Watermark opacity (0-100). Default: `100`.
- `--mode <string>`: Processing mode (`single` or `dir`). Default: `single`.
- `--recursive`: Recursively process subdirectories in `dir` mode.
- `--workers <int>`: Number of concurrent workers for `dir` mode. Default: `4`.

### Examples

1.  **Convert a PNG to a high-quality JPG**

    ```bash
    .\imgtool.exe convert input.png output.jpg --to jpg --quality 95
    ```

2.  **Resize an image to 50% of its original size**

    ```bash
    .\imgtool.exe convert big.jpg small.jpg --resize "50%"
    ```

3.  **Apply a watermark to an image**

    ```bash
    .\imgtool.exe convert photo.png watermarked.png --watermark logo.png --watermark-opacity 70
    ```

4.  **Process an entire directory of images**

    This command converts all images in the `input-folder` to `webp` and saves them in `output-folder`.

    ```bash
    .\imgtool.exe convert input-folder output-folder --mode dir --to webp
    ```