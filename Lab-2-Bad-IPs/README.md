# sans-ip-block-waf

M.Chambers 2016

Please understand that I do not support this code, and neither does anyone else. Sorry.

You should never install anything in an AWS account that is not supported (i.e. written and support by you, verified and supported by you, or under a 3rd party support arrangement).  To verify a 'thing' you could absolutely install it in an isolated test environment, but even then under a watchful eye, especially if the 'thing' is going to incur costs.

## aCloud.Guru

This file was created for the purposes of the Event Based Security course from aCloud.Guru

## What is it?
An Example AWS CloudFormation template that creates an AWS WAF ACL which blocks traffic from IPs contained within the
Recommended Block List published by DShield.org via The SANS Technology Institute.

## What is created?
The main objects created by this template are:
- AWS WAF ACL, Rule and Conditions (IPSet)
- Lambda function

## What does it do?
This template helps setup a WAF ACL to block IPs listed on the Bad IP list.  It also sets up a Lambda function
to help keep the WAF up-to-date with the current SANS list.   

## How to use
Create a stack using the template.  Everything, including the Lambda function is included.   

After creating a stack you can manually initiate an update by performing a test run on the Lambda function.  Hoever the updates are scheduled for
once an hour.

You will need an AWS CloudFront distribution 'in front' of your website that you can configure to work with an WAF ACL.

##IMPORTANT
These files are distributed on an AS IS BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
