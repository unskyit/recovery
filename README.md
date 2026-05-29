# 🔓 PDF & ZIP Password Recovery (Web-Based)

A clean, secure, and blazing-fast client-side utility to recover lost passwords for `.pdf` and `.zip` files. 

**No installation, no server uploads, and no command-line hassle.** Everything runs 100% locally in your web browser.

## ✨ Key Features

* **Zero Installation Required:** Just open the HTML file in any modern browser and start recovering.
* **100% Privacy:** Files never leave your device. All processing happens offline using client-side JavaScript Web Workers.
* **RAM-Safe Disk Streaming:** Unlike typical web tools that crash when loading large files, this engine **streams dictionary `.txt` files directly from your hard disk (NOT RAM)**. You can feed it multi-gigabyte wordlists without eating up your system memory.
* **Auto-Decrypt & Save:** Automatically generates and downloads a clean, unencrypted copy of your file the moment the password is found.
* **Local Vault:** Securely logs your successfully recovered passwords in your browser's local storage so you don't lose them again.
* **Dynamic Concurrency:** Automatically scales to use multiple CPU cores (up to 64x parallel processing) for maximum speed.

## 🚀 Performance Benchmarks

Browser-based decryption speed depends heavily on your device's CPU and the encryption standard of the target file. 

* **Mobile Benchmark:** On a **Snapdragon 7+ Gen 2**, this tool reliably achieves **20 to 35 p/s (Passwords per Second)** depending on the file complexity. 
* Desktop processors (especially with 16+ cores) will see significantly higher throughput.

## 🛠️ How to Use

1. Clone or download this repository.
2. Open `index.html` in your web browser (Chrome/Edge/Brave recommended for best Web Worker performance).
3. Select your **Password Dictionary (.txt)** file.
4. Select one or more **Encrypted Targets (.pdf, .zip)**.
5. Click **Start Extraction**.
6. Monitor the real-time HUD and Activity Stream to track speed and progress.

## ⚠️ Disclaimer

This tool is built for **educational purposes and legitimate password recovery only**. You may only use this software on files and systems that you own or have explicit, documented permission to access. The developer assumes no liability for misuse of this software.

## 📜 Libraries Used
* [PDF.js](https://mozilla.github.io/pdf.js/) - Core PDF processing
* [pdf-lib](https://pdf-lib.js.org/) - Document regeneration and saving
* [zip.js](https://gildas-lormeau.github.io/zip.js/) - ZIP archive extraction
