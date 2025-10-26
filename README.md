# Elevate-Lab-internship-task3

Below is a sample README file you can use to accompany your documentation for the Nessus Essentials (or OpenVAS) vulnerability assessment project. This README summarizes setup, usage, and report interpretation steps, ensuring clarity for anyone reviewing or repeating the task.

***

# README: Local Vulnerability Assessment using Nessus Essentials

Overview

This project demonstrates how to perform a local vulnerability scan using Nessus Essentials on a Linux machine. The documentation describes each step, from installation to report analysis, and provides suggested mitigations for found vulnerabilities.[1]

 Setup Steps

- Install Nessus Essentials:  
  Download and install Nessus Essentials on your preferred Linux distribution. Start the Nessus service with:
  ```
  sudo systemctl start nessusd
  ```
- Access the Web Interface:  
  Open a browser and connect to `https://localhost:8834` to access the Nessus dashboard.

Scanning Procedure

1. Set Scan Target  
   Specify your local machine’s IP (commonly `127.0.0.1` or `localhost`) as the scan target.
2. Start Vulnerability Scan  
   Use the "Basic Network Scan" template to launch a full scan of your local machine.
3. Wait for Completion  
   Scanning may take 15–60 minutes depending on system resources.
4. Review and Save Results  
   Download or screenshot the results from the Nessus interface for documentation.
Report Summary

- Vulnerability Findings:  
  The scan results detail vulnerabilities categorized as Critical, High, Medium, Low, and Informational.
  - Highlighted Issues:  
  - Self-signed or untrusted SSL certificates  
  - Certificate common name mismatches  
  - Apache `mod_status` information disclosure  
  - Various information disclosure issues in SSH, HTTP, and services
- **Screenshots:**  
  Key findings are supported by screenshots of the Nessus interface, as included in the documentation.[1]

Example Fixes and Mitigations

- **SSL Certificate Issues:**  
  Install a valid certificate issued by a trusted Certificate Authority.
- **Apache `mod_status`:**  
  Restrict access to the status page or disable the module for public exposures.
- **Service Information Disclosure:**  
  Harden configurations, restrict unnecessary information, and limit network exposures.


This README provides an orientation for users to reproduce the scan process, interpret results, and take action based on the documented findings.[1]

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/133020198/9a72036b-0fb9-4a24-9529-bd2e2a12c2b6/task3_documantation.docx)
