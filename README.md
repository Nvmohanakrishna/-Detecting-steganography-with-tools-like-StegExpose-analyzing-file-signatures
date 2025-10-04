# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
<img width="691" height="538" alt="Screenshot 2025-10-04 111814" src="https://github.com/user-attachments/assets/7827b6b5-17a3-4702-9f5f-ea6f00a61ae9" />
<img width="710" height="569" alt="Screenshot 2025-10-04 111837" src="https://github.com/user-attachments/assets/106b3047-8dbb-49b0-a85d-d1710a7f3f75" />
<img width="679" height="513" alt="Screenshot 2025-10-04 111916" src="https://github.com/user-attachments/assets/f58d092d-1a4d-4bf4-9667-84f35a0f62d8" />
<img width="702" height="502" alt="Screenshot 2025-10-04 111936" src="https://github.com/user-attachments/assets/99cdb060-5993-4673-9ee2-310a7f558eb3" />



List of Images with Steganography Detection Scores and File Signature Details

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
