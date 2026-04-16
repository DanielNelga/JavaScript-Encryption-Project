# Encryption Cipher Website

A multi-page educational web application that lets users encrypt and decrypt messages using two classic ciphers the **Vigenère Cipher** and the **Atbash Cipher** while also providing informational pages on encryption and cybersecurity.

---

## Pages Overview

| Page | File | Description |
|---|---|---|
| Home | `index.html` | Introduction to encryption and its real-world uses |
| Atbash Cipher | `Atbash.html` | Encrypt/decrypt using the Atbash cipher |
| Vigenère Cipher | `Veginere.html` | Encrypt/decrypt using the Vigenère cipher with a custom key |
| CyberSecurity | `CyberSecurity.html` | Overview of cybersecurity concepts and threats |
| Contact | `Contact.html` | Developer contact information |

---

## Features

- **Vigenère Cipher** — Encrypt and decrypt messages using a custom keyword. The key repeats across the message length, shifting each letter by the corresponding key character value.
- **Atbash Cipher** — Mirrors the alphabet (A↔Z, B↔Y, etc.), working identically for both encryption and decryption.
- **Session Storage** — Your input text, key, and output are saved to `sessionStorage` so they persist during your browser session. Access them via DevTools → Application → Session Storage (or press `F12`).
- **Responsive Navigation** — A consistent 5-button nav bar links all pages together.
- **Educational Content** — Each cipher page includes an explanation of how the cipher works and its advantages/limitations.

---

## Getting Started

No installation or build step required this is a pure HTML/CSS/JavaScript project.

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. Navigate between pages using the top navigation buttons.

---

## How the Ciphers Work

### Vigenère Cipher
Each letter in the plaintext is shifted by the value of the corresponding letter in the keyword (A=0, B=1, ... Z=25). The key repeats if it is shorter than the message. Non alphabetic characters are passed through unchanged.

**Example:**
```
Message:  HELLO
Key:      KEYKE
Output:   RIJVS
```

### Atbash Cipher
The alphabet is reversed every letter maps to its mirror opposite. Since it's symmetric, the same operation both encrypts and decrypts.

**Example:**
```
Message:  HELLO
Output:   SVOOL
```

---

## Technologies Used

- **HTML5**
- **CSS3** (Google Fonts: Lilita One, Do Hyeon, Caveat)
- **Vanilla JavaScript**
- **Browser Session Storage**

---

## Developers

| Name | Email |
|---|---|
| Vladyslav Meinert | G00462913@atu.ie |
| Daniel Nelga | G00464658@atu.ie |
| Oleksandra Odrikovska | G00437332@atu.ie |


---

## Known Limitations

- The Atbash page requires a **page refresh** between encryptions.
- The `decrypt()` function in `Veginere.html` references `encryptedText` instead of `decryptedText` in the `sessionStorage.setItem` call this is a minor bug that can be fixed by updating that variable name.
- The site uses external image URLs which may become unavailable if those sources go offline.

---

## License

This project was built for educational purposes as part of a college module at ATU.
