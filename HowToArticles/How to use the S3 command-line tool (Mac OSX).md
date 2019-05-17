# How to use the S3 command-line tool (Mac OSX/Linux)

Install the AWS CLI on macOS : 
Follow the instructions in the AWS Documentation 
https://docs.aws.amazon.com/cli/latest/userguide/install-macos.html

Configuring the CLI Tool: 
Follow the instructions in the AWS Documentation 
https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html


Using the CLI Tool for S3 Operations:

List S3 Buckets in AWS account:
> aw s3 ls

Output:
Rahuls-MacBook-Pro:.aws rahulagarwal$ aws s3 ls
2019-05-17 12:54:20 rahul54781-devuser1-bucket1


Download a file from S3 bucket:
> aws s3 cp s3://bucket-name/path/of/object ~/Downloads

The object / File will be saved to the Downloads folder

Remove a file from S3 bucket:
> aws s3 rm s3://bucket-name/path/of/object

Upload a file to S3 bucket
> aws s3 cp ~/Downloads/file1.txt s3://bucket-name/path/to/destination --acl public-read

Various acl options: 
private
pubic-read
public-read-write
authenticated-read
authenticated-owner-read