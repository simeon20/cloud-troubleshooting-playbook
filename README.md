## Real Failures & Fixes

> This repository intentionally documents real failures and how they were resolved,
> focusing on system behavior observed through logs, metrics, and controlled testing
> rather than architectures.

### Serverless & Event-Driven Systems
- EventBridge rules not triggering Lambda → fixed via event pattern isolation and schema validation
- Lambda invocation failures due to missing permissions → resolved through explicit invoke roles
- Silent event loss → mitigated with SQS DLQ attachment and failure testing
- Overly permissive IAM → replaced DynamoDBFullAccess with scoped read/write policies

### API Gateway, Auth & Edge Security
- Cognito JWT 401/403 errors → corrected issuer, audience, and token type alignment
- HTTP API event parsing issues → fixed handler logic for request context
- API abuse risk → mitigated with AWS WAF rate-based rules

### Data Modeling & Query Behavior
- Inefficient scans → replaced with DynamoDB GSIs for status/time access patterns
- Composite key retrieval issues → normalized identifiers and query paths

### Observability & Reliability
- Missing failure visibility → added CloudWatch alarms for errors and throttles
- False confidence from green dashboards → validated alerts via forced failures

### Kubernetes, Identity & IaC (Prior Projects)
- EKS node registration failures → resolved IAM + subnet tagging issues
- PVCs stuck Pending → corrected EBS CSI lifecycle + IRSA
- Conditional Access false positives → tuned risk signals and policy order
- Terraform provider/dependency failures → resolved via version pinning and explicit dependencies
