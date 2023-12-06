# AWS
INTRODUCTION TO CLOUD COMPUTING (AWS)

## CLOUD COMPUTING ##
Delivey of computing services or storing, managing and accessing the data and programs on the remote servers

- ### Benefits of cloud computing ###
   - faster time to market
   - scalability and flexibility
   - cost savings
   - advanced security
   - on time delivery
- ### Public cloud vs Private cloud ###

  ![Screenshot 2023-12-05 175531](https://github.com/Mragankk/AWS/assets/145200189/0d15eb68-03ec-4587-865c-7aac09a19daf)

  ![Screenshot 2023-12-05 175809](https://github.com/Mragankk/AWS/assets/145200189/c818a1a8-6683-40e3-870d-bc33fb643e8b)

- ### Hybrid cloud ###
   - Both public and private cloud
   - shared security responsiblity
- ### Cloud service model ###
  1. **IAAS**- Infrastructure as a service
  2. **PAAS**- Platform as a service
  3. **SAAS**- Software as a seervice

    ![Screenshot 2023-12-05 181044](https://github.com/Mragankk/AWS/assets/145200189/7323c83a-9e3e-47bb-8f8d-88dadee53af4)


# AWS( AMAZON WEB SERVICES)
A cloud computing platform that offers on-demand computing services such as virtual servers and storage that can be used to build and run applications and websites

- ### Compute services ###
  -**EC2**- Elastic Compute cloud
  
  -**ECS(Elastic conatiner services)/EKS** for conatiner services
 
   -**lambda**- serverless (serverless means cloud provider dynamically manages the allocation of machine resources)

    -**Fargate**- a serverless, pay-as-you-go compute engine p that allows you to run containers without having to manage servers or clusters. it is compatible with both ECS and EKS.

   ![Screenshot 2023-12-05 194851](https://github.com/Mragankk/AWS/assets/145200189/d07a0a13-b046-4ce8-bf87-105f451b6c0a)
- ### Storage Services ###
   - **S3** Simple storage service
   - **EBS**Elastic Block store
   - **EFS**elastic file system
   - **glacier** Archival storage (cheapest storage service with no instant data pickup)

    ![Screenshot 2023-12-05 195007](https://github.com/Mragankk/AWS/assets/145200189/dbb7a28f-ab08-4d08-b2cb-262534ed794e)

- ### Network services ###
   - **VPC**- Virtual Priavte Cloud
   - **Route 53**- Domain name service
   - **Direct connect**
     
     ![Screenshot 2023-12-05 210522](https://github.com/Mragankk/AWS/assets/145200189/5c698ccc-ae0c-425b-a499-a2d2fd359044)




# S3 #
- **Security**
  - user based- IAM policies
  - resource based
     - bucket policies
     - bucket ACLs
     - Object ACLs
- **Public vs private accessible Buckets**
- **Object versioning**
- **State of the art in transit and at rest encryption**
- **Infinitely scaling stoerage**
- **buckets**
- **Gloabally unique bucket names**
- **object storage with durability of 11 9's, 99.999999999%**

   ![Screenshot 2023-12-05 211654](https://github.com/Mragankk/AWS/assets/145200189/ddfe6e25-ea01-4489-9094-821c140f0ebd)
- **Storage classes**
   - amazon S3 standard- General purpose (cheaper than  buying  a pen drive)
   - amazon S3 standard- infrequent Access(IA)
   - amazon S3 Glacier Instant Retrieval (pick up data less frequently)
   - amazon S3 glacier flexible Retrieval ( pick up data more frequently)
   - amazon S3 Galcier deep archive ( rarely pickup data)
   - amazon S3 glacier Intelligent tiering (old data automatically deleted)

# EC2 #
- **most popular AWS Offering**
- **IAAS**
- **provide rented virtual machine**
- **it uses EBS and instance store to store data** ( in intstnaces if EC2 shut down then data will be lost)
- **it uses ELB to distribute data**
- **uses autoscaling for scaling purpose**

  ## EC2 insance type ##
  - m type (balanced RAM and CPU, used for general purpose)
  - c type (provides CPU intensive)
  - t type (provides burst capabilities)
  - r type (provides RAM)
  - i type (provides IOPS)
- Establishes balance between
   - compute
   - memory
   - networking
 
    ![Screenshot 2023-12-06 124138](https://github.com/Mragankk/AWS/assets/145200189/193cffe7-3d14-4e6f-a94c-98824bb994cd) ![Screenshot 2023-12-06 124152](https://github.com/Mragankk/AWS/assets/145200189/df7ff25c-2021-4b26-9f33-e5f5b0a8b33b)

- **security groups and instances own firewall**
- **several ports**
   - 21-FTP
   - 22-SSH
   - 23-Telnet
   - 53-DNS
   - 80-HTTP
   - 443-HTTPS
   - 3306-MYSQL
   - 3389-RDP
  - **On-demand Instances**- short workload, predictable pricing, pay by second
  - **Reserved**( ex- 1 to 3 years)- make a commitment of using service and ask for discount( about 72% of biling can be saved)
  - **Spot Instances**- short workload, cheap,can lose instances(less reliable)
  - **Dedicated hosts**- book an entire physical server, control instances placement, most expensive EC2
  - **Dedsicated Instances**- no other custoemrs will share your hardware

#  ELB #
- **implementation of horizontal scaling**
- **Required for high availablity**
- **TYPES OF LOAD BALANCER**
   - Classic load balancer- layer 4 & 7
   - Application Load balancer- layer 7
   - Network load balancer- Layer 4
 
     ![Screenshot 2023-12-06 232124](https://github.com/Mragankk/OOPS/assets/145200189/052b09d9-bf48-40de-b670-f31d935542f1)
     


