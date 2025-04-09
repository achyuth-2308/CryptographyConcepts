# 🔐 Cryptography Concepts | Semester 6

Built as part of our **CS3002 - Cryptography Concepts** course, this repository includes fully functional **C implementations** of 15 classic cryptographic algorithms across different categories — from simple monoalphabetic ciphers to complex transpositional systems.

Each algorithm comes with its own set of input/output examples, implementation logic, and is grouped for better understanding. Designed to be **technically informative**, **well-documented**, and **student-friendly**!

---

## 🧠 Table of Contents

- [Categories of Ciphers](#categories-of-ciphers)
  - [1. Monoalphabetic Substitution](#1-monoalphabetic-substitution)
  - [2. Polyalphabetic Substitution](#2-polyalphabetic-substitution)
  - [3. Polygraphic Substitution](#3-polygraphic-substitution)
  - [4. Transpositional Ciphers](#4-transpositional-ciphers)
  - [5. Utility Algorithms](#5-utility-algorithms)
- [🔎 How to Run](#how-to-run)
- [📸 Sample Output Screenshots](#sample-output-screenshots)
- [📚 References](#references)

---

## 📂 Categories of Ciphers

### 1️⃣ Monoalphabetic Substitution
These algorithms replace each plaintext character with a unique ciphertext character.

| No. | Algorithm | Description |
|-----|-----------|-------------|
| 1. | **Atbash Cipher** | A fixed-key cipher that mirrors the alphabet (A ↔ Z, B ↔ Y, ...). |
| 2. | **Caesar Cipher** | Shifts each letter by a fixed number (e.g., +3: A → D). |
| 3. | **August Cipher** | Modified Caesar with a month-based shift. |
| 4. | **Affine Cipher** | Applies a linear function `E(x) = (ax + b) mod m`, with `a` and `b` as keys. |
| 5. | **Multiplicative Cipher** | A special case of affine where only multiplication is used (i.e., `b=0`). |

---

### 2️⃣ Polyalphabetic Substitution
These ciphers use multiple substitution alphabets to obscure frequency analysis.

| No. | Algorithm | Description |
|-----|-----------|-------------|
| 6. | **Vigenère Cipher** | Uses a repeated keyword to shift letters cyclically. |
| 7. | **Gronsfeld Cipher** | Variant of Vigenère using digits instead of letters for the key. |
| 8. | **Beaufort Cipher** | Similar to Vigenère but with reverse encryption logic. |
| 9. | **Autokey Cipher** | Appends plaintext to the key for dynamic shifting. |
| 10. | **Running Key Cipher** | Uses a longer key such as a book passage for encryption. |

---

### 3️⃣ Polygraphic Substitution
These encrypt multiple characters at once, increasing complexity.

| No. | Algorithm | Description |
|-----|-----------|-------------|
| 11. | **N-gram Splitting** | Preprocessing step for splitting plaintext into fixed-length chunks, often used in Hill Cipher. |
| 12. | **Hill Cipher** | Uses matrix multiplication over mod 26 to encrypt blocks of plaintext. Requires invertible key matrices. |

---

### 4️⃣ Transpositional Ciphers
These rearrange the order of characters rather than substituting them.

| No. | Algorithm | Description |
|-----|-----------|-------------|
| 13. | **Rail Fence Cipher** | Zig-zag pattern across rows and then concatenated row-wise. |
| 14. | **Route Cipher** | Fills a grid in a pattern and reads off ciphertext in a specified route. |
| 15. | **Myszkowski Cipher** | A transposition cipher that uses repeated-key digits to determine columnar reordering. |

---

### 5️⃣ Utility Algorithms

- **N-Gram Splitting**: Used for preprocessing in the **Hill Cipher**, this splits text into uniform-length blocks (e.g., digraphs or trigraphs). Essential to maintain matrix size consistency in block ciphers.

---

## 💻 How to Run

To compile and run any algorithm:

```bash
gcc <filename>.c -o <filename>
./<filename>
