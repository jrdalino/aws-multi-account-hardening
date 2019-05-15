# AWS Organization & Multi-Account Hardening

## Step 1: AWS Organizations and Multi-Account Hardening
- Wait for https://aws.amazon.com/controltower/
- Enable AWS Organizations + Landing Zone (https://aws.amazon.com/solutions/aws-landing-zone/)
- Add SCP Policies
- Create new AWS Account per product and per environment (production and staging)
- New Email alias, AWS Account, Contacts
- Secure Root User, MFA
- Delete Default VPC's
- S3 Buckets for Logging
- S3 Buckets for ELB Logging
- S3 Buckets for Cloudfront Logs
- Enable CloudTrail Logs (Auditing)
- Enable VPC Flow Logs
- Enable ELB Logging
- Enable Config for AWS resource config tracking
- Enable SNS topics for alerting and notifications
- Enable Guard Duty for Intelligent threat detection
- Enable Security Hub for Compliance Scanning

## (Clean Up)
