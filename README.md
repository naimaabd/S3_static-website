# Terraform S3 Static Website Deployment

## Overview

This Terraform project automates the deployment of a static website hosted on Amazon S3. It creates an S3 bucket, configures it to serve static website content, uploads HTML files to the bucket, applies a bucket policy for public read access, and outputs the website endpoint.

## Requirements

- **AWS Credentials**: Valid AWS credentials with appropriate permissions are required to deploy resources using Terraform in AWS. Ensure that you have configured your AWS credentials properly before running Terraform commands. For more information on configuring AWS credentials, refer to the [AWS documentation](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html).

- **Visual Studio Code (Optional)**: While not strictly necessary, using an integrated development environment (IDE) like Visual Studio Code (VSCode) can enhance the development experience for Terraform projects. VSCode offers features like syntax highlighting, code completion, and integrated terminal support, which can streamline Terraform development. If you choose to use VSCode, ensure that it is installed on your system and properly configured for Terraform development.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.42.0 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.6.0 |

## Modules

This project does not utilize any external modules.

## Resources

| Name                                            | Type                            |
| ----------------------------------------------- | ------------------------------- |
| `aws_s3_bucket.bucket`                         | AWS S3 Bucket                   |
| `aws_s3_bucket_website_configuration.blog`     | AWS S3 Bucket Website           |
| `aws_s3_bucket_public_access_block.public_access_block` | AWS S3 Bucket Public Access Block |
| `aws_s3_object.upload_object`                  | AWS S3 Object                   |
| `aws_s3_bucket_policy.read_access_policy`      | AWS S3 Bucket Policy            |
| `random_string.random`                         | Random String                   |

## Inputs

This project does not require any inputs.

## Outputs

| Name           | Description           |
| -------------- | --------------------- |
| `s3_bucket_id` | S3 Bucket Website URL |

## Usage

To deploy the static website using Terraform, follow these steps:

1. **Clone the Repository**: Clone this repository to your local machine.

    ```bash
    git clone <repository-url>
    ```

2. **Change Directory**: Navigate to the cloned repository directory.

    ```bash
    cd S3_static-website
    ```
Cloning the repository and navigating to the cloned directory is necessary if you want to work with your Terraform project locally. Cloning the repository allows users to have a local copy of the project on their machine, and changing the directory ensures that they are in the correct location to run Terraform commands and manage the project files.

3. **Initialize Terraform**: Initialize Terraform in the project directory.

    ```bash
    terraform init
    ```

4. **Review Terraform Plan**: Optionally, review the Terraform execution plan to ensure that the correct resources will be created.

    ```bash
    terraform plan
    ```

5. **Apply Terraform Changes**: Apply the Terraform configuration to create the resources.

    ```bash
    terraform apply
    ```

6. **Access the Website**: Once the deployment is complete, access the static website using the provided website URL.
