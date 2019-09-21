# AWS-Cloud-Practitioner-Notes-Prueba
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
 
 #### Elastic Load Balancing & Auto Scaling 
Enables to manage the consuption of your resources.3 types of ELB:
* Network load Balancer
  -Useful for routing target to your VPC 
  - Used for ultra-high performance for your aplication 
  - Operates at the connection (Transport) level
  -Low latencies
* Aplication Load Balancer
 -Feature set for your web applications with HTTp and HTTPS traffic
 -operates at the request (aplication) level
* Classic Load Balancer
 -Used when you have an existing application running in the EC2-Classic enviroment
 -Operates at the connection(transport) and the request (application) level
 
 #### Setting up and ELB
 1. Define Load Balancer(define internal or external LB)
 2. Assign SG
 3. Configure SG
 4. Configure Health checks
 5. add EC2 Instances
 6. Add tags
 
 #### Auto Scaling
Is a mechanism that automatically allows you to increase or decrease resources depending on demand.

### Elastic Beanstalk

Is a managed services to help you deploy web aplications:
* Perfect for engineers unfamiliar with AWS
* Simple,effective and a quick solution 
* Free to use,charging only for resources

#### AWS Elastic Beanstal Architechture

* Applications:
 * A collection of different elements susch as enviroments,enviroments configurations,aplication versions
* Application versions:
 * Specific reference to a section of deployable code
* Eviroment
 * An enviroment refers to an application version deployed on AWS resources
 * Enviroment configuration
  * a collection of parameters that dictate the resources behavior within enviroment.
* Configuration Template
 * a baseline for creating a new template.
 
 ### AWS LAMBDA
 Lambda allows you to run your own code in response to events in a serverles enviroment.
 


### Architecture Fundamentals of AWS 

#### AWS global Infrastructure

*Availability zones (AZ's)
  - refered to AZ's
  - DataCenters of AWS
  - A single AZ can be comprised of multiple individual datacenters
  - Each AZ is separeted from other AZ's
*Regions
  - Collection of AZ's that are geographically close to one another
  - Regions act independently of each other
  - Every region contains at least 2 AZ's
  - Most services within AWS are region specific
* Edge Locations 
  - used by AWS cloudfront & lambda to cache data and reduces latency
  - primary used tu lower latency
* Regional Edge Caches
  -A regional edge cache sits between yout cloudfront origin servers and the edge locations
  -They have larger cache-with than a edge location
  - Reduced latency
 
#### Disaster recovery 

**RTO**
Is the time it takes after a disruption to restore a businees process yo its operational level
**RPO**
Is the acceptable amount of data loss measured in time 

**Different scenarios for DR**

**Back up and restore**
data is store as a virtual tape library,using AWS storage gateway
**Pilot Light**
Data is mirror and the enviroment is script as a template(AMI's) that can scale in case of a disater
**Warm StandBy**
All key services running with the smallest possible impact
**Multi-site**
you duplicate your production enviorment(thats on-premise) in AWS

#### Well Architechted FrameWork

**5 Pillars**
* Operational Excellence 
  * running and monitoring system to help optimize and deliver value to the business
* Cost Optimization 
* Security
* Performance efffiency 
* Reliability


