#This repository is intentionally focused on real failures and how they were resolved, not idealized architectures.


## Why I Enjoy Troubleshooting

I enjoy troubleshooting because it reveals how systems actually behave under real conditions.
When something breaks, I focus on signals — logs, metrics, and system behavior — instead of assumptions.
My approach is to isolate variables, identify root causes, and validate fixes through telemetry

# Cloud Troubleshooting & Systems Debugging

## AWS & Kubernetes
- EKS node failures (IAM, subnet tagging)
- PVCs stuck Pending (EBS CSI lifecycle)
- Prometheus / Grafana telemetry gaps

## Azure & Identity
- Conditional Access false positives
- MFA enforcement analysis
- Risk-based sign-in troubleshooting

## Edge & Security
- WAF rule tuning and exclusions

## Infrastructure as Code
- Terraform provider failures
- Permission and dependency resolution

## How I Troubleshoot
- Follow signals, not assumptions
- Isolate variables
- Validate fixes through telemetry
