https://registry.terraform.io/providers/hashicorp/aws/latest/docs

# Authentication
need to set the following in the env when running terraform apply 
 AWS_ACCESS_KEY_ID="anaccesskey"
 AWS_SECRET_ACCESS_KEY="asecretkey"
# Or
  shared_config_files      = ["/some_Dir/.aws/conf"]
  shared_credentials_files = ["/some_Dir/.aws/creds"]
  profile                  = "customprofile"

 
# Required Output
 
 terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 3.0"
    }
  }
}

#Configure the AWS Provider
provider "aws" {
  region = "us-east-1",
#optionally
  shared_config_files      = ["/some_Dir/.aws/conf"]
  shared_credentials_files = ["/some_Dir/.aws/creds"]
  profile                  = "customprofile"
}


# Note 
 can set the region with AWS_REGION="us-west-2"