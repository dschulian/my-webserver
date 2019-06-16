Demonstrates how to create a simple system on the Amazon Web Services Platform.

### Summary
The CloudFormation template creates an EC2 instance in a custom security group with an Amazon Linux 2 AMI in us-west-1 region. An EBS volume - based on a given snapshot with website content - is being attached. EC2's Userdata is used to install docker and host website content data in a containerized nginx webserver using a custom ```Dockerfile```.

### Steps to manage the stack
* Create stack:
```console
aws cloudformation create-stack --stack-name my-webserver --template-body file://my-webserver.yaml --parameter ParameterKey=KeyPairName,ParameterValue=my-key
```

* Delete stack:
```console
aws cloudformation delete-stack --stack-name my-webserver
```
