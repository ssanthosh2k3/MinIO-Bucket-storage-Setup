#  MinIO Object Storage Setup (Pre-Production & Internal Use)

This repository documents the setup, usage, and maintenance of a **MinIO S3-compatible object storage** instance configured for **pre-production environments** and **internal use cases**.

---

![jenkinsProcess Output](https://github.com/ssanthosh2k3/MinIO-Bucket-storage-Setup/blob/main/IMG_20250406_183314_793.jpg)


## 📚 Table of Contents

- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Creating Buckets](#creating-buckets)
- [Uploading Files](#uploading-files)
- [Access Control](#access-control)
- [Use Cases](#use-cases)
- [Maintenance & Cleanup](#maintenance--cleanup)
- [Monitoring (Optional)](#monitoring-optional)
- [References](#references)
- [Contact](#contact)

---

## 📌 Overview

MinIO is a lightweight, high-performance, object storage system with S3 API compatibility. It is ideal for:

- Hosting internal files and artifacts
- CI/CD pipeline storage
- Backup and restore workflows
- Testing S3 integrations before moving to production

---
![jenkinsProcess Output](https://github.com/ssanthosh2k3/MinIO-Bucket-storage-Setup/blob/main/IMG_20250406_183346_059.jpg)



## 🧰 System Requirements

- macOS or Linux
- Homebrew (for macOS users)
- MinIO Server (running on a VM, container, or bare metal)
- Access credentials (Access Key / Secret Key)

---

![jenkinsProcess Output](https://github.com/ssanthosh2k3/MinIO-Bucket-storage-Setup/blob/main/IMG_20250406_183241_162.jpg)


## 🔧 Installation

### ✅ Install MinIO Client (`mc`)

#### macOS (via Homebrew):

```bash
brew install minio/stable/mc
```

![jenkinsProcess Output](https://github.com/ssanthosh2k3/MinIO-Bucket-storage-Setup/blob/main/IMG_20250406_183257_612.jpg)


###🔐 Access Control
- 🔑 Access credentials are managed using internal vaults or CI/CD secrets.

- 🔐 TLS should be enabled in production environments.

- 🔒 MinIO policy management can be used to limit access to buckets.


##You can integrate with Prometheus & Grafana:

- Enable metrics using:
```
  mc admin prometheus generate internal-minio/
```

##Import MinIO dashboards to Grafana.

### References
- MinIO Official Docs

- MinIO Client (mc) CLI Docs

- MinIO GitHub
