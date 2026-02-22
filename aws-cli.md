Here are the most commonly used AWS CLI commands organized by service:

**General / Setup**
- `aws configure` — set up credentials, region, output format
- `aws configure list` — view current config
- `aws sts get-caller-identity` — verify who you're authenticated as (account ID, user/role ARN)

**S3**
- `aws s3 ls` — list all buckets
- `aws s3 ls s3://bucket-name` — list contents of a bucket
- `aws s3 cp file.txt s3://bucket-name/` — upload a file
- `aws s3 cp s3://bucket-name/file.txt .` — download a file
- `aws s3 sync ./folder s3://bucket-name/` — sync a local folder to S3
- `aws s3 rm s3://bucket-name/file.txt` — delete a file

**EC2**
- `aws ec2 describe-instances` — list all EC2 instances
- `aws ec2 start-instances --instance-ids i-xxxx` — start an instance
- `aws ec2 stop-instances --instance-ids i-xxxx` — stop an instance
- `aws ec2 describe-security-groups` — list security groups

**IAM**
- `aws iam list-users` — list all IAM users
- `aws iam list-roles` — list all roles
- `aws iam get-user` — get current IAM user info
- `aws iam create-user --user-name bob` — create a new user

**Lambda**
- `aws lambda list-functions` — list all Lambda functions
- `aws lambda invoke --function-name my-fn output.json` — invoke a function
- `aws lambda get-function --function-name my-fn` — get function details

**CloudFormation**
- `aws cloudformation list-stacks` — list stacks
- `aws cloudformation deploy --template-file template.yaml --stack-name my-stack` — deploy a stack
- `aws cloudformation delete-stack --stack-name my-stack` — delete a stack

**Logs (CloudWatch)**
- `aws logs describe-log-groups` — list log groups
- `aws logs tail /aws/lambda/my-fn --follow` — stream logs in real time

**Useful Flags**
- `--region us-east-1` — override region for a single command
- `--profile my-profile` — use a specific named profile
- `--output table` — format output as a table for readability
- `--query` — filter output using JMESPath, e.g. `--query 'Instances[*].InstanceId'`

A handy pattern: append `help` to any command to see its docs, e.g. `aws s3 cp help`.
