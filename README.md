<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./images/logo-dark.png" width="300px;">
  <img alt="Text changing depending on mode. Light: 'So light!' Dark: 'So dark!'" src="./images/logo-light.png" width="300px;">
</picture>
<br/>

# Isotope

Isotope scans AWS services and makes suggestions on how to improve them using AWS Bedrock (Artificial Intelligence).

## Key benefits
- No exfiltration of data beyond your AWS account 
- Discrete examination of your services within AWS
- Simplistic remediation steps designed for humans.

## Installation

```
brew install isotope-rs/homebrew-isotope/isotope
```

## Usage

1. Set environment variables for AWS access

```
export AWS_ACCESS_KEY=""
export AWS_SECRET_ACCESS_KEY=""
export BEDROCK_REGION="eu-central-1"  ( e.g. us-east-1,us-west-2, ap-southeast-1, ap-northeast-1 )
export BEDROCK_MODEL="anthropic.claude-v2" ( e.g. anthropic.claude-v2, anthropic.claude-v1, anthropic.claude-instant-v1 )
```
2. Run all isotope analyzers

```
isotope 
```

Optionally for a single analyzer

```
isotope -a S3
```

### Analyzers

- S3
    - Public bucket detection
- STS
  - MFA detection




