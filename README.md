# Advanced-Traversal-LFI-Wordlist

A curated wordlist focused on **Path Traversal**, **Local File Inclusion (LFI)**, and sensitive file discovery.

This collection contains payloads and paths commonly used during authorized penetration testing and security research to identify:

- Directory Traversal vulnerabilities
    
- Local File Inclusion (LFI)
    
- Log file exposure
    
- Sensitive file disclosure
    
- Admin panel discovery
    
- Encoding and filter bypass attempts
    

---

## 📂 Content Overview

This wordlist includes:

### 1️⃣ Basic Traversal Payloads

Examples:

```cs
../  
../../  
../../../
```

---

### 2️⃣ Encoded Traversal Bypass

Examples:

```cs
%2f  
%5c  
..%2f..%2f  
..%5c..%5c
```

Used to bypass weak input filters.

---

### 3️⃣ Windows-Specific Targets

Examples:

```cs
/boot.ini  
windows/win.ini
```

---

### 4️⃣ Log File Discovery

Examples:

```cs
/apache2/logs/access.log  
/apache2/logs/access_log  
../../../../apache2/logs/access.log  
admin/access_log
```

Useful for LFI-to-RCE escalation attempts (log poisoning scenarios).

---

### 5️⃣ Administrative Paths

Examples:

```cs
/admin/install.php  
../../../administrator/inbox
```

---

## 🎯 Intended Use

This wordlist is designed for:

- Bug bounty research
    
- CTF challenges
    
- Security training labs
    
- Authorized penetration testing
    
---

## 💡 Recommended Usage

You can use this wordlist with tools such as:

- ffuf
    
- Burp Suite Intruder
    
- wfuzz
    
- dirsearch (for path testing)
    
- Custom scripts
    
- dirsearch

---

## ⚙️ Installation (Using wget)

Download the wordlist directly:

```bash
wget https://raw.githubusercontent.com/brono4/Path-Traversal-and-File-Disclosure-Wordlist/main/traversal-lfi-wordlist.txt
```

After download, you’re ready to use it ✅

---

## 🚀 Quick Usage Example

With **ffuf**:

```bash
ffuf -u https://target.com/page=FUZZ -w traversal-lfi-wordlist.txt
```
