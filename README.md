# Chronicle 3p Ingestion Scripts

### Deploying the cloud function

Execute the following command from inside the previously created directory to
deploy the cloud function.

```
gcloud functions deploy <FUNCTION NAME> --entry-point main --trigger-http --runtime python39 --env-vars-file .env.yml
```

### Setting the required runtime environment variables

Edit the .env.yml file to populate all the required environment variables.
Information related to all the environment variables can be found in the
README.md file.

#### Common runtime environment variables

The following envs are available

CHRONICLE_CUSTOMER_ID
CHRONICLE_REGION
CHRONICLE_SERVICE_ACCOUNT
CHRONICLE_DATA_TYPE

#### Using secrets

CHRONICLE_SERVICE_ACCOUNT should not be directly stored as an env on the cloud function. Instead the secret functionality of the cloud function can be used to assign a secret to the env CHRONICLE_SERVICE_ACCOUNT. See UI 

