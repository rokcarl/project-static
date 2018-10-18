# Static project

This project shows the entire lifecycle of a static project.

## Run locally

```bash
npm run build
npm run start
```
Then you can visit http://localhost:3000 to see the page.

## Create Infra

### Set up secrets

1. Copy the example secrets file: `cp infra/cf/infra-params-secrets-example.json infra/cf/infra-params-secrets.json`.
2. Edit the file `infra/cf/infra-params-secrets.json` and put in your secrets where needed.

### Provision infrastructure

```bash
STACK_NAME=project-static
aws cloudformation deploy --template-file infra/cf/infra.yml --stack-name $STACK_NAME --parameter-overrides file://./infra/cf/infra-params-secrets.json --capabilities CAPABILITY_NAMED_IAM
```
