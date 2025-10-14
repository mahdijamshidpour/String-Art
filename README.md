# String Art Generator

This is the exact implementation from the [HalfMonty StringArtGenerator](https://github.com/halfmonty/StringArtGenerator) repository.

## About

Web-based string art generator that creates beautiful string art patterns from uploaded images. This implementation uses OpenCV.js for image processing and runs entirely in the browser.

## Features

- Upload any image to generate string art
- Real-time preview of string art generation
- Adjustable parameters (nail count, string count, etc.)
- Pure client-side implementation (no server required)
- Uses OpenCV.js for advanced image processing

## Running the Application

### Method 1: Python HTTP Server (Recommended)
```bash
cd /Users/arsham1/development/Arsham/Cursor/StringArt/String-Art
python3 -m http.server 8080
```
Then open http://localhost:8080 in your browser.

### Method 2: Any HTTP Server
You can use any HTTP server to serve the files:
- Node.js: `npx http-server -p 8080`
- PHP: `php -S localhost:8080`
- Or any other static file server

## Files

- `index.html` - Main application file with UI and algorithm
- `style.css` - Styling for the interface
- `ndarray.js` - NDArray library for image processing
- `opencv.js` - OpenCV.js library (compiled to WebAssembly)
- `ae300.jpg` - Sample image for testing

## Usage

1. Open the application in your browser
2. Upload an image using the file input
3. Adjust parameters if needed (nail count, string count)
4. Click "Generate" to create string art
5. Watch the real-time generation process
6. Download the result when complete

## Algorithm

This implementation uses an error minimization algorithm:
- Starts with the uploaded image as the target
- Iteratively finds the best line to add that reduces the error
- Uses precalculated line coordinates for speed
- Maintains minimum distance between consecutive pins
- Avoids repetitive patterns by tracking recent pins

## Credits

Based on the work of reddit user /u/kmmeerts and implemented by HalfMonty.
Original repository: https://github.com/halfmonty/StringArtGenerator

## License

MIT License