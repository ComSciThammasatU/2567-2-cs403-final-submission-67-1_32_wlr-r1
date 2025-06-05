[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/w8H8oomW)

**รหัสโครงงาน:** 67-1_32_wlr-r1

**ชื่อโครงงาน (ไทย):** การพัฒนาเครื่องมือสแกนหาช่องโหว่ของเว็บเซิฟเวอร์แบบอัตโนมัติบนพื้นฐานของเดเบียน

**Project Title (Eng):** การพัฒนาเครื่องมือสแกนหาช่องโหว่ของเว็บเซิฟเวอร์แบบอัตโนมัติบนพื้นฐานของเดเบียน

**อาจารย์ที่ปรึกษาโครงงาน:** ผศ. ดร. วิลาวรรณ รักผกาวงศ์

**ผู้จัดทำโครงงาน:** 
1. นายนพพร ชมภูโคตร  6409680011  nopporn.cho@dome.tu.ac.th
   
---

# VulnScan - Debian-based Automated Web Server Vulnerability Scanner

VulnScan is a Multi-tool, lightweight, and extensible automated vulnerability scanner for websites. It aggregates results from well-known tools like `nmap`, `nikto`, `uniscan`, `wapiti`, `gobuster`, `lbd`, and more to detect common web vulnerabilities with clear categorization, severity scoring, and comprehensive reporting (including HTML and TXT formats).

---

## 🗂 File Structure of the VulnScan Program   

```
 2567-2-cs403-final-submission-67-1_32_wlr-r1/
├── demo
    └── 67-2_CS403_67-1_32_wlr-r1_demo.mp4 # Demonstrating the installation of the tool
├── final_reports
    ├── 67-2_CS403_67-1_32_wlr-r1.pdf # Final report file
    ├── 67-2_CS403_67-1_32_wlr-r1_abstract_en.txt # English abstract file
    └── 67-2_CS403_67-1_32_wlr-r1_abstract_th.txt # Thai abstract file
├── scan_reports/ # Folder containing all scan result outputs
    └── logo.png
├── README.md # Project documentation
└── scanner.py # Main script to perform vulnerability scans
```

---

## 📄 Features

- ✅ Integrates multiple scanning tools in one interface
- ⚖️ Classifies vulnerabilities by severity: Low, Medium, High, Critical
- 📈 Provides rich reports: Summary, Remediation, Charts (HTML)
- ⌛ Shows scan duration and progress animation
- 🚫 Handles tool skips (e.g., via Ctrl+C) and unavailable dependencies
- ⬆️ Auto-updatable using `-U` flag (Git clone)

---

## ⚙️ Installation

### Requirements
- VirtualBox (https://www.virtualbox.org/wiki/Downloads)
- Kali Linux OS Image (https://www.kali.org/get-kali/#kali-installer-images)
- Python 3.6+
- Linux environment (tested on Kali Linux)
- Tools that must be installed beforehand (if not present, the scanner will skip their scans):
  - `nmap`
  - `nikto`
  - `uniscan`
  - `wapiti`
  - `gobuster`
  - `lbd`

---

## ⚡ Usage

### Basic Command
```bash
sudo python3 scanner.py [options]
```

### Options

| Option | Description |
|--------|-------------|
| `-V` or `-v` | Print version information |
| `-U` or `-u` | Replace local files with the latest from GitHub |
| `-H` or `-h` or `-help` | Show help message |
| `target` | DNS name. for an example "gooogle.com" |

---

## 🔹 Example

### Run a full vulnerability scan on a target:
```bash
sudo python3 scanner.py testphp.vulnweb.com
```

### Update the scanner to the latest version from GitHub:
```bash
python3 scanner.py -U
```

### Check the version:
```bash
python3 scanner.py -V
```

---

## 📝 Output

- **Raw Report**: Detailed tool output saved as `.txt`
- **Summary Report**: Organized threat summary with remediation
- **HTML Report**: Colorful interactive report with charts

All reports are saved in the `scan_reports/` folder.

---

## ⚠️ Disclaimer
This tool is designed for educational and authorized security auditing purposes only. Unauthorized use is strictly prohibited.

---

## 🚀 Credits
Developed and maintained by [@parkkung456](https://github.com/parkkung456/VULNscan)


