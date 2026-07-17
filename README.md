# AWS Cloud Security Monitoring Infrastructure

Automated cloud security monitoring system built with Terraform that detects threats, logs AWS activity, and delivers real-time email alerts.

## Architecture

GuardDuty → EventBridge → SNS → Email Alert
CloudTrail → S3 Bucket (Private)

## Components

| Service | Purpose |
|---|---|
| AWS GuardDuty | Monitors for malicious activity and unauthorized behavior |
| AWS CloudTrail | Records all AWS API calls across all regions |
| AWS S3 | Private bucket for secure CloudTrail log storage |
| AWS SNS | Sends real-time email alerts when threats are detected |
| AWS EventBridge | Routes GuardDuty findings to SNS automatically |

## Security Features

- S3 bucket with public access fully blocked
- Multi-region CloudTrail enabled
- Automated alerting with zero manual intervention

## Usage

```bash
terraform init
terraform plan
terraform apply
terraform destroy
```

## Technologies
Terraform · AWS GuardDuty · AWS CloudTrail · AWS S3 · AWS SNS · AWS EventBridge
