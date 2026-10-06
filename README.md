# Part Scanner

A phone web app that works like a barcode scanner for electronic parts: it opens straight into the camera, reads Data Matrix / Code 128 / Code 39 / QR barcodes and printed part numbers, and shows the matching company part number.

- The lookup table is published encrypted (`parts.enc.json`, PBKDF2-SHA256 + AES-256-GCM) and unlocked once per phone with a passphrase; the page holds no readable part numbers.
- Barcodes: @zxing/library. Printed text: Tesseract.js. Both load from jsDelivr.
- Optional: a Claude API key entered in Settings reads hard labels and judges whether a part from another manufacturer is the same physical part. The key stays on the phone.

Install on iPhone: open the site in Safari, Share, Add to Home Screen.
