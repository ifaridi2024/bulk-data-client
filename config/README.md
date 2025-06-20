# Bulk Data Client Config

## Config Files for Server Connection and Download Configuration

In order make it workable, make sure you configure AWS config settings in your running environment for FHIR Bulk Account.

![AWS Account](account.png)

```sh
export AWS_ACCESS_KEY_ID="ASIAZZBVXAFOMDPSMJZI"
export AWS_SECRET_ACCESS_KEY="bFDgw9usmcOwBeKx9/jr2svEeAoHDFWKr72cY2s1"
export AWS_SESSION_TOKEN="IQoJb3JpZ2luX2VjEKj//////////8k27U9L9GAD2bSMLSFLo6DRkE3jZKO1QRhNNNC1Wu6NeHojx+0="
```

### 1. BCDA Server Config
This configuration will upload files to S3 bucket in BCDA folder.

File Server URL: https://sandbox.bcda.cms.gov/api/v2/

For running Bulk client to upload files in AWS S3 bucket use the following CLI command
```sh
node . --config config/bcda-config.js --reporter text
```

### 2. Bulk Data Server Config
This configuration will upload files to S3 bucket in FHIR folder.

File Server URL: https://bulk-data.smarthealthit.org/

For running Bulk client to upload files in AWS S3 bucket use the following CLI command
```sh
node . --config config/fhir-config.js --reporter text
```

### AWS Bucket location for both Bulk data client and BCDA:

![S3 Bucket](s3.png)
