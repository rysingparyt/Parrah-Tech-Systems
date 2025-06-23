# 🔐 Parrah Cipher v1

**Parrah Cipher v1** is a printable, offline-friendly personal encryption system.  
It helps you encode and decode passwords manually or with a simple Python script—perfect for survivors, students, or anyone needing a low-tech, high-trust backup.

### ✅ Parrah Cipher v1  
A printable personal encryption system designed for offline password safety.  
→ Beginner-friendly, human-readable, survivor-first.

📌 [How to use the cipher »](./parrah-cipher-v1/README.md#how-to-use)

---

## ✨ What It Does

- Shifts every letter **+7 letters** forward (Caesar cipher style)
- Swaps certain characters using a custom table
- Adds a prefix and suffix for visual security
- Leaves numbers untouched (you can scramble if you want)
- Easy to decode by hand or script

---

## 🔧 How to Use It

### ▶️ Encrypt a Password (Manual Steps)

1. **Shift each letter +7** in the alphabet  
   Example: `I → P`, `E → L`, `T → A`

2. **Swap characters using this table:**

| Original | Replace With |
|----------|--------------|
| A        | `@`          |
| E        | `3`          |
| I        | `!`          |
| O        | `0`          |
| S        | `$`          |
| T        | `+`          |

3. **Add prefix and suffix:**  
   - Prefix: `XZ-`  
   - Suffix: `-P7`

🔒 **Example:**
Original: `Identity123`  
→ Shifted: `PKLUAPAF123`  
→ Swapped: `PKLU@P@F123`  
→ Final Encrypted: `XZ-PKLU@P@F123-P7`

---

### 🧠 Decryption Instructions

1. Remove `XZ-` and `-P7`  
2. Reverse the character swaps (`@ → A`, etc.)  
3. Shift each letter **backward by 7**

---

## 🐍 Python Script Version

> Want to automate the cipher? Use this simple Python script:

[📂 `parrah_cipher.py`](./parrah_cipher.py)



# To use:
python parrah_cipher.py


What is Parrah Cipher v1?
A lightweight personal encryption system designed for:
✅ Offline password storage
✅ Basic obfuscation (printable & coded)
✅ Human-friendly decoding
✅ Open-source adaptation and learning

⚙️ How It Works:
Step 1: Caesar Shift

Shift every letter forward by +7 (A → H, B → I, etc.)

Step 2: Character Swap Table

Letter	→	Code
A	→	@
E	→	3
I	→	!
O	→	0
S	→	$
T	→	+

Step 3: Add Prefix + Suffix

Prefix: XZ-

Suffix: -P7
This helps visually separate the encoded content from junk/spam.

🧠 Example:
Original password: Identity123
Encrypted: XZ-PKLU@P@F123-P7
(You can write this down, store it in a notebook, and decode it easily later.)

## Features
- Caesar shift + character swaps
- Printable-friendly output
- Easy to decode by hand


 Why Share This?
Because security shouldn’t be complicated or reserved for experts. I’m building tools I can trust and teach—and I’m hoping others who want to build their digital discipline can fork this and make it their own.

This is also part of a bigger reboot I’m working on: new emails, a new AI project, and a personal mission to build safe, open tools for privacy, AI ethics, and survivor resilience.
