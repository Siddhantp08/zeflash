# Battery ML Lambda Service

## Setup Instructions

### Environment Variables

Copy `.env.example` to `.env` and fill in your AWS credentials:

```bash
cp .env.example .env
```

Required environment variables:
- `AWS_ACCESS_KEY_ID`: Your AWS access key
- `AWS_SECRET_ACCESS_KEY`: Your AWS secret key
- `AWS_DEFAULT_REGION`: AWS region (default: us-east-1)
- `S3_BUCKET`: S3 bucket name for storing ML results
- `S3_PREFIX`: Prefix for S3 objects (default: battery-reports/)

### Security Notes

⚠️ **IMPORTANT**: Never commit `.env` files with actual credentials to git!

- Keep your AWS credentials secure and private
- Use IAM roles with minimal required permissions
- Rotate credentials regularly
- The `.env` file is already in `.gitignore`

### Required AWS Permissions

Your AWS IAM user/role needs the following permissions:
- S3: `PutObject`, `GetObject`, `ListBucket`
- DynamoDB: (if used) appropriate read/write permissions

## Deployment

See the main project documentation for deployment instructions.
