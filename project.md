---
slug: github-gcputils
id: github-gcputils
title: Python Utility Library for Google Cloud Platform Services
repo: justin-napolitano/gcputils
githubUrl: https://github.com/justin-napolitano/gcputils
generatedAt: '2025-11-24T21:34:53.066Z'
source: github-auto
summary: >-
  A Python library that provides reusable clients for Google Cloud services like
  BigQuery and Cloud Storage to streamline development.
tags:
  - python
  - google-cloud-storage
  - google-cloud-bigquery
  - google-cloud-logging
  - google-cloud-secret-manager
seoPrimaryKeyword: google cloud platform python utility
seoSecondaryKeywords:
  - gcp client library
  - bigquery client
  - cloud storage management
  - secret manager access
  - python gcp utilities
seoOptimized: true
topicFamily: null
topicFamilyConfidence: null
kind: project
entryLayout: project
showInProjects: true
showInNotes: false
showInWriting: false
showInLogs: false
---

A Python utility library providing reusable clients for Google Cloud Platform services including BigQuery, Cloud Storage, Cloud Logging, and Secret Manager. Designed to streamline development by consolidating common GCP client code into a single submodule.

---

## Features

- **BigQueryClient**: Simplifies dataset creation and table existence checks.
- **GCSClient**: Manage Google Cloud Storage buckets, list buckets, and create new buckets.
- **GoogleCloudLogging**: Setup and send logs to Google Cloud Logging with configurable severity.
- **GoogleSecretManager**: Access secrets securely from Google Secret Manager.

## Tech Stack

- Python 3
- Google Cloud Client Libraries:
  - `google-cloud-bigquery`
  - `google-cloud-storage`
  - `google-cloud-logging`
  - `google-cloud-secret-manager`

## Getting Started

### Prerequisites

- Python 3 installed
- Google Cloud SDK installed and authenticated

### Installation

Clone the repository as a Git submodule in your project:

```bash
git submodule add -b pit https://github.com/justin-napolitano/gcputils.git
```

Install required Google Cloud libraries:

```bash
pip install google-cloud-storage google-cloud-bigquery google-cloud-logging google-cloud-secret-manager
```

### Usage

Import and initialize clients in your Python code. Example for Google Cloud Storage:

```python
from gcputils.gcpclient import GCSClient

project_id = 'your-gcp-project-id'
gcs_client = GCSClient(project_id, credentials_path='path/to/credentials.json')

buckets = gcs_client.list_buckets()
print(buckets)
```

Refer to each client class for available methods.

## Project Structure

```
./
├── bash/                      # Bash scripts (if any)
├── BigQueryClient.py          # BigQuery client wrapper
├── gcpclient.py               # Google Cloud Storage client wrapper
├── GoogleCloudLogging.py      # Cloud Logging client wrapper
├── GoogleSecretManager.py     # Secret Manager client wrapper
├── google-cloud-stroage-python.md # Documentation snippet for GCS Python library
├── index.md                   # Project overview and usage guide
└── readme.md                  # This README file
```

## Future Work / Roadmap

- Complete implementation and testing of BigQueryClient methods.
- Add support for additional GCP services.
- Enhance error handling and logging.
- Provide more comprehensive usage examples and documentation.
- Automate deployment and CI/CD integration.

---

*Note: This repository is intended as a reusable submodule for GCP client utilities to avoid code duplication across projects.*
