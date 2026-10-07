# Required GitHub Secrets

Each environment uses its own set of secrets, with the environment name as a
suffix: `DEV`, `RELEASE`, `DEMO` or `PROD`. Example for the demo environment:

| Secret | Purpose |
|---|---|
| `AWS_ACCESS_KEY_ID_DEMO` | IAM user access key used by the pipeline |
| `AWS_SECRET_ACCESS_KEY_DEMO` | IAM user secret key |
| `AWS_REGION_DEMO` | AWS region of the ECR repository |
| `ECR_REPO_URI_DEMO` | Full ECR repository URI, e.g. `123456789012.dkr.ecr.eu-west-1.amazonaws.com/trainings-manager` |
| `EC2_HOST_DEMO` | Public IP or hostname of the EC2 instance |
| `EC2_USER_DEMO` | SSH user on the instance (e.g. `ubuntu`) |
| `SSH_KEY_DEMO` | Private SSH key for the deploy user |

The IAM user needs only the ECR permissions to push and pull images
(`ecr:GetAuthorizationToken`, `ecr:BatchCheckLayerAvailability`,
`ecr:PutImage`, `ecr:InitiateLayerUpload`, `ecr:UploadLayerPart`,
`ecr:CompleteLayerUpload`, `ecr:BatchGetImage`, `ecr:GetDownloadUrlForLayer`).
