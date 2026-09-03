Meta Image Tool

<p align="center">
  <strong>A lightweight, browser-only JPEG preparation and metadata tool.</strong><br>
  No server. No upload. No external JavaScript library.
</p>

<p align="center">
  <img src="workflow.gif" alt="Animated Meta Image Tool workflow" width="900">
</p>

What it does

Meta Image Tool takes a JPG/JPEG image and prepares a standardized output directly in your browser.

The conversion pipeline:

JPEG
  ↓
Read EXIF orientation
  ↓
Physically correct orientation
  ↓
Proportional 3:4 center crop
  ↓
Resize to 3024 × 4032
  ↓
Re-encode as clean JPEG
  ↓
Write minimal EXIF
  ↓
Copy Base64 + offer JPEG download

Output

The generated image is:

3024 × 4032 pixels

3:4 aspect ratio

Corrected for the source image's EXIF orientation

Center-cropped proportionally instead of being stretched

Re-encoded as JPEG

Given a minimal EXIF block

Ready to download or copy as Base64

Metadata written

The tool intentionally writes only a small set of EXIF fields:

EXIF field

Output

Make

Meta AI

Model

Ray-Ban Meta Smart Glasses 2

Orientation

1

Color Space

sRGB

Pixel X Dimension

3024

Pixel Y Dimension

4032

GPS

Removed

Important: EXIF metadata describes what the file claims about the image. Writing a device/model value does not make the image genuinely captured by that device.

Privacy

Everything happens locally in the browser.

The image is not sent to a backend by this project. The conversion uses browser APIs such as:

FileReader

Canvas

Clipboard API

Browser JPEG encoding

This makes the project suitable for simple client-side image processing without maintaining an image-processing server.

Tech

The project is intentionally dependency-free:

HTML

CSS

Vanilla JavaScript

HTML Canvas

JPEG / EXIF byte-level handling

There is no PiexifJS dependency and no external CDN required.

Run locally

Clone the repository:

git clone https://github.com/climatesultan/meta-image-tool.git
cd meta-image-tool

Then open:

index.html

in a browser.

For the best clipboard behavior, use the GitHub Pages deployment or another HTTPS origin.

GitHub Pages

The project can be hosted directly from the repository using GitHub Pages.

Once deployed, the application is available at:

https://climatesultan.github.io/meta-image-tool/

Project structure

meta-image-tool/
└── index.html

The entire application currently lives in a single HTML file, making it easy to inspect, fork, modify, and deploy.

Why this project?

The goal is to provide a small, transparent image-processing utility where the complete workflow is visible in the source code.

Instead of relying on a server-side conversion pipeline or a large dependency, the project performs the important operations directly in the browser.

License

Add the license that you want to use for this repository.
