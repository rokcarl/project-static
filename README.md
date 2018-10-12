# Static project

This project shows the entire lifecycle of a static project.

## Create Infra

```bash
STACK_NAME=project-static
aws cloudformation deploy --template-file infra/cf/infra.yml --stack-name $STACK_NAME --parameter-overrides file://./infra/cf/infra-params-secrets.json --capabilities CAPABILITY_NAMED_IAM
```
