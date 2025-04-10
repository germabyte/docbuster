# docbuster

## 1. Introduction and Purpose

**docbuster** is a user-friendly desktop application that helps users unlock password-protected PDF and Excel (`.xlsx`) files using two types of attack methods:
- **Numeric Brute-Force Attack**: Systematically tries numeric combinations of a user-defined length.
- **Dictionary Attack**: Tries passwords from one or more text files supplied by the user.

### Purpose & Problem Statement

Users often lose or forget passwords to their own PDF or Excel documents. Re-accessing these files without third-party services can be challenging. `docbuster` solves this issue by enabling users to attempt password recovery in a secure and local environment.

### Value Proposition

- Provides a **graphical interface** to select files and password lists.
- Supports **both brute-force and dictionary-based password recovery**.
- Works **entirely offline** to ensure privacy and data security.
- **No technical skills required** to operate.

---

## 2. Dependencies (Required Software/Libraries)

This program requires Python and several open-source libraries:

| Dependency | Description | Installation |
|------------|-------------|--------------|
| `Python 3.x` | Core programming language used to run the script. | [Download Python](https://www.python.org/downloads/) |
| `msoffcrypto` | Required to open and decrypt password-protected Excel files. | `pip install msoffcrypto-tool` |
| `PyPDF2` | Used to handle and decrypt PDF documents. | `pip install PyPDF2` |
| `openpyxl` | Required to read `.xlsx` files post-decryption. | `pip install openpyxl` |
| `tqdm` | Provides a progress bar during the brute-force attempts. | `pip install tqdm` |
| `tkinter` | Used for GUI elements such as file pickers. | Included with most Python distributions |

---

## 3. Getting Started (Installation & Execution)

### 🔽 Step 1: Download the Repository

1. Click the green **"Code"** button in this repository.
2. Select **"Download ZIP"**.
3. Extract the ZIP file to a folder on your computer.

### ▶️ Step 2: Run the Program

1. Ensure Python is installed (see [above](#2-dependencies-required-softwarelibraries)).
2. Open a **Command Prompt (Windows)** or **Terminal (macOS/Linux)**.
3. Navigate to the extracted folder using the `cd` command:
   ```bash
   cd path/to/extracted/folder
   ```
4. Run the script:
   ```bash
   python docbuster.py
   ```

---

## 4. User Guide (How to Effectively Use the Program)

### 🪄 Step-by-Step Usage

1. **Select a File**: Choose a PDF or Excel (`.xlsx`) file you want to unlock.
2. **Enter Digits**: Specify how many numeric digits the brute-force should try (e.g., 4 for `0000` to `9999`).
3. **(Optional) Add Dictionaries**: Select one or more `.txt` files containing potential passwords (one per line).
4. The program will first attempt numeric brute-force. If unsuccessful, it will try passwords from the selected text files.

### 💡 Notes on Inputs & Outputs

- **Inputs Required**:
  - A password-protected `.pdf` or `.xlsx` file.
  - A number indicating how many digits to try.
  - (Optional) One or more `.txt` files with password lists.

- **Outputs**:
  - If the password is found:
    - PDF: Displays the working password in the terminal.
    - Excel: Decrypts and saves the file as `decrypted_[original_filename].xlsx`.
  - If no password is found: Displays a failure message.

---

## 5. Use Cases and Real-World Examples

### ✅ Use Case 1: Forgotten PDF Password

- **Scenario**: A user forgets the 4-digit numeric password used to secure a financial report in PDF.
- **Action**: Runs `docbuster`, selects the file, and inputs `4` digits.
- **Result**: The program finds the password `0832` and displays it.

### ✅ Use Case 2: Recovering Access to a Locked Excel Sheet

- **Scenario**: A business user needs to access a locked `.xlsx` sales report.
- **Action**: Selects the file and provides a text file of commonly used passwords.
- **Result**: The program finds the matching password from the list and saves a decrypted copy.

### ✅ Use Case 3: Combined Attack

- **Scenario**: A user tries a 6-digit brute-force followed by a dictionary attack.
- **Action**: Selects both methods through the GUI.
- **Result**: Password found during the dictionary phase; file unlocked successfully.

---

## 6. Disclaimer & Important Notices

- This repository and its contents may be updated at any time without notice.  
- Such updates may render parts of this README obsolete.  
- No commitment is made to maintain or update the README to reflect future changes.  
- The provided code is delivered **"as-is"** and **no guarantees** are made regarding functionality, reliability, compatibility, or correctness.
