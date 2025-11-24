---
slug: github-gcputils-note-technical-overview
id: github-gcputils-note-technical-overview
title: gcputils
repo: justin-napolitano/gcputils
githubUrl: https://github.com/justin-napolitano/gcputils
generatedAt: '2025-11-24T18:36:59.065Z'
source: github-auto
summary: >-
  This repo is a Python utility library that simplifies interactions with Google
  Cloud Platform services, including BigQuery, Cloud Storage, Cloud Logging, and
  Secret Manager. I built it to consolidate common GCP client code into a single
  module for easy reuse.
tags: []
seoPrimaryKeyword: ''
seoSecondaryKeywords: []
seoOptimized: false
topicFamily: null
topicFamilyConfidence: null
kind: note
entryLayout: note
showInProjects: false
showInNotes: true
showInWriting: false
showInLogs: false
---

This repo is a Python utility library that simplifies interactions with Google Cloud Platform services, including BigQuery, Cloud Storage, Cloud Logging, and Secret Manager. I built it to consolidate common GCP client code into a single module for easy reuse.

## Key Components

- **BigQueryClient**: Handles dataset creation and table checks.
- **GCSClient**: Manages Cloud Storage buckets, including listing and creating.
- **GoogleCloudLogging**: Sends logs to Cloud Logging with configurable severity.
- **GoogleSecretManager**: Retrieves secrets securely.

## Getting Started

1. Ensure you have Python 3 and Google Cloud SDK installed and authenticated.
2. Add the repo as a submodule:

   ```bash
   git submodule add -b pit https://github.com/justin-napolitano/gcputils.git
   ```

3. Install required packages:

   ```bash
   pip install google-cloud-storage google-cloud-bigquery google-cloud-logging google-cloud-secret-manager
   ```

## Usage

Initialize the clients like this:

```python
from gcputils.gcpclient import GCSClient

gcs_client = GCSClient('your-gcp-project-id', credentials_path='path/to/credentials.json')
print(gcs_client.list_buckets())
```

Check each client for available methods.
