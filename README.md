# AWS-CloudPractitioner
Sharing My Learning 


## Creating a VPC
 VPC is a Virtual Private Cloud where you can launch AWS resources in a virtual network, such as Amazon EC2 instances. You can configure your VPC by modifying its IP adress range, configure route tables, create subnets, network gateways and security groups. Remembering that VPC is a regional service.

### VPC
 ![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/cf209d41-20af-48a5-a7bc-79b1be886293)

### Creating a VPC
The print shows 4 subnets, because the tool will automatically select Availability Zones(Azs) from the region the VPC is being created in. In this case: US West (Oregan)
 ![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/7ba66170-1e74-4e34-accd-08fbe4c0186c)

 "A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances." Source: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
 
 "The DNS hostnames attribute determines whether instances launched in the VPC receive public DNS hostnames that correspond to their public IP addresses. The DNS resolution attribute determines whether DNS resolution through the Amazon DNS server is supported for the VPC." Source: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-dns.html
