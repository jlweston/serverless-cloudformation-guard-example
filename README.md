# serverless-cloudformation-guard-example

A simple demonstration of using AWS's CloudFormation Guard alongside the Serverless framework to provide guards that ensure the created CloudFormation templates adhere to defined rules.

CloudFormation Guard allows us to shift left the testing of our stack, so we can discover instances of broken guard rules during the development process instead of at deploy time.

## Usage

- Inspect the rules defined in `cfn.guard`
- Run `npm run package`
- Inspect the failures in the console when packaging fails

You will see that the first rule that S3 bucket names must match a pattern passes. However, the second rule around access policies for buckets fails, as we have not correctly set these properties in `serverless.yml`.
