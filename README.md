# docbuster.py

## Introduction and Purpose

**docbuster.py** is a user-friendly tool designed to assist in unlocking password-protected PDF and Excel files through brute force or dictionary-based password attempts. Whether you've forgotten a password or need access to locked content for legitimate purposes, this program can help by systematically testing potential passwords.

### What It Does
- Attempts to unlock password-protected PDF and Excel files.
- Supports numeric brute force attacks for passwords of up to 10 digits.
- Offers dictionary-based password attempts using custom text files containing potential passwords.
- Allows easy selection of files and configuration of options via a graphical interface.

This tool is particularly useful for recovering access to documents when the password has been misplaced or forgotten.

---

## Getting Started

### Step 1: Download the Program
1. Navigate to the repository page on GitHub.
2. Click on the green **Code** button, then select **Download ZIP**.
3. Extract the downloaded ZIP file to a folder of your choice on your computer.

### Step 2: Install Required Dependencies
This program relies on Python libraries that need to be installed before running the script. To install these dependencies:
1. Ensure Python (3.8 or later) is installed on your system.
2. Open a terminal or command prompt.
3. Run the following command to install the required libraries:
   ```bash
   pip install msoffcrypto PyPDF2 openpyxl tqdm tkinter
   ```

### Step 3: Run the Program
1. Open a terminal or command prompt.
2. Navigate to the folder where the program was extracted.
3. Run the script using the following command:
   ```bash
   python docbuster.py
   ```

---

## Use Cases and Examples

### Example 1: Recovering a Forgotten PDF Password
1. Run the program and select the locked PDF file when prompted.
2. Enter the number of digits you believe the password contains (e.g., 4 for a four-digit PIN).
3. Optionally, select text files containing potential passwords for a dictionary attack.
4. The program will attempt all possible combinations and alert you when the correct password is found.

### Example 2: Unlocking a Protected Excel File
1. Run the program and select the Excel file when prompted.
2. Choose the number of digits for numeric brute force or upload dictionary files for potential password lists.
3. Once the correct password is identified, the program decrypts the file and saves it as a new unlocked version.

### Example 3: Using Custom Dictionary Files
1. Create one or more text files with potential passwords, each password on a new line.
2. Run the program and select your dictionary files when prompted.
3. The program will attempt to unlock the file using the passwords in your text files.

---

## Disclaimers and Updates

- This repository may be updated at any time, potentially rendering parts of this README obsolete. Users are encouraged to check for updates in the repository periodically.
- The README may not always reflect the latest features or changes in the program.
- Ensure that you have proper authorization to access the files you attempt to unlock. This tool is intended only for ethical and lawful use.

---

By following these instructions, users of all skill levels can effectively use **docbuster.py** to regain access to their locked files with minimal effort.

