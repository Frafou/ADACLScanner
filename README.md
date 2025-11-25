# AD ACL Scanner

[![PowerShell](https://img.shields.io/badge/PowerShell-3.0+-blue.svg)](https://github.com/PowerShell/PowerShell)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-8.1-brightgreen.svg)](https://github.com/canix1/ADACLScanner/releases/latest)

> A comprehensive PowerShell tool for Active Directory Access Control List (ACL) analysis, reporting, and security assessment.

## 📊 Current Version

**Version: 8.1** | **Released: May 16, 2025**

**SHA256:** 202B97106F90FB742000742360219C86E03DA11F7199B9660001AB9DAC0E4BC3

**New Features**

* Added info for Windows 2022 and Windows 2025

![](https://github.com/canix1/ADACLScanner/blob/master/src/ADACLScan7.0_Permission.png)

* From the CLI you can select Target and select RiskyTemplates to scan published certificate templates with "supply in request".
* The default output from CLI is structured and translated
* The default csv file output option is structured and translated and cannot be used for comparing.
* New output option for comparing that is called CSVTEMPLATE from CLI and "CSV Template" in GUI.
* Old CLI output format is produced by using the -RAW switch

## 💾 Download

**[⬇️ Latest Release](https://github.com/canix1/ADACLScanner/releases/latest)**

## ☕ Support Development

If you find this tool valuable, consider supporting its development:

* **PayPal**: [paypal.me/canix1](https://www.paypal.me/canix1)
* **Bitcoin**: `bc1qte7vlwhvrju7msv9hzfytwy7jd9vlmnjfpm0366d62yx4ke89czsavk0hr`

![Bitcoin Donation](https://github.com/canix1/ADACLScanner/blob/master/src/DonateBitCoin.png)

## 📝 Description

AD ACL Scanner is a powerful PowerShell-based tool designed for comprehensive Active Directory security analysis. It provides detailed reports of Access Control Lists (DACLs) and System Access Control Lists (SACLs) with an intuitive GUI interface.

### 🎯 Key Capabilities

* **Complete PowerShell Implementation**: Pure PowerShell solution requiring no additional dependencies
* **GUI-Based Analysis**: User-friendly interface for interactive AD security assessment
* **Comprehensive Reporting**: Detailed HTML, CSV, and Excel report generation
* **Security Assessment**: Identify security risks and permission anomalies

### 📚 Related Resources

* [Forensics - Active Directory ACL Investigation](https://blogs.technet.microsoft.com/pfesweplat/2017/01/28/forensics-active-directory-acl-investigation)
* [Take Control Over AD Permissions And The AD ACL Scanner Tool](https://blogs.technet.microsoft.com/pfesweplat/2013/05/13/take-control-over-ad-permissions-and-the-ad-acl-scanner-tool)

## 📜 History

Features and fixes: [View Changelog](https://github.com/canix1/ADACLScanner/wiki/History)

## ✨ Key Features

### 📊 Reporting & Analysis

* **Effective Rights Analysis**: Generate comprehensive effective rights reports from command line
* **Modified Security Descriptors**: Track when permissions were last modified
* **Excel Export**: Save reports to Excel format without Excel installation (requires ImportExcel module)
* **Command Line Support**: Full automation capabilities for scripted operations
* **Pipeline Integration**: Accept input via PowerShell pipeline using distinguishedName

### 🔍 Advanced Scanning

* **Custom Search Filters**: Target specific objects with flexible filtering options
* **Group Policy Analysis**: Scan linked Group Policy Objects for permission analysis
* **Multiple Output Formats**: HTML, CSV, and Excel report generation

![](https://github.com/canix1/ADACLScanner/blob/master/src/ADACLScan6.0.png)

## Feature list

* Scan linked Group Policy Objects
* View HTML reports of DACLs/SACLs and save it to disk.
* Export DACLs/SACLs on Active Directory objects in a CSV format.
* Export DACLs/SACLs on Active Directory objects in a Excel sheet.
* Connect and browse you default domain, schema , configuration or a naming context defined by distinguishedname.
* Browse naming context by clicking you way around, either by OU�s or all types of objects.
* Report only explicitly assigned DACLs/SACLs.
* Report on OUs , OUs and Container Objects or all object types.
* Filter DACLs/SACLs for a specific access type.. Where does �Deny� permission exists?
* Filter DACLs/SACLs for a specific identity. Where does "Domain\Client Admins" have explicit access? Or use wildcards like "jdoe".
* Filter DACLs/SACLs for permission on specific object. Where are permissions set on computer objects?
* Skip default permissions (defaultSecurityDescriptor) in report. Makes it easier to find custom permissions.
* Report owner of object.
* Compare previous results with the current configuration and see the differences by color scheme (Green=matching permissions, Yellow= new permissions, Red= missing permissions).
* Report when permissions were modified
* Can use AD replication metadata when comparing.
* Can convert a previously created CSV file to a HTML report.
* Effective rights, select a security principal and match it agains the permissions in AD.
* Color coded permissions based on criticality when using effective rights scan.
* List you domains and select one from the list.
* Get the size of the security descriptor (bytes).
* Rerporting on disabled inheritance .
* Get all inherited permissions in report.
* HTLM reports contain headers.
* Summary of criticality for all report types.
* Refresh Nodes by right-click container object.
* Exclude of objects from report by matching string to distinguishedName
* You can take a CSV file from one domain and use it for another. With replacing the old DN with the current domains you can resuse reports between domains. You can also replace the (Short domain name)Netbios name security principals.
* Reporting on modified default security descriptors in Schema.
* Verifying the format of the CSV files used in convert and compare functions.
* When compairing with CSV file Nodes missing in AD will be reported as "Node does not exist in AD"
* The progress bar can be disabled to gain speed in creating reports.
* If the fist node in the CSV file used for compairing can't be connected the scan will stop.
* Display group members in groups in the HTLM report.
* Present the value of the true SDDL in NTsecurityDescriptor, bypassing Object-Specific ACE merge done when a new instance of the ObjectSecurity class is initialized.

## 💻 System Requirements

### ⚙️ Core Requirements

* **PowerShell**: Version 3.0 or higher
* **Threading**: Single-threaded apartment (STA) mode
* **.NET Framework**: Version 4.0 or higher (for specific functions)

### 💾 Optional Dependencies

* **ImportExcel Module**: For Excel file export functionality

  ```powershell
  Install-Module ImportExcel -Scope CurrentUser
  ```

### 🌐 Network Requirements

* Active Directory domain connectivity
* Appropriate permissions for AD object enumeration
* Read access to target Active Directory objects

## 📚 Additional Information

* **Version History**: [View complete changelog](https://github.com/canix1/ADACLScanner/wiki/History)
* **Documentation**: Comprehensive help available within the tool
* **Community**: Report issues and contribute via GitHub
