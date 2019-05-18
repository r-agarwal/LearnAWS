# How to use the S3 command-line tool (Mac OSX/Linux)

Install the AWS CLI on macOS : 
Follow the instructions in the AWS Documentation 
https://docs.aws.amazon.com/cli/latest/userguide/install-macos.html

Configuring the CLI Tool: 
Follow the instructions in the AWS Documentation 
https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html


Using the CLI Tool for S3 Operations:

List S3 Buckets in AWS account:
> aws s3 ls
```
Rahuls-MacBook-Pro:.aws rahulagarwal$ aws s3 ls
2019-05-17 12:54:20 rahul54781-devuser1-bucket1
```
List an S3 bucket directory :
> aws s3 ls s3://bucket-name/path/to/file

```
Rahuls-MacBook-Pro:.aws rahulagarwal$ aws s3 ls s3://rahul54781-devuser1-bucket1/images/
2019-05-17 12:54:52          0 
2019-05-17 12:57:55      49128 photo1.jpg
```
Tip: Add the --human-readable flag to the end of your command to get more human-readable sizes
Command
aws s3 ls s3://bucket-name/path/to/file --human-readable

```
Rahuls-MacBook-Pro:.aws rahulagarwal$ aws s3 ls s3://rahul54781-devuser1-bucket1/images/ --human-readable
2019-05-17 12:54:52    0 Bytes 
2019-05-17 12:57:55   48.0 KiB photo1.jpg
```


Download a file from S3 bucket:
> aws s3 cp s3://bucket-name/path/of/object ~/Downloads

The object / File will be saved to the Downloads folder

Remove a file from S3 bucket:
> aws s3 rm s3://bucket-name/path/of/object

Upload a file to S3 bucket
> aws s3 cp ~/Downloads/file1.txt s3://bucket-name/path/to/destination --acl public-read

For canned ACL options, Please refer AWS Documentation below:
https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl