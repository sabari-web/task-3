Basic Vulnerability Scan - 

## 🔍 Objective
To perform a basic vulnerability scan on my local PC using **Nessus Essentials** and identify common security issues.

---

## 🧰 Tools Used
- [Nessus Essentials](https://www.tenable.com/products/nessus/nessus-essentials)


## 📝 Steps Followed

1. **Installed Nessus Essentials**
   - Downloaded from Tenable's official website
   - Installed and activated using a free license key

2. **Set Up Scan**
   - Created a scan using "Advanced Scan" template
   - Target: ` 192.168.80.1` (local machine)
  
  

3. **Ran Full Vulnerability Scan**

   - Scanner automatically identified open ports, services, and OS version

4. **Reviewed Results**
   - Exported report in HTML format (`file:///C:/Users/sabha/Downloads/Local%20Vulnerability%20Scan%201_54j5gc.html#id1`)
   - Analyzed detected vulnerabilities and severity levels

---

## ⚠️ Critical Vulnerabilities Found

| Plugin ID | Vulnerability Title | Severity | Description |
|----------:|---------------------|----------|-------------|
| 108798    | SMB Signing not required | High | Can lead to man-in-the-middle attacks on SMB connections |
| 26920     | Outdated OpenSSL version | Medium | May be vulnerable to known CVEs (e.g., Heartbleed) |
| 33850     | Anonymous FTP login allowed | Medium | Unauthorized users may access files without authentication |
| 19506     | Nessus Scan Information | Info | General scan metadata, not a vulnerability |

---

## 🔧 Fixes / Mitigation Steps

- **SMB Signing**: Enforce SMB signing via Windows Group Policy or Samba config.
- **OpenSSL**: Update OpenSSL package to the latest secure version.
- **Anonymous FTP**: Disable anonymous access in the FTP server config.
- **Regular Updates**: Ensure OS and software patches are applied regularly.



## 📌 CVSS Awareness

- Most vulnerabilities are rated using **CVSS (Common Vulnerability Scoring System)**.
- Critical issues have CVSS scores above **7.0**, requiring immediate attention.

---

## 📅 Recommended Scan Frequency
- Personal computers: Monthly
- Enterprise environments: Weekly or after major system changes
