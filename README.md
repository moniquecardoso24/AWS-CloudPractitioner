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
### VPCs
![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/1457804a-8bbb-4a04-a90b-c2d5d6d44300)

### Subnets
![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/167d2d6e-7708-4bc1-8a35-08602cb1c8db)

### Internet Gatweays and Routes
Internet Gateways enables resources in public subnets to connect to the internet if it has a public IPv4 or IPv6 adress.
Route tables contains a set of rules, that determine where network traffic from your subnet or gateway is directed.

In this print, the first route is the internet gateway, that provides external access for resources within any subnets that are attached to this table. Second is for all local traffic.

![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/711c5320-adcd-46e3-a080-0dc7a030f38c)

### Network access control list (ACL)

"A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets." 
Source: https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html

Network ACls is are stateless because when a resource in VPC connects to another one, traffic in both directions must have a rule to allow it.

![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/49b0b1ad-c3cc-4099-83ff-0ca30601f716)

There are 2 rules in this print. The first allows access to IG and then out to the internet. Any subnet associated with this route will become a public subnet.

![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/557d6fd4-f47c-44f9-8dcc-94df714ebb26)

### Security Groups

Security groups also controls access for inbound and outbound traffic. It is stateful because when a resource in your security group makes a connection to another resource, any reply traffic is automatically allowed.

![image](https://github.com/moniquecardoso24/AWS-CloudPractitioner/assets/118371689/0d473706-b285-478c-97b2-f52297d7cd3b)
