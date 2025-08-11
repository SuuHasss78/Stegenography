# 🖼️ BMP Image Steganography in C

This project hides secret data inside a **BMP image** using the **Least Significant Bit (LSB)** technique and retrieves it later.
It supports **encoding** (hiding) and **decoding** (extracting) operations via command line.

## 🚀 Features
- LSB-based image steganography (24-bit BMP)
- Magic string validation for secure decoding
- Stores file extension & size along with data
- Modular C implementation with separate encode/decode modules

## 💻 Usage
```bash
# Compile
gcc main.c encode.c decode.c -o stego

# Encode
./stego -e image.bmp secret.txt output.bmp

# Decode
./stego -d output.bmp decoded.txt
```

## 📖 How It Works
The **Least Significant Bit (LSB)** method changes only the smallest bit in the image’s pixel data.
This change is imperceptible to the human eye but can store secret information efficiently.

## 📂 Project Structure
```
├── main.c              # Handles CLI and calls encoding/decoding modules
├── encode.c / encode.h # Encoding functions
├── decode.c / decode.h # Decoding functions
├── types.h             # Custom data types and status enums
├── README.md           # Project documentation
```
