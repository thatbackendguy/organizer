# 📁 Image Organizer by Year

A fast, terminal-based tool to organize image files into folders by **year**, using only their **filenames**. Supports `.jpg`, `.png`, `.heic`, and more. Built in Go with concurrency for high performance.

---

## 🚀 Features

- 🔍 Extracts year from image filenames using smart regex patterns
- 🖼️ Supports common image formats: `.jpg`, `.jpeg`, `.png`, `.gif`, `.bmp`, `.tiff`, `.webp`, `.raw`, `.heic`
- ⚡ Uses Go’s goroutines for concurrent processing of files
- 🧪 **Preview mode** to simulate organization before moving files
- 📂 Automatically moves unmatched files to an `Extra/` folder
- 🧠 Skips existing files to prevent overwrites
- 🔒 Fully offline, no dependencies

---

## 📦 Downloads

Grab the latest version for your OS from the [Releases page](https://github.com/thatbackendguy/organizer/releases):

| OS         | Architecture | Download Link                                                  |
|------------|--------------|----------------------------------------------------------------|
| Windows    | x64          | [v1.0-io-win-x64.exe](https://github.com/thatbackendguy/organizer/releases/tag/windows) |
| macOS      | Universal    | [v1.0-io-macos](https://github.com/thatbackendguy/organizer/releases/tag/macos)             |
| Linux      | x64          | [v1.0-io-linux-x64](https://github.com/thatbackendguy/organizer/releases/tag/linux)     |

> ⚠️ Make sure to give execute permission on Unix-like systems:  
> `chmod +x v1.0-io-linux-x64` or `chmod +x v1.0-io-macos`

---

## 🛠️ Usage

1. Place the executable in the folder with your image files.
2. Open a terminal or command prompt in that folder.
3. Run the program:
   ```bash
      ./v1.0-io-linux-x64     # Or the relevant binary for your OS
   ```
4. You will be prompted to:
  * Choose between Preview (1) or Organize (2)
  * Enter a starting year (e.g., 2000)
  * Confirm the operation (for Organize mode)

## 📂 What It Does
* Detects years in filenames using many formats (e.g. IMG_20230404_223211.jpg, 2020-01-01.png, BURST20191212, etc.)
* Organizes images into folders named after the detected years:
  ```text
  2020/
    IMG20201212.jpg
  2021/
    photo20210101.png
  Extra/
    random_image.png
  ```
## 🧪 Example Session
```text
Choose option:
1. Preview organization (recommended first)
2. Organize files
Enter choice (1 or 2): 1

Enter starting year (e.g., 2000, default is 1900): 2010

PREVIEW MODE - Analyzing files in: /Users/Yash/Pictures
==================================================
Looking for years from 2010 to 2025
Found 56 image files

Proposed organization:

2020/ (8 files)
  - IMG20201110_203045.jpg
  - 20201111_family.png
  - IMG_20201112_123000.jpg
  ... and 5 more

2021/ (12 files)
  - trip2021-03-05.jpg
  - IMG_20210306.jpg
  - 2021.03.07.jpg
  ... and 9 more

Extra/ (4 files)
  - unknown1.png
  - image_xyz.jpg
  ... and 2 more
```
## ⚠️ Limitations
1. Only uses filename-based date detection (EXIF support coming soon)
2. Only processes files in the current directory (non-recursive)
3. No undo after organizing

## 📄 License
MIT License © [ThatBackendGuy](https://github.com/thatbackendguy/)
