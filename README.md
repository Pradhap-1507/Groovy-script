**Jenkins Pipeline for Validating and Processing Artifacts in AWS S3**
This repository contains a Jenkins pipeline script designed to validate user-provided artifacts against the latest artifacts in an AWS S3 bucket. The script ensures artifact accuracy and includes safeguards to prevent deploying outdated files.

**Features:**

User Input: Prompts the user to specify the artifact for processing.

AWS S3 Integration: Lists and validates contents from an S3 bucket using the AWS CLI.

Artifact Validation: Compares the user-provided artifact with the latest artifact in the bucket based on timestamps.

Dynamic Decision Making: Warns and requests confirmation before proceeding if the artifact does not match the latest version.

Error Handling: Ensures robust error reporting for missing artifacts or invalid input.

**Use Case:**
This pipeline is ideal for CI/CD workflows where:

Artifacts (e.g., build files or deployment packages) are stored in an S3 bucket.
Validating and deploying the correct version of an artifact is critical to ensure reliability and consistency.

**Prerequisites:**
Jenkins configured with AWS CLI and credentials to access the S3 bucket.
A valid S3 bucket and folder structure.
