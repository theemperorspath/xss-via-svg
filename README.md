# 0days XSS SVG

This repository contains Proof of Concepts (PoCs) for Cross-Site Scripting (XSS) using SVG images. The SVG files demonstrate two attack vectors: a visible popup alert and a blind XSS callback to an out-of-band (OOB) listener.

## Overview

The PoCs illustrate how an attacker can introduce XSS to a web application through SVG files. The included SVG files are designed to be minimal examples for educational purposes and awareness about XSS risks.

## Features

- **SVG Image Carrier:** Blue square SVG images that serve as carriers for XSS payloads.
  
- **PoC 1 - Popup Alert:** The `popup.svg` file contains an embedded script that triggers an alert dialog on load.

- **PoC 2 - Blind XSS Callback:** The `blind.svg` file sends a callback to an OOB listener (webhook.site, Burp Collaborator) for detecting blind XSS vulnerabilities.

## PoC Details

### PoC 1: Popup Alert (popup.svg)
This PoC creates a visible alert box when the SVG is loaded, useful for demonstrating stored or reflected XSS in contexts where you can see the result.

### PoC 2: Blind XSS (blind.svg)
This PoC sends data to an external OOB listener, ideal for scenarios where you cannot directly observe XSS execution (e.g., admin panels, email clients, PDF generators). Replace `YOUR-WEBHOOK-URL` with your actual webhook.site or Burp Collaborator URL.

## Usage

1. **Clone this repository:**
```bash
    git clone https://github.com/theemperorspath/xss-via-svg.git
```

2. **Configure the blind XSS payload:**
   
   Edit `blind.svg` and replace `YOUR-WEBHOOK-URL` with your OOB listener URL (e.g., `https://webhook.site/your-unique-id` or your Burp Collaborator domain).

3. **Upload the SVG files to your target web server:**
   
   After cloning and configuring the repository, upload `popup.svg` or `blind.svg` to the target application. These typically work well for profile pictures, file upload features, or anywhere SVG files are accepted.

## Note

These PoCs are created for educational purposes to demonstrate the potential risks associated with XSS vulnerabilities. Always practice responsible disclosure and obtain proper authorization before conducting security research.

## Disclaimer

These PoCs are provided "as is" without warranty of any kind. Use them responsibly and only in environments where you have explicit permission to test for vulnerabilities.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

## License

These PoCs are released under the [MIT License](LICENSE).
