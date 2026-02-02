# AWS Operations and Security Project

## What this is
Portfolio project focused on operating and securing AWS workloads.  
It includes monitoring and alerting setup, CloudTrail auditing, IAM hardening notes, and support-style runbooks for common incidents.

## Architecture
This repo assumes a workload exists, for example the hosted app project, and adds an operations layer:

- CloudWatch dashboards and alarms
- Centralized logs using CloudWatch Logs
- CloudTrail for audit events
- IAM hardening decisions documented

Diagrams will be stored in `/diagrams`.

## Requirements
- AWS account with IAM user and MFA
- CloudWatch and CloudTrail access
- Optional: A deployed sample workload to generate metrics and logs. Can be minimal

## Deploy steps
This section will document:
- Enable and verify CloudTrail
- Create CloudWatch dashboards
- Create alarms:
  - 5xx errors
  - Unhealthy targets
  - CPU and memory where applicable
- Configure log retention to control cost

## Validate steps
This section will document how to confirm:
- CloudTrail is recording events
- Logs are flowing to CloudWatch
- Alarms trigger in a controlled test

## Monitoring and alerts
This project will include:
- Dashboard screenshots or exported JSON
- Alarm list and rationale
- Suggested thresholds and what they catch
- Cost controls such as log retention and avoiding high-cost services

## Security notes
This project will document:
- Root MFA and account safety steps
- IAM approach. Least privilege and roles instead of access keys
- How to investigate events using CloudTrail
- Optional additions later. GuardDuty and Config if enabled

## Runbooks
Runbooks will be stored in `/runbooks`:
- `site-down.md`
- `5xx-spike.md`
- `dns-issues.md`
- `permission-denied-iam.md`
- `security-group-blocking-traffic.md`

Each runbook will include symptoms, checks, likely causes, fix steps, and verification.

## Teardown
Steps to remove alarms, dashboards, log groups, and trails created for the project.

## Lessons learned
Summary of operational patterns, common incident causes, and improvements.
