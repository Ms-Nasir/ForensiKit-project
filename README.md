# ForensiKit — Mobile Device Forensics & Data Recovery

ForensiKit is a web-based mobile device forensics application developed with **Python and Flask** to support digital evidence collection, file analysis, recovery identification, metadata examination, timeline analysis, hashing, and automated forensic reporting.

The application provides a centralized interface for working with extracted or manually uploaded evidence files.

--- 

## Features

- 📱 **ADB Evidence Extraction**
  - Pull files from an Android device using Android Debug Bridge (ADB)
  - Supports a demo mode when ADB is unavailable

- 📂 **Evidence File Upload**
  - Upload multiple forensic evidence files
  - Validates supported file extensions
  - Uses secure filenames before saving evidence

- 🔐 **SHA-256 File Hashing**
  - Generates SHA-256 cryptographic hashes
  - Supports evidence integrity verification

- 🔎 **File Recovery Identification**
  - Identifies hidden files
  - Detects temporary files
  - Detects backup files
  - Identifies files marked as deleted
  - Flags empty/zero-byte files

- 🖼️ **Metadata & EXIF Analysis**
  - Extracts file information
  - Reads image dimensions and format
  - Extracts available EXIF metadata
  - Extracts GPS information when available

- 🕒 **Forensic Timeline**
  - Collects file creation and modification timestamps
  - Sorts evidence chronologically

- 📄 **Automated Forensic Reports**
  - Generates PDF forensic reports
  - Includes case name and investigator information
  - Lists extracted files, sizes, and SHA-256 hashes

- 📁 **Evidence Management**
  - Lists collected evidence files
  - Provides access to generated output files

---

## Technology Stack

- **Python**
- **Flask**
- **HTML5**
- **CSS3**
- **JavaScript**
- **Android Debug Bridge (ADB)**
- **Pillow**
- **ReportLab**
- **SHA-256**

---

## Application Workflow

```text
Android Device / Evidence Files
            ↓
     Evidence Acquisition
       (ADB / Upload)
            ↓
       Output Evidence
            ↓
 ┌──────────┼───────────┐
 ↓          ↓           ↓
Hashing   Metadata   Recovery
 ↓          ↓           ↓
 └──────────┼───────────┘
            ↓
       Timeline Analysis
            ↓
     Forensic PDF Report
```

---

### Installation

**1. Clone the repository**

git clone https://github.com/YOUR-USERNAME/ForensiKit.git
cd ForensiKit

**2. Install Python dependencies**

pip install -r requirements.txt

**3. Android ADB Setup**

For Android device extraction, install Android Debug Bridge (ADB) and ensure the adb command is available from the terminal.

The application can also operate in demo mode when ADB is not installed.

--- 

Running the Application

Start the Flask application:

python app.py

Open:

http://127.0.0.1:5000

--- 

### API Endpoints

| Endpoint        | Purpose                                 |
| --------------- | --------------------------------------- |
| `/`             | Main forensic dashboard                 |
| `/extract`      | Evidence extraction interface           |
| `/upload`       | Evidence upload                         |
| `/hash`         | SHA-256 hashing                         |
| `/metadata`     | Metadata and EXIF analysis              |
| `/recovery`     | Recovery identification                 |
| `/timeline`     | Evidence timeline                       |
| `/report`       | Forensic report interface               |
| `/api/extract`  | Extract files using ADB                 |
| `/api/upload`   | Upload evidence files                   |
| `/api/hash`     | Generate SHA-256 hash                   |
| `/api/metadata` | Extract metadata and GPS information    |
| `/api/recover`  | Identify potentially recoverable files  |
| `/api/timeline` | Generate chronological file information |
| `/api/report`   | Generate PDF forensic report            |

--- 

### Digital Forensics Applications

ForensiKit demonstrates practical concepts used in digital and mobile forensics:

- Evidence acquisition
- Evidence integrity verification
- File examination
- Metadata analysis
- GPS information extraction
- Recovery identification
- Timeline reconstruction
- Automated forensic documentation

--- 

### Limitations

ForensiKit is an educational and research-oriented forensic application.

The recovery module identifies files based on indicators such as hidden names, temporary extensions, backup extensions, deleted markers, and zero-byte files. It does not perform low-level physical storage recovery or reconstruct deleted data from raw device sectors.

ADB extraction also depends on the Android device being accessible through ADB.

--- 

### Future Enhancements

- Android device information collection
- Advanced deleted-file recovery
- SQLite database analysis
- Browser artifact extraction
- Android application artifact analysis
- More forensic image formats
- Advanced case management
- Evidence chain-of-custody tracking
- Expanded automated forensic reporting

--- 


### Project Purpose

This project was developed to demonstrate practical implementation of mobile device forensics, digital evidence handling, file analysis, cryptographic hashing, metadata examination, timeline analysis, and forensic reporting using Python and Flask.

--- 

### Disclaimer

ForensiKit is intended for authorized forensic investigations, education, and research. Only analyze devices and evidence that you are legally authorized to access.
