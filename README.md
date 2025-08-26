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

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

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


# Delete the Image on the Drive E **
<img width="1918" height="1079" alt="Screenshot 2025-08-26 190030" src="https://github.com/user-attachments/assets/5aeccde8-7ec8-40b8-a6c6-be2587dbd46f" />

# Click Extract File on the Autopsy To recover the Deleted File on the Drive E 

<img width="1873" height="1067" alt="Screenshot 2025-08-26 192728" src="https://github.com/user-attachments/assets/35b094d4-f445-42db-be97-314c8fbf403f" />


# The Deleted Picture Is Successfully Recoverd On the Export Folder 

<img width="1919" height="1079" alt="Screenshot 2025-08-22 120312" src="https://github.com/user-attachments/assets/b274a7cd-c211-4656-b582-745795754891" />



## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
