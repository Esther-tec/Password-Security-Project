# Password-Security-Project
This project demonstrates fundamental cybersecurity concepts including: - Password strength validation - Dictionary-based password attacks - Password hashing using SHA-256  It’s designed as a beginner-friendly project for computer science students venturing into cybersecurity.

## 📌 Table of Contents

- [🔒 What Makes a Strong Password?](#-what-makes-a-strong-password)
- [⚙️ Password Strength Checker](#️-password-strength-checker)
- [🧠 Dictionary Attack Explained](#-dictionary-attack-explained)
- [🔑 Hashed Passwords & SHA-256](#-hashed-passwords--sha-256)
- [📷 Example Output](#-example-output)
- [📂 Project Files](#-project-files)
- [📌 How to Run](#-how-to-run)

- ## 🧠 What Makes a Strong Password?

A **strong password** is hard to guess and resistant to common attacks like:
- **Brute-force**
- **Dictionary attacks**
- **Social engineering**
## 🔑 Characteristics of a Strong Password

| Criteria                 | Reason                                                                 |
|--------------------------|------------------------------------------------------------------------|
| Length ≥ 12 characters   | Longer passwords are harder and take longer to brute-force             |
| Includes Uppercase       | Increases complexity and combinations                                  |
| Includes Lowercase       | Common in natural language; still essential                            |
| Includes Numbers         | Adds numerical diversity; better when mixed                           |
| Includes Special Chars   | Harder to predict (e.g., `@`, `#`, `!`, etc.)                          |

> **Weak Password Example:** `password123`  
> **Strong Password Example:** `G!tM4r$T@h9z`

## 🧪 How the Password Check Function Works

The password checker uses Python to evaluate several criteria:

| Check                    | Python Logic Used                                              |
|--------------------------|----------------------------------------------------------------|
| Minimum Length (8 chars) | `len(password) >= 8`                                           |
| Uppercase Letters        | `any(char.isupper() for char in password)`                    |
| Lowercase Letters        | `any(char.islower() for char in password)`                    |
| Digits (Numbers)         | `any(char.isdigit() for char in password)`                    |
| Special Characters       | `any(char in string.punctuation for char in password)`        |

The result classifies your password as **Weak**, **Moderate**, or **Strong**.

---
## 📂 Dictionary Attack Overview

A **dictionary attack** attempts to crack a password by testing commonly used passwords from a precompiled list. It is simple but very effective.

### 🛠 How It Works:
- Load a list of common passwords from `common_passwords.txt`
- Ask the user to input a password to test
- Loop through each password in the list
- Strip spaces and newlines
- Compare each item with the user’s input
- Print `Success` if a match is found, or `Fail` if no matches exist

- ## 🔒 Hashed Passwords & Dictionary Attacks

A **hashed password** is a version of the password transformed using a one-way function into a fixed-length string.

### 📌 What is Hashing?

Hashing is the process of converting data (like passwords) into a fixed-length string of characters, called a hash value or digest. It uses a **hash function** and has several important properties:

- **Collision Resistance**: It’s computationally infeasible to find two inputs with the same hash
- **Brute Force Impracticality**: Reversing the hash through brute force would take an enormous amount of time
- **Fixed Output Length**: Regardless of input size, the hash has a consistent length
- **One-Way Function**: Hashing cannot be feasibly reversed to retrieve the original input
### 📌 Example:

| Input   | Algorithm | Hash Value                                                                                         | Length |
|---------|-----------|----------------------------------------------------------------------------------------------------|--------|
| `hello` | SHA-256   | `2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824`                                  | 64     |

> In summary, hashing secures passwords by making it practically impossible to recover the original input, even if the hash is exposed.

---

## 📁 Project Components

```plaintext
📁 password-security/
│
├── password_checker.py         # Checks password strength
├── dictionary_attack.py        # Simulates a dictionary-based cracking attempt
├── common_passwords.txt        # Sample password list for testing
├── hashing_demo.py             # Demonstrates password hashing
└── README.md                   # This documentation


This project demonstrates:

What makes a password strong or weak
How to test password strength in Python
How dictionary attacks are conducted
The role of hashing in secure password storage
Password security is essential for protecting personal and system data. Use strong, unique passwords and always follow best practices.
