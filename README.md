# AWS Organizations & Multi-Account Hardening

## Prerequisites
- New Email aliases

## Step 1: AWS Organizations and Multi-Account Hardening

### Step 1.1: Create AWS Organization
- Enable AWS Organizations + Landing Zone (https://aws.amazon.com/solutions/aws-landing-zone/)

### Step 1.2: Create Core OU's

### Step 1.3: Create Core Accounts
- AWS Organizations AWS Account
- Shared Services AWS Account
- Log Archive AWS Account
- Security AWS Account
- Identity & Access AWS Account (Replace with AWS SSO + Directory Connector)
- (Optional) Network AWS Account for Direct Connect

### Step 1.4: Add SCP Policies
- Prevent Users from Disabling AWS CloudTrail
- Prevent Users from Disabling Amazon CloudWatch or Altering Its Configuration
- Prevent Users from Deleting Amazon VPC Flow Logs
- Prevent Users from Disabling AWS Config or Changing Its Rules
- Denies Access to AWS Based on the Requested Region
- Require Encryption on Amazon S3 Buckets
- Denies the modification of the account contacts & settings via the Billing Portal and My Account Page
- Denies the account from leaving the organization

Reference
- https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_example-scps.html
- https://github.com/jchrisfarris/aws-service-control-policies

### Step 1.5: Per new Developer Create a Sandbox and per Project a set of Development, Staging and Production Accounts
- Developer Sandbox AWS Account
- Development AWS Account
- Staging AWS Account
- Production AWS Account

### Step 1.6: Activate MFA and Secure Root User

### Step 1.7: Create Groups, Users and Roles in the Identify & Access Account

### Step 1.8: In All Accounts Apply IAM Password Policy

### Step 1.9 Create S3 Buckets in the Log Archive Account
- CloudTrail Logs
- Config Logs
- ELB Logs
- Cloudfront Logs
- VPC Flow Logs

### Step 1.10: Enable SNS topics for alerting and notifications

### Step 1.11: In All Accounts Enable AWS CloudTrail and send logs to Log Archive Account

### Step 1.12: Enable Config for AWS resource config tracking

### Step 1.13 Enable Config Rules
- https://github.com/awslabs/aws-config-rules
- https://github.com/awslabs/aws-config-engine-for-compliance-as-code

### Step 1.14: In All Accounts Delete Default VPC's in all Regions

### Step 1.15: Enable Guard Duty for Intelligent threat detection

### Step 1.16: Enable Security Hub for Compliance Scanning

### Step 1.17: Enable Cost Usage Report
- https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-reports-gettingstarted-turnonreports.html

### Step 1.18: Create Tags
- https://aws.amazon.com/answers/account-management/aws-tagging-strategies/

### Step 1.19: Create AWS Budgets
- https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/budgets-create.html

## (Clean Up)

## Others
- Check Out https://aws.amazon.com/controltower/
