# NETWORKWALKS-EMMANUEL-V083-WK3-PASSWORD-CRACKING-ATTACKS-WITH-MULTIPLE-TOOLS

# NETWORKWALKS-EMMANUEL-V083-WK3-PM1-PASSWORD-CRACKING-WITH-JTR

# Password Cracking with JTR

## 📌 Project Overview
This repository documents a password cracking exercise performed against an encrypted PDF file using John the Ripper (JTR) and its graphical front-end, Johnny. The goal is to extract a crackable hash from a password-protected PDF, run a dictionary attack against that hash, and recover the original password used to lock the file.

## 🖥️ Lab Architecture
*   **Attacking Machine:** Windows PC (also compatible with Kali Linux)
*   **Target:** My Locked PDF1.pdf (password-protected PDF, used with permission for training purposes)
*   **Tools Used:** John the Ripper (JTR), Johnny (JTR GUI), OnlineHashCrack PDF Hash Extractor

## 🛠️ Tasks Performed
1. **Download JTR & Johnny** – Downloaded John the Ripper and the Johnny GUI from the official Openwall website.
2. **Install Johnny** – Ran the installer and configured Johnny to point to the `john.exe` executable.
3. **Extract PDF Hash** – Uploaded the locked PDF to the OnlineHashCrack PDF Hash Extractor to generate a `$pdf$...` hash (pdf2john format).
4. **Save Hash File** – Copied the extracted hash into Notepad and saved it as `hash1.txt`.
5. **Load Hash into Johnny** – Opened Johnny, selected "Open password file," and loaded `hash1.txt`.
6. **Run the Attack** – Clicked "Start new attack" and allowed JTR to crack the hash.
7. **Unlock the PDF** – Used the recovered password to open the encrypted PDF file.

## 📊 Key Findings
*   **Hash Format:** PDF hash extracted in `$pdf$...` (pdf2john/hashcat-compatible) format.
*   **Cracking Tool:** John the Ripper successfully cracked the hash using its default wordlist.
*   **Recovered Password:** `password1`
*   **Time to Crack:** Dependent on password complexity and system speed; a simple password cracked quickly.

## 🚀 How to Use This Lab
1. Download John the Ripper and Johnny GUI on a Windows PC (Kali Linux users can skip this step, as JTR is pre-installed).
2. Extract the hash from your target PDF using the [OnlineHashCrack PDF Hash Extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php).
3. Save the hash to a `.txt` file.
4. Open Johnny, configure the path to `john.exe`, and load the hash file.
5. Start the attack and wait for the password to be cracked.
6. Use the recovered password to open the PDF.



# NETWORKWALKS-EMMANUEL-V083-WK3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS

# Password Cracking with Networkwalks Tools

## 📌 Project Overview
This repository documents a password cracking exercise performed against an encrypted PDF file using two free, browser-based tools built by Networkwalks: the Hash Calculator and the Password Cracker. The goal is to extract a crackable hash directly in the browser and recover the original password without installing any software.

## 🖥️ Lab Architecture
*   **Attacking Machine:** Windows PC (also compatible with Kali Linux)
*   **Target:** My Locked PDF1.pdf (password-protected PDF, used with permission for training purposes)
*   **Tools Used:** Networkwalks Hash Calculator, Networkwalks Password Cracker

## 🛠️ Tasks Performed
1. **Download Target File** – Downloaded the encrypted PDF (`My Locked PDF1.pdf`) from the lab page.
2. **Open Hash Calculator** – Opened the [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/) in a web browser.
3. **Extract PDF Hash** – Uploaded the locked PDF; the tool parsed it locally and returned a `$pdf$...` crackable hash.
4. **Copy the Hash** – Copied the complete hash value, starting from `$pdf$`.
5. **Open Password Cracker** – Opened the [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/) in a web browser.
6. **Run the Attack** – Pasted the hash and clicked "Start Cracking," using the built-in wordlist.
7. **Unlock the PDF** – Used the recovered password to open the encrypted PDF file.

## 📊 Key Findings
*   **Hash Format:** PDF hash extracted in `$pdf$...` format, computed locally in-browser with no file uploaded to a server.
*   **Cracking Tool:** Networkwalks Password Cracker successfully matched the hash using its built-in 100-password dictionary.
*   **Recovered Password:** `password1`
*   **Time to Crack:** Match found at 91% progress through the wordlist (91 of 100 attempts).

## 🚀 How to Use This Lab
1. Download the target PDF file to your machine.
2. Open the [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/) and upload the PDF to extract its hash.
3. Copy the full `$pdf$...` hash value.
4. Open the [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/), paste the hash, and click **Start Cracking**.
5. Wait for the tool to display the cracked password.
6. Open the PDF and enter the recovered password to unlock it.

## 📸 Snapshots
*   `Lock_pdf_1_HashCalculate` – Hash Calculator interface with the locked PDF 1 uploaded.
*   `Lock_pdf_2_HashCalculate` – Hash Calculator interface with the locked PDF 2 uploaded.
*   `Lock_pdf_3_HashCalculate` – Hash Calculator interface with the locked PDF 3 uploaded.
*   `Lock_pdf_1_PasswordCrack` – Password Cracker interface with the hash pasted in.
*   `Lock_pdf_2_PasswordCrack` – Password Cracker interface with the hash pasted in.
*   `Lock_pdf_3_PasswordCrack` – Password Cracker interface with the hash pasted in.
*   `Lock_pdf_1_Johnny` – Password Cracking using Johnny.
*   `Lock_pdf_2_Johnny` – Password Cracking using Johnny.
*   `Lock_pdf_3_Johnny` – Password Cracking using Johnny.
*   `Lock_pdf_1_open` – Lock pdf 1 open using the password.
*   `Lock_pdf_2_open` – Lock pdf 2 open using the password.
*   `Lock_pdf_3_open` – Lock pdf 3 open using the password.

## ⚖️ Disclaimer
This lab was performed strictly for educational purposes on a file provided specifically for this training program by Networkwalks Academy. Cracking passwords on files or systems you do not own or have explicit permission to test is illegal.
