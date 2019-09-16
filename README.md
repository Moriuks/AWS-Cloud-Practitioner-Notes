# AWS-Cloud-Practitioner-Notes
Notes for my first AWS certification.Cloud practitioner,intended for individuals who have the knowledge and skills necessary to effectively demonstrate an overall understanding of the AWS Cloud

## Overview


### What is Compute in AWS?

* The brains and processing power required by applications and systems(CPU,RAM)
* Compute in AWS could be EC2 instances or Lambda functions
* ELB and Auto Scaling allow control and manage the amount of compute resources used by services.


 ### Elastic Compute Cloud EC2
 
 * Most Common services in AWS
 * Allows to deploy virtual services
 
#### EC2 Elements
* Amazon Machine Images(AMI)
* Instance Types 
* Instance Purchasing options
* Tenancy
* User Data
* Storage Options
* Security

#### Amazon Machine Images(AMI)
Templates of pre-configures EC2 Instances,it includes OS,aplications along with any custom configuration,you can make your own or buy one from the AMI's marketplace 

#### Instance Types
Defines the size of an instance from a CPU,Memory,Storage and networking perspective.They are categorized in family types depending on your application needs and can be summarized as:

1. General Purpose
 -Balance of CPU,memory and storage 
 -Ideal for small and medium applications
2. Compute Optimized 
 -Higher perfomance on compute
 -High performance front-end,web servers and science applications
3. GPU
 -Optimized for grapihc intensive applications
4. Memory Optimized 
 -Used for large-scale,enterprise-class,in-memory applications(SAP Hana)
5. Storage Optimized 
 -SSD backed instance storage for low latency
 -High I/O performance
 -analitic worloads
 -Data filesystems and NoSQL databases
 
#### Instances Purchasing Options 
different payment options:

* On-Demand Instances
* Reserved Instances
* Spot Instances
* Dedicated Instances
* Dedicated Host

* On-Demand Instances
 -can be launched at any time
 -Can be used for as long as needed
 -Used for irregular uninteruptable used
 -Charged by the hour
 -best for testing and development enviroment
* Reserved Instances
 -Purchased for a set period of time for a reduced cost (up to 70%)
 -diferent ypes of reservations
  -All Upfront: Complete payment for 1 or 3 years time frame
  -Partial Upfront: Smaller upfront payment for smaller discount
  -No Upfront: The smallest discount is applied
 -Best applied for long term ,predictable workloads
* Spot Instances
 -Bid for unused EC2 Compute resources
 -No guarentee of having the resource for fixed period of time
 -Fluctuation of prices based on supply and demand
 -Bid for larges EC2 instances at a very low price
 -Useful for processsing data that can be suddenly interrupted like
 -Batch jobs and backgrounf processing  

#### EC2 Tanancy
Tenancy relates to underlying hosting of your EC2 Instances

**Shared** 
- EC2 instances are launched on any available host with the required resources
-The same host may be used by multiple customers
**Dedicated Instances**
-Instances hosted on hardware that no other customer can access
-May be required to meet compliance
-Incur additional instances

**Dedicated Host**
-Additional visibility and control of the physical host
-Allows you to use the same host for a number of your instances
-May be requiere to meet compliance

#### Storage options 
it can be clasified in two categories:
* Persisten Storage 
 -EBS are considered network attached devices
 -similar like a hard-drive
 -EBS volumes are physically separeted from EC2 instance

* Ephemeral storage
 -Instance back storage
 -similar to laptop's internal hard disk
 -they are physically attached to the host
 -whe intance is stoped ...the info is lost

#### Security
 -security is a firewall for you instance
 -some restrictions are:
   -Source and destiniations
   -Inbound and outbound rules
   -Ports and protocols usage
 
 
 

