# HighlyAvailableWebApp
AWS workshop
https://catalog.us-east-1.prod.workshops.aws/v2/workshops/3de93ad5-ebbe-4258-b977-b45cdfe661f1/en-US/introduction

# Overview
Web applications typically need to scale continuously in response to the number of users on the platform and to be available in a highly available manner. In being highly available an application needs to be able to operate in multiple data centers and continue to function as components, servers, or even data centers fail.

In this series of labs you will create a highly available, scalable deployment of the Wordpress web application . You will deploy the Wordpress application in such a way that the application server, database, and file server can scale independently of one another. You will also deploy the application's components into two availability zones to distribute it and guard against failure of any one availability zone. The Wordpress application will be deployed in a stateless fashion so that we can add or remove web application servers in response to the requests flowing into the system.

To create this scalable, HA web application you will use various AWS services in a series to create an architecture similar to the full scale reference architecture linked below. You will first create a virtual network spread across multiple availability zones in your region of choice. You will then deploy a highly available relational database across those availability zones using Amazon RDS . With your database deployed the next step will be to create a database caching layer using Amazon ElastiCache . This will provide you with a cache around your database for frequently run queries, improving HTTP response time performance and reducing strain on your RDBMS. With the data tier created you will then begin to create the application tier. You will provision a shared storage layer powered by NFS. Using Amazon EFS  you will create an NFS cluster across multiple availability zones. Then you will create a load-balanced group of web servers  that will automatically scale in response to load to complete your application tier.

These labs are based upon the materials developed as a reference architecture by AWS. The reference architecture is available as a GitHub repository .
https://github.com/aws-samples/aws-refarch-wordpress
