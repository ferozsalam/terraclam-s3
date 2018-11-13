# terraform-s3-clamav

## What is this?

This is a Terraform module that allows antivirus scanning of S3 buckets 
on object creation.

Pretty rough-and-ready, but does the job.

The code and architecture of the resulting AWS infrastructure is the work of
[Upside Travel](https://github.com/upsidetravel/bucket-antivirus-function). The
library build was created in November 2018. This is simply a wrapper to ease
the provisioning of this service, removing the need to manually click on
buttons in the AWS console.

See the Upside Travel documentation for more information regarding how the
system works.

Clamav definitions are updated every three hours.

The major current limitation is that it only works with a single folder. I do
have plans to modify the system so that it can watch multiple folders in
the future.

This is the result of two days of learning Terraform and two weeks of
playing with AWS, so I welcome any pull requests, especially if they make 
my configuration files more idiomatic.