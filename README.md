# Web Media Kit

A simple, client-side web application for processing images and PDFs directly in your browser. Perfect for creating optimized media assets with background removal, trimming, and cropping, plus a full PDF toolkit for merging, splitting and converting. Nothing is uploaded anywhere.

## Features

### Image Tools

- **Drag & Drop Upload**: Easily upload multiple images at once
- **Background Removal**: Automatically remove white/light backgrounds with adjustable tolerance
- **Auto-Trim**: Automatically crop to content bounds
- **Padding Control**: Add custom padding around processed images
- **Size Optimization**: Compress images to target file sizes (KB)
- **Format Conversion**: Output in PNG, WEBP, or JPEG formats
- **Manual Cropping**: Interactive crop tool powered by CropperJS
- **Real-time Preview**: See processed results instantly
- **Download Ready**: One-click download of optimized images

### PDF Tools
- **One Workspace**: Drop any mix of PDFs and images; every page appears as a thumbnail, colour-coded by source file
- **Adjustable Page Size**: The workspace stretches to wide screens, and a size slider (remembered between visits) enlarges pages, which re-render sharply at any size
- **Select Pages**: Click, shift-click for a range, or type ranges like `1-3, 5, 8-end`
- **Reorder, Rotate, Remove**: Drag pages (or a whole selection) into place, rotate in 90° steps, delete what you don't need
- **Merge**: Combine every page, across all files, into one PDF in the order shown
- **Extract**: Build a new PDF from just the selected pages, then repeat to dice one document into several
- **Split**: One PDF per page, every N pages, or custom groups like `1-3; 4, 6-8; 9-end` (each `;` is a new file)
- **Compress**: *Balanced* and *Strong* re-encode embedded photos and scans (up to 1600px / 70% or 1000px / 50%) while text and vector graphics stay untouched; *Maximum* flattens each page to an image, which suits scans best
- **PDF → Images**: Export pages as PNG, JPEG or WEBP at 72, 150 or 300 DPI
- **PDF → Text**: Extract the text layer to a `.txt` file
- **Images → PDF**: Dropped images become pages, sized to the image, A4 or US Letter
- **Batch Download**: Open or download each result, or grab everything as a ZIP

## Quick Start

1. Download or clone this repository
2. Open `index.html` in any modern web browser
3. Configure your processing settings in the top control bar
4. Drag and drop images onto the upload zone or click to browse
5. Process and download your optimized images

For PDFs, switch to the **PDF Tools** tab (or open `index.html#pdf`), drop your files in, and use the panel on the right.

### Page Ranges

Ranges refer to the numbered badges under each thumbnail, i.e. the current workspace order after any reordering or removals.

| Input | Pages |
|-------|-------|
| `5` | page 5 |
| `1-3` | pages 1, 2, 3 |
| `8-end` or `8-` | page 8 to the last page |
| `-3` | pages 1 to 3 |
| `5-3` | pages 5, 4, 3 (reversed) |
| `1-3, 7` | pages 1, 2, 3, 7 |

Custom split groups use the same syntax, with `;` or a new line separating each output file.

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

PDF tools work the same way, entirely client-side: pdf.js renders thumbnails and image exports, pdf-lib copies pages into new documents (keeping text and vector content intact rather than rasterizing), and JSZip bundles multiple results. These libraries load from cdnjs the first time the PDF tab is opened.

Password-protected or permission-restricted PDFs can be viewed but not rebuilt; remove the protection first.

## Browser Support

Works in all modern browsers that support:
- HTML5 Canvas
- File API
- ES6 JavaScript

## Technologies Used

- **HTML5/CSS3**: Modern web standards for layout and styling
- **Vanilla JavaScript**: No frameworks, pure client-side processing
- **CropperJS**: Powerful cropping library for manual edits
- **pdf.js**: PDF rendering for thumbnails, image export and text extraction
- **pdf-lib**: Creating, merging and splitting PDF documents
- **JSZip**: Bundling multiple outputs into one download

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
