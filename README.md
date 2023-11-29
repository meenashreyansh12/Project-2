VPC Peering between two VPCs
Created two VPCs with names Prod1 and Prod2
Enabling hostnames, as if you've multiple VPCs connected it allows resources in different VPCs to refer to each other using DNS hostnames.
Created two subnets for each VPC respectively
Enabled internet access for instances in the associated subnet as it allows instances in the associated subnet to send outbound traffic to the internet and receive inbound traffic from the internet.
We then update the route table associated with the subnet, to include a route to the Internet Gateway (usually with the destination 0.0.0.0/0). This route directs traffic destined for the internet to the Internet Gateway.
While creating subnet groups, when we configure a Multi-Availability Zone (Multi-AZ) deployment, we need to specify a subnet group with subnets in different Availability Zones to ensure that if one Availability Zone becomes unavailable, your application can still access the database in another Availability Zone. Also when we've a mix of public and private subnets within your VPC, subnet groups help you define which subnets your resources 
Created two databases with names database1 and database2 as we need to establish secure and private communication between databases located in different VPCs. While creating databases its important to plan and configure the peering connections, routing tables, and security groups to ensure that the communication is secure
