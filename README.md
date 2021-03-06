# OpenCravat CloudFormation Pipeline
This project is a Cloudformation template for an automated AWS pipeline to run the OpenCravat software. This pipeline will take two input files and return all pertinent results to your selected s3 bucket.

What you'll need to get started:
- A configured AWS account with permissions to create EC2, S3, CF, and IAM Resources
- An existing s3 bucket to which you have write permissions
- At least one configured EC2 keypair inside of your AWS account
- Within that bucket should be an input file and a YAML file for OpenCravat configuration parameters
- Important note : this pipeline will incur cost on your amazon account and you are responsible for ensuring all components are deleted

To get started, click this link: [CloudFormation Quick Start](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/template?stackName=OpenCravatRunner-v2&templateURL=http://haplocravat2-testing.s3.amazonaws.com/oc-cf-template.yml)

At this first screen, you'll only need to confirm with the "Next" button. The template selection and file locations have been processed with the link.

![First Screen](https://github.com/hynesgra/OC-cloudform/blob/master/images/FirstScreen.png)

The second screen is where you will provide all necessary values for the pipeline run. The ImageID and machine type values will already be populated from default, but the rest will require completion. The InputFile and OCYMLFile values should be the names of files within your S3 bucket. 

If your files are nested in a within a "directory", that should be included in your OCS3Bucket values  "bucket-name/folder-name" 

If you don't see any values for keypairs, follow these instructions: [EC2 Keypair Generation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair)

If you don't have an s3 bucket configured, follow these instructions: [S3 Bucket Creation](https://docs.aws.amazon.com/AmazonS3/latest/gsg/CreatingABucket.html)

Your SubnetId and VpcId will not match these values.


![Second Screen](https://github.com/hynesgra/OC-cloudform/blob/master/images/SecondScreen.png)

On the third screen you won't need to modify any values and should just click "Next"

![Third Screen](https://github.com/hynesgra/OC-cloudform/blob/master/images/ThirdScreen.png)

The fourth screen submits the OpenCravat runner. You'll only need to confirm the objects and permissions being granted in the CloudFormation process. Finally just click the "Create Stack" buttong to get your pipeline working.

![Fourth Screen](https://github.com/hynesgra/OC-cloudform/blob/master/images/FourthScreen.png)

