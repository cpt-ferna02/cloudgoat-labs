# cloudgoat-labs
# ☁️ CloudGoat Labs — AWS Cloud Security Attack & Defense

A collection of hands-on AWS penetration testing labs using [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) by Rhino Security Labs. Each scenario simulates a real-world AWS attack technique in a controlled, intentionally vulnerable environment.

These labs complement my existing security projects by adding cloud offensive security coverage — practicing the same attack techniques seen in real-world AWS breaches, and documenting the defensive detections to stop them.

---

## 🎯 Objectives

- Practice real-world AWS attack techniques in a safe lab environment
- Understand how IAM misconfigurations lead to privilege escalation
- Simulate cloud data breaches using SSRF and credential theft
- Map all attacks to MITRE ATT&CK framework
- Document detection and remediation strategies for each attack

---

## 🛠️ Lab Environment

| Component | Details |
|---|---|
| **Tool** | CloudGoat by Rhino Security Labs |
| **Platform** | AWS (dedicated lab account) |
| **OS** | Ubuntu 24.04 (WSL2 on Windows) |
| **Languages** | Python, Bash, AWS CLI |
| **Frameworks** | MITRE ATT&CK for Cloud |

---

## 📁 Scenarios Completed

| # | Scenario | Difficulty | Techniques | Status |
|---|---|---|---|---|
| 01 | [IAM Privilege Escalation by Rollback](./01-iam_privesc_by_rollback/) | 🟢 Easy | IAM Enumeration, Policy Rollback, PrivEsc | ✅ Complete |
| 02 | [Cloud Breach via S3](./02-cloud_breach_s3/) | 🟢 Easy | SSRF, Credential Theft, Data Exfiltration | ✅ Complete |

---

## 🧠 MITRE ATT&CK Coverage

| Technique ID | Technique Name | Scenario |
|---|---|---|
| T1078.004 | Valid Accounts: Cloud Accounts | 01, 02 |
| T1548 | Abuse Elevation Control Mechanism | 01 |
| T1098 | Account Manipulation | 01 |
| T1552.005 | Cloud Instance Metadata API | 02 |
| T1530 | Data from Cloud Storage Object | 02 |

---

## ⚙️ Setup

See [CloudGoat's official repo](https://github.com/RhinoSecurityLabs/cloudgoat) for full installation instructions.

**Prerequisites:**
- AWS Free Tier account (dedicated lab account recommended)
- Python 3.x
- Terraform
- AWS CLI v2
- CloudGoat installed via Poetry

**Quick Start:**
```bash
git clone https://github.com/RhinoSecurityLabs/cloudgoat.git
cd cloudgoat
pip3 install poetry
poetry install
poetry run cloudgoat config aws
poetry run cloudgoat config whitelist --auto
```

---

## ⚠️ Disclaimer

All labs are conducted in a dedicated AWS account using intentionally vulnerable resources created by CloudGoat. These techniques are documented for **educational purposes only**. Never use these techniques against systems you do not own or have explicit permission to test.

---

## 🔗 Related Projects

- [Active Directory Lab](https://github.com/cpt-ferna02/active-directory-lab)
- [Splunk SIEM Lab](https://github.com/cpt-ferna02/splunk-siem-lab)
- [Python Log Analyzer](https://github.com/cpt-ferna02/python-log-analyzer)
- [IR Toolkit](https://github.com/cpt-ferna02/ir-toolkit)
