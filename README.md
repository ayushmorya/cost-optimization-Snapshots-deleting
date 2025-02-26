# cost-optimization-Snapshots-deleting



The Smart Vault

Overview

The Smart Vault is an AWS-based cost-optimization solution for managing EC2 snapshots. It automates the deletion of outdated snapshots, ensuring cost-effective storage management while maintaining compliance with backup policies. The solution leverages AWS Free Tier components for affordability and efficiency.

Features

Automated snapshot deletion based on retention policies

Event-driven architecture using AWS EventBridge

Serverless execution using AWS Lambda

Notification alerts via AWS SNS

Monitoring with AWS CloudWatch

Disaster recovery support with Amazon S3

AWS Services Used

Amazon EC2 (Elastic Compute Cloud) – Source instances for backups

Amazon EBS (Elastic Block Store) – Persistent storage for EC2 instances

Amazon S3 – Optional backup storage for disaster recovery

AWS Lambda – Automates snapshot deletion

Amazon CloudWatch – Monitors logs and events

Amazon SNS (Simple Notification Service) – Sends alerts and notifications

Amazon EventBridge – Triggers automated deletion workflows

Architecture

The Smart Vault follows a serverless and event-driven architecture:

EventBridge Rule: Triggers based on a scheduled time (e.g., daily or weekly) to evaluate existing snapshots.

Lambda Function: Fetches EBS snapshots, applies the retention policy, and deletes outdated snapshots.

CloudWatch Logs: Captures execution details and errors for monitoring.

SNS Notifications: Sends alerts about deleted snapshots or any issues encountered.

Prerequisites

An AWS account (Free Tier recommended)

IAM permissions for Lambda to manage EC2 snapshots and logs

AWS CLI configured (optional for manual testing)
