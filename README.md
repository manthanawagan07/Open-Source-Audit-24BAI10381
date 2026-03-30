# Open-Source-Audit-24BAI10381
This project presents a detailed study of the Apache HTTP Server, a widely used open-source web server. It combines theoretical concepts, ethical aspects, and practical Linux scripting to understand how open-source software operates in real-world systems.

## Student Information

| Field               | Details              |
| ------------------- | -------------------- |
| Student Name        | Manthan Awagan       |
| Registration Number | 24BAI10381           |
| Course              | Open Source Software |

---

## Project Overview

This project focuses on a detailed study and practical examination of the Apache HTTP Server, one of the most widely used open-source web servers globally. It combines both conceptual understanding and hands-on implementation to explore how such systems function in real environments.

The study covers:

* The origin and evolution of the Apache HTTP Server over time
* Key features and permissions defined by the Apache License 2.0
* The open-source ecosystem and community contributions supporting Apache
* A comparison between Apache and proprietary web server solutions
* Practical implementation through five Bash scripts demonstrating system-level operations

The practical component connects theory with real-world usage by utilizing Linux command-line tools. It includes working with files, monitoring processes, and performing system audits, helping build a deeper understanding of open-source systems in practice.

---

## Tech Stack

| Component        | Details                                          |
| ---------------- | ------------------------------------------------ |
| Operating System | Kali Linux / Ubuntu                              |
| Shell            | Bash (/bin/bash)                                 |
| Web Server       | Apache HTTP Server (apache2)                     |
| Package Manager  | apt                                              |
| Utilities        | uname, whoami, dpkg, du, grep, awk, date, uptime |

---

## Project Structure

```
├── Script1.sh                 # System Identity Report
├── Script2.sh                 # Package Inspector
├── Script3.sh                 # Disk & Permission Audit
├── Script4.sh                 # Log File Analyzer
├── Script5.sh                 # Manifesto Generator
├── Screenshots                # Output images
├── The Open Source Audit      # Main report
└── README.md                  # Project documentation
```

---

## Setup Instructions

### Prerequisites

Ensure you are using a Debian-based Linux distribution such as Ubuntu or Kali Linux.

### Step 1 — Update Packages

```
sudo apt update
```

### Step 2 — Install Apache

```
sudo apt install apache2 -y
```

### Step 3 — Verify Installation

```
apache2 -v
```

### Step 4 — Make Scripts Executable

```
chmod +x Script1.sh Script2.sh Script3.sh Script4.sh Script5.sh
```

---

## Running the Scripts

| Script     | Command                                       |
| ---------- | --------------------------------------------- |
| Script1.sh | ./Script1.sh                                  |
| Script2.sh | ./Script2.sh                                  |
| Script3.sh | ./Script3.sh                                  |
| Script4.sh | ./Script4.sh /var/log/apache2/error.log error |
| Script5.sh | ./Script5.sh                                  |

**Note:** Script4 requires a log file path and a keyword. If no keyword is provided, it searches for “error” by default.

---

## Script Descriptions

* **Script1.sh – System Identity Report**
  Displays system details such as kernel version, logged-in user, OS name, uptime, and current date/time.

* **Script2.sh – Package Inspector**
  Verifies whether Apache is installed using dpkg and displays package details. A case statement prints a short description of the software.

* **Script3.sh – Disk and Permission Auditor**
  Iterates through selected directories and reports their permissions, ownership, and disk usage. It also checks the Apache configuration directory.

* **Script4.sh – Log File Analyzer**
  Reads a log file and counts occurrences of a given keyword. It also displays the last five matching entries.

* **Script5.sh – Manifesto Generator**
  Collects user input and generates a personalized open-source manifesto, which is saved as a text file.

---

## Output Explanation

* **Script1.sh:** Shows formatted system information including OS, kernel, user, uptime, and date.
* **Script2.sh:** Displays installation status and package details of Apache.
* **Script3.sh:** Outputs directory audit results including permissions, ownership, and size.
* **Script4.sh:** Provides keyword count and last matching lines from the log file.
* **Script5.sh:** Creates and displays a personalized manifesto file.

---

## Concepts Used

The scripts demonstrate essential Linux and shell scripting concepts:

* **Variables:** Store and use dynamic values (e.g., $(whoami), $(uname -r))
* **User Input:** Using `read` to accept input from users
* **Conditional Statements:** `if-else` used for decision-making
* **Case Statements:** Handle multiple conditions efficiently
* **Loops:** `for` and `while` used for repetition
* **Command-line Arguments:** Using `$1`, `$2` for flexibility
* **File Handling:** Reading and writing files using redirection
* **Text Processing:** Tools like grep, awk, cut, tail, tr
* **System Commands:** Used to retrieve system information
* **Exit Codes:** Used for error handling
* **Retry Logic:** Improves reliability using delays (`sleep`)

---

## Notes

* These scripts are designed specifically for Linux systems.
* Ensure execution permission is given before running scripts.
* Script4 requires a valid log file (e.g., /var/log/syslog).
* Script3 may require sudo for complete directory access.
* Script5 generates a file named `manifesto_<username>.txt`.

---

## Conclusion

This project uses the Apache HTTP Server as a case study to understand the concept of open-source software and its real-world applications.

The scripting tasks help develop practical Linux administration skills while reflecting core open-source principles such as transparency, collaboration, and adaptability.

By combining theoretical insights with practical implementation, this project provides a well-rounded understanding of how open-source systems operate.

This work is submitted as part of the Open Source Software course requirements.

