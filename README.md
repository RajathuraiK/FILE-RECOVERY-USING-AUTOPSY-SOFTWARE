# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

<img width="1600" height="934" alt="WhatsApp Image 2026-11-02 at 10 06 35 AM" src="https://github.com/user-attachments/assets/15fea011-3f16-43a0-81b7-b0365f3aa52d" />


<img width="1220" height="746" alt="WhatsApp Image 2026-11-02 at 1 22 51 PM" src="https://github.com/user-attachments/assets/aa08fba4-8f99-4035-8306-40c6df3a2954" />


<img width="1276" height="752" alt="WhatsApp Image 2026-11-02 at 1 23 01 PM" src="https://github.com/user-attachments/assets/899822c1-3ed6-4cc4-9c45-bd368c57ba00" />


<img width="1150" height="755" alt="WhatsApp Image 2026-11-02 at 1 23 23 PM" src="https://github.com/user-attachments/assets/cfdcb27b-89b0-4181-bb11-426a2931afb1" />


### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

<img width="1150" height="755" alt="WhatsApp Image 2026-11-02 at 1 23 23 PM" src="https://github.com/user-attachments/assets/99c31f05-80f1-4da0-bbaf-8da0ebb229a4" />


### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

<img width="1600" height="788" alt="image" src="https://github.com/user-attachments/assets/95f25146-1458-45ac-95a5-ba1282a31a06" />


## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
