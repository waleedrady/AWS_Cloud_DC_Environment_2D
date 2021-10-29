# DataCenter Enviroment 2D

Source Code for this Module (https://github.com/WEEMR/terraform-aws-DataCenter_Enviroment_2D)

Terraform Registery         (https://registry.terraform.io/modules/WEEMR/DataCenter_Enviroment_2D/aws/latest)

The module will create the below resources:

- 2 x VPCs, one of Hub and one for Spoke
- Networking Stack (VPC, Subnets, Route Tables, Security Groups and Internet Gateway) - Please refer to the diagram below.
- 2 x FortiGate with 3 interfaces (Two Interfaces in two different Public Subnets and one in the Private subnets)
- Windows Server 2019 Behind the FGT Port 3 [LAN]
- Ubunutu Server with Apache installed, iperf, fzf, pydf, firefox, lynx and elinks installed on it behind the FGT port 3 [LAN]
- Route53 DNS Public Hosted Zones
- FortiManager, FortiAnalyzer and FortiAuthenticator will be deployed as well behind the Hub FGT on Port 3 [LAN]
- VPC Flow Logs


![image](https://user-images.githubusercontent.com/83562796/139353367-5b9839bd-40db-46b5-be5b-3bcc1fb2c290.png)


// The DNS Hosted Zones must be sub-zones for a domain that is registered or managed by AWS Route53 //

// i.e xyz.com is the domain name and you will create the subzone Lab1.xyz.com // 

![image](https://user-images.githubusercontent.com/83562796/139353508-06b049a1-a48c-4785-8689-48a4e273465c.png)
