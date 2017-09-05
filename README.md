# Track Terraform

In this repo are a couple of helper scripts used to help trace which services terraform commands are utilising to spin up and spin down infrastructure.

## THIS IS JUST A TOY

This is a toy project still in develop which MAY prove useful; testing is required

## Usage

Remove any cached data in the .terraform directory to ensure that all permissions are captured in the output.

Output from terraform is tracked in the `/tmp/terraform.{{unix-time}}.log` file
NOTE: These scripts will set the TF_LOG_PATH and TF_LOG environment variables. More information about terraform environment variables [here](https://www.terraform.io/docs/configuration/environment-variables.html)

* run ./track-terraform init to get source file to set environment variables
* run ./track-terraform clear to clear the terraform data logged to the existing log file
* run ./track-terraform get-params to get the services accessed by terraform logged to the current log file
* run ./track-terraform destory to get the source file to unset environment variables and rm the log file
