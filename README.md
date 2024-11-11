# AWS Nuke Automation

This repository automates the process of cleaning up AWS accounts using [aws-nuke](https://github.com/rebuy-de/aws-nuke). It is designed to run periodically or on-demand through a CI/CD pipeline to remove all resources from specified AWS accounts, ensuring cost optimization and better resource management.

## Overview

`aws-nuke` is a tool used to delete all resources within an AWS account. This repository sets up a GitHub Actions workflow that runs `aws-nuke` for different AWS regions in a secure and automated manner.

## Features

- **Scheduled Cleanup**: Runs at specific times based on your CI/CD configuration.
- **Multi-Region Support**: Configured for different AWS regions.
- **Error Handling**: Detailed logging and error handling in case of failures.
- **Platform Compatibility**: Supports both `linux/amd64` and `linux/arm64` architectures for flexible deployment.

## Repository Structure

```plaintext
.
├── .github/workflows        # Contains the CI/CD pipeline configuration
│   └── aws-nuke.yml         # GitHub Actions workflow for running aws-nuke
├── nuke
│   └── config
│       └── config.yaml      # Configuration file for aws-nuke specifying resources to clean up
├── Dockerfile               # Dockerfile for building a custom aws-nuke container
├── README.md                # This file
