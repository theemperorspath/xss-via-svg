# 🔓 0days XSS SVG

<p align="center">
  <img src="https://img.shields.io/badge/XSS-Proof%20of%20Concept-red?style=for-the-badge&logo=security&logoColor=white" alt="XSS PoC">
  <img src="https://img.shields.io/badge/SVG-Vector%20Exploit-blue?style=for-the-badge&logo=svg&logoColor=white" alt="SVG">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/0days-Security%20Research-orange?style=for-the-badge&logo=hackaday&logoColor=white" alt="0days">
</p>

<p align="center">
  <strong>🎯 Advanced Cross-Site Scripting PoCs via SVG Image Exploitation</strong>
</p>

---

## 📋 Overview

This repository contains **Proof of Concepts (PoCs)** for Cross-Site Scripting (XSS) using SVG images. The SVG files demonstrate two powerful attack vectors: a visible popup alert and a blind XSS callback to an out-of-band (OOB) listener.

> ⚠️ **Educational Purpose Only** - These PoCs illustrate how attackers can introduce XSS to web applications through SVG files.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🖼️ **SVG Image Carrier** | Blue square SVG images that serve as stealthy carriers for XSS payloads |
| 💥 **PoC 1 - Popup Alert** | `popup.svg` triggers an alert dialog on load for immediate XSS verification |
| 🕵️ **PoC 2 - Blind XSS** | `blind.svg` sends callbacks to OOB listeners (webhook.site, Burp Collaborator) |
| 🎨 **Minimal Footprint** | Lightweight payloads designed for maximum compatibility |
| 🔧 **Easy Configuration** | Simple URL replacement for OOB listeners |

---

## 🎯 PoC Details

### 💥 PoC 1: Popup Alert (`popup.svg`)
```
✅ Use Case: Stored or Reflected XSS
✅ Visibility: Immediate visual confirmation
✅ Best For: Testing accessible endpoints
```

This PoC creates a visible alert box when the SVG is loaded, perfect for demonstrating XSS in contexts where you can directly observe the result.

### 🕵️ PoC 2: Blind XSS (`blind.svg`)
```
✅ Use Case: Blind XSS Detection
✅ Visibility: Out-of-band callback to external listener
✅ Best For: Admin panels, email clients, PDF generators, backend systems
```

This PoC sends data to an external OOB listener, ideal for scenarios where you cannot directly observe XSS execution. Replace `YOUR-WEBHOOK-URL` with your actual webhook.site or Burp Collaborator URL.

---

## 🚀 Usage

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/theemperorspath/xss-via-svg.git
cd xss-svg
```

### 2️⃣ Configure Blind XSS Payload

Edit `blind.svg` and replace `YOUR-WEBHOOK-URL` with your OOB listener:
```javascript
// Example webhook URLs:
https://webhook.site/your-unique-id
your-subdomain.burpcollaborator.net
```

### 3️⃣ Upload & Test

Upload `popup.svg` or `blind.svg` to your target web application:

- 📸 Profile pictures
- 📁 File upload features  
- 🎨 Image galleries
- 📝 Content management systems
- ✉️ Email attachments (HTML emails)

---

## 🎓 Attack Vectors
```
🔸 Profile Picture Uploads
🔸 Forum Avatars
🔸 User-Generated Content
🔸 File Sharing Platforms
🔸 CMS Image Libraries
🔸 Email Signature Images
🔸 PDF Generation Endpoints
```

---

## 📝 Note

> 🎓 These PoCs are created for **educational purposes** to demonstrate the potential risks associated with XSS vulnerabilities.  
> 🤝 Always practice **responsible disclosure** and obtain proper authorization before conducting security research.  
> ⚖️ Use these tools only in environments where you have **explicit permission** to test for vulnerabilities.

---

## ⚠️ Disclaimer
```
These PoCs are provided "AS IS" without warranty of any kind.
Use them responsibly and ethically.
Unauthorized access to computer systems is illegal.
The authors are not responsible for misuse of these tools.
```

---

## 🤝 Contributing

Contributions are welcome! 🎉

- 🐛 Found a bug? Open an issue
- 💡 Have an idea? Submit a pull request
- ⭐ Like the project? Give it a star!

---

## 📄 License

This project is released under the [MIT License](LICENSE).

---

<p align="center">
  <sub>Built with 💀 by the 0days team</sub>
</p>

<p align="center">
  <a href="https://github.com/theemperorspath">
    <img src="https://img.shields.io/badge/Follow-@0days-black?style=social&logo=github" alt="Follow">
  </a>
</p>
