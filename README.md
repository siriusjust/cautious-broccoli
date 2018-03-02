To deploy the CloudFormation stack:

`aws cloudformation package --template-file app-spec.yml --s3-bucket team#_code --output-template-file packaged_template.yml`

This will take the hand-coded stack specification and package it into something that CloudFormation can use, as well as upload artifacts (e.g. the lambda functions) to S3 where it can get at them.

`aws cloudformation deploy --template-file packaged_template.yml --stack-name <a_stack_name> --capabilities CAPABILITYIAM`

This actually uploads the thing.