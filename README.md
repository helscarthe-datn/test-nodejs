# test-nodejs

Simple Node.js app scaffolded by Backstage.

## Run locally

```
node index.js
```

## Terraform (EC2)

This repo includes a minimal Terraform setup under `infra/` to create a single EC2 instance.

### Prereqs

- Terraform installed
- AWS credentials available in your environment
- An existing AWS key pair name (optional, but recommended)

### Quick start

```
cd infra
terraform init
terraform apply
```

### Inputs

- `aws_region` (default: `us-east-1`)
- `instance_type` (default: `t3.micro`)
- `key_name` (optional)
- `allowed_ssh_cidr` (default: `0.0.0.0/0`)
- `allowed_app_cidr` (default: `0.0.0.0/0`)
- `app_port` (default: `3000`)

### Outputs

- `public_ip`
- `public_dns`
