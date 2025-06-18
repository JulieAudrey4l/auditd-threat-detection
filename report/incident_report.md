#Incident Report: Unauthorized File Access Detection

## Overview

This report outlines the detection of unauthorized access to a sensitive file (`testfile.txt`) on a monitored Linux system using `auditd`.

---

##System Setup

- **Monitored system**: Ubuntu 22.04 (Defender VM)
- **Attacker**: Kali Linux (via SSH)
- **Monitoring tool**: `auditd`
- **Target file**: `~/testfile.txt`

---

##Simulated Attack

The attacker connected via SSH and modified the file:

```bash
ssh defender@192.168.56.101
echo "attacker was here" >> ~/testfile.txt
```
