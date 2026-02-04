# Web Media Kit

A simple, client-side web application for processing images directly in your browser. Perfect for creating optimized media assets with background removal, trimming, and cropping capabilities.

## Features

- **Drag & Drop Upload**: Easily upload multiple images at once
- **Background Removal**: Automatically remove white/light backgrounds with adjustable tolerance
- **Auto-Trim**: Automatically crop to content bounds
- **Padding Control**: Add custom padding around processed images
- **Size Optimization**: Compress images to target file sizes (KB)
- **Format Conversion**: Output in PNG, WEBP, or JPEG formats
- **Manual Cropping**: Interactive crop tool powered by CropperJS
- **Real-time Preview**: See processed results instantly
- **Download Ready**: One-click download of optimized images

## Quick Start

1. Download or clone this repository
2. Open `index.html` in any modern web browser
3. Configure your processing settings in the top control bar
4. Drag and drop images onto the upload zone or click to browse
5. Process and download your optimized images

## Configuration Options

### Background Removal
- **Toggle**: Enable/disable automatic white background removal
- **Tolerance**: Adjust sensitivity (1-50) - higher values remove lighter grays

### Auto-Trim
- **Toggle**: Automatically crop to non-transparent content bounds
- **Padding**: Add pixel padding around trimmed images

### Optimization
- **Max Size**: Target file size in KB (minimum 10KB)
- **Format**: Choose output format (PNG, WEBP, JPEG)

## How It Works

The app processes images entirely in your browser using HTML5 Canvas:

1. **Upload**: Images are loaded and displayed
2. **Background Removal**: Pixels above the tolerance threshold are made transparent
3. **Trimming**: Content bounds are detected and cropped
4. **Padding**: Specified padding is added with appropriate background fill
5. **Optimization**: Images are scaled down iteratively until under target size
6. **Output**: Final images are rendered and made available for download

## Browser Support

Works in all modern browsers that support:
- HTML5 Canvas
- File API
- ES6 JavaScript

## Technologies Used

- **HTML5/CSS3**: Modern web standards for layout and styling
- **Vanilla JavaScript**: No frameworks, pure client-side processing
- **CropperJS**: Powerful cropping library for manual edits

## Contributing

This is a simple tool - feel free to fork and enhance! Pull requests welcome.

## License

See [LICENSE](LICENSE) for details.

## Donations

If you find this tool useful, consider supporting development via [DONATIONS.md](DONATIONS.md).

## Author

**Keagan Gilmore**
- GitHub: [@KeaganGilmore](https://github.com/KeaganGilmore)
- Email: keagangilmore@gmail.com
- Discord: keagan2980

## Version

v1.0
