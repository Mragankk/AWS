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
 
    ![Screenshot 2023-12-08 090735](https://github.com/Mragankk/AWS/assets/145200189/59af4c07-f0e9-4ee0-be8d-8e848cd66be2)

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
 
   - **Apache web server works on layer 7 , using single apache server one can deploy multiple applications on different ports based on paths (URLbased) (virtual hosts) . virtual hosting can only work on layer 7**
## AUTOSCALING ##
 
   ![Screenshot 2023-12-06 232124](https://github.com/Mragankk/OOPS/assets/145200189/052b09d9-bf48-40de-b670-f31d935542f1)
     

- **public subnet** : can receive traffic from outerworld
- **private subnet** : cannot receive traffic from outerworld but may or may not send traffic to outerworld

## Application Based LOAD BALANCER ##
- **key pair** : kind of like a password (public key is username; private key is password)
  - PPK (PuTTY Private Key) and PEM (Privacy Enhanced Mail) are two file formats that are commonly used for SSH and SSL/TLS connections. While PPK files are primarily used with PuTTY on Windows, PEM files are more widely supported and can be used with various tools and platforms
- **security groups** : A security group controls the traffic that is allowed to reach and leave the resources that it is associated with. For example, after you associate a security group with an EC2 instance, it controls the inbound and outbound traffic for the instance. When you create a VPC, it comes with a default security group. (acts as a firewall)

   ![Screenshot 2023-12-07 184851](https://github.com/Mragankk/AWS/assets/145200189/de0eb6f3-70b6-4391-a09e-4b6e4ce3fee8)

   ![Screenshot 2023-12-07 184941](https://github.com/Mragankk/AWS/assets/145200189/f5965d42-6b05-4b25-812f-d32beeaea53a)

   ![Screenshot 2023-12-07 184956](https://github.com/Mragankk/AWS/assets/145200189/62a97191-15c9-4778-800b-46fb1bc34404)

### Creating a target group ###
- Your load balancer routes requests to the targets in a target group and performs health checks on the targets.
- LB routes traffic to target group then traffic group routes traffic to the back end ec2 instances or IP addresses etc.

  
![Screenshot 2023-12-07 185638](https://github.com/Mragankk/AWS/assets/145200189/f2f8780b-ec05-4f42-bce3-21e112cfb719)


![Screenshot 2023-12-07 190556](https://github.com/Mragankk/AWS/assets/145200189/94a6b398-cf6f-455e-a2e9-36eabe98f5db)
![Screenshot 2023-12-07 192558](https://github.com/Mragankk/AWS/assets/145200189/51c28e46-bd83-4e8a-b2b8-a8b9a47811da)
![Screenshot 2023-12-07 190835](https://github.com/Mragankk/AWS/assets/145200189/c8f2ea8c-6d65-4f4d-be7f-751a7c64a912)

### CREATING LAUCNCH TEMPLATE
  
![Screenshot 2023-12-07 193713](https://github.com/Mragankk/AWS/assets/145200189/fddbcd3b-cdbc-4288-a264-a24a2f3e7bba)
![Screenshot 2023-12-07 193722](https://github.com/Mragankk/AWS/assets/145200189/b86163e1-c0fe-4295-ae18-bd2602092417)
![Screenshot 2023-12-07 193731](https://github.com/Mragankk/AWS/assets/145200189/113e8e8e-2425-4c5f-aa2e-3d69b0cbdf07)
![Screenshot 2023-12-07 193741](https://github.com/Mragankk/AWS/assets/145200189/e09b407a-ec71-4ec6-808b-ab002094b0ed)
![Screenshot 2023-12-07 193749](https://github.com/Mragankk/AWS/assets/145200189/426ddbf5-cb2c-49ba-9046-b13d91b3bf7f)
![Screenshot 2023-12-07 193759](https://github.com/Mragankk/AWS/assets/145200189/5b009e73-0488-4665-a8db-d13db321843c)
![Screenshot 2023-12-07 193807](https://github.com/Mragankk/AWS/assets/145200189/d11757da-fcb1-4d89-a340-543ce6e5aa20)

### CREATING SCALING POLICIES
  
![Screenshot 2023-12-07 194442](https://github.com/Mragankk/AWS/assets/145200189/013fc0bc-d104-449e-8cf7-7dbc853204ff)
![Screenshot 2023-12-07 194450](https://github.com/Mragankk/AWS/assets/145200189/27e15f0b-f20f-47ed-bcc2-c3a98a8da585)

### ARTIFICIAL LOAD
```
htop
```

![Screenshot 2023-12-07 194921](https://github.com/Mragankk/AWS/assets/145200189/65f581b3-77d4-480e-84e8-07fedc7c6a11)

- currently 0

- making instance count to a high number
```
seq 999999999999999999999 > /dev/null &
```


![Screenshot 2023-12-07 195155](https://github.com/Mragankk/AWS/assets/145200189/f14ce79c-4c28-4cca-bb5d-ca97d41b7278)
![Screenshot 2023-12-07 195203](https://github.com/Mragankk/AWS/assets/145200189/f22fa763-6aba-4957-9c33-c9d405890512)
![Screenshot 2023-12-07 195211](https://github.com/Mragankk/AWS/assets/145200189/49e69834-feee-487a-b133-69f8d36881af)

- going to the DNS name and reloading will take you to diff targets(3)
- this is **round robin** at work  

## AWS CLI : The AWS Command Line Interface (AWS CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.
- BOTO library in python

![Screenshot from 2023-11-27 16-45-38](https://github.com/KRIISHSHARMA/AWS/assets/86760658/fae33c2d-6122-4ee2-aa75-5f061bcbba20)
![Screenshot from 2023-11-27 16-47-42](https://github.com/KRIISHSHARMA/AWS/assets/86760658/768d5a91-8c74-42ed-b08e-14c3ad5c11eb)

``` bash
sudo snap install aws-cli
```
``` bash
aws configure
```
![Screenshot from 2023-11-27 17-08-27](https://github.com/KRIISHSHARMA/AWS/assets/86760658/71a8036d-299a-4b48-adbb-8049b3f16dea)

- in security credentials , before creating access key copy and paste PU , PrK and fill location and format in terminal 
- give user access

![Screenshot from 2023-11-27 17-30-18](https://github.com/KRIISHSHARMA/AWS/assets/86760658/50c16ed9-0a30-49a2-b9aa-d834c2622e99)

![Screenshot from 2023-11-27 17-31-17](https://github.com/KRIISHSHARMA/AWS/assets/86760658/a7ce2566-0cbb-4b6e-8412-106c939a0f81)
![Screenshot from 2023-11-27 17-31-32](https://github.com/KRIISHSHARMA/AWS/assets/86760658/cb651886-272d-4b28-94de-25785de9fcab)

- after creating instance
``` bash
aws ec2 describe-instances
``` 

![Screenshot from 2023-11-27 17-35-01](https://github.com/KRIISHSHARMA/AWS/assets/86760658/e4ba62f0-42f5-4e8d-840f-41d32e1cf6a3)
![Screenshot from 2023-11-27 17-35-01](https://github.com/KRIISHSHARMA/AWS/assets/86760658/de7fef08-39e8-4525-a276-6da3f8c2e742)
![Screenshot from 2023-11-27 17-46-10](https://github.com/KRIISHSHARMA/AWS/assets/86760658/15f77e24-064b-4aca-9de0-562c6a54c890)
![Screenshot from 2023-11-27 18-12-04](https://github.com/KRIISHSHARMA/AWS/assets/86760658/1cf4f02a-59c8-43d9-896f-28d980add612)
![Screenshot from 2023-11-27 18-12-32](https://github.com/KRIISHSHARMA/AWS/assets/86760658/6e9a8d71-0ede-42fd-9c93-3a53a2e109a0)
![Screenshot from 2023-11-27 18-14-02](https://github.com/KRIISHSHARMA/AWS/assets/86760658/899d441d-7208-4778-8537-6be1a92008d0)
![Screenshot from 2023-11-27 18-17-35](https://github.com/KRIISHSHARMA/AWS/assets/86760658/89a6f2f4-a014-4ec6-91fe-4994d0e26d40)
![Screenshot from 2023-11-27 18-26-06](https://github.com/KRIISHSHARMA/AWS/assets/86760658/4789776e-d9e7-4a27-8c3d-038298c02daf)


- docker image to create art load
- pods : Pods are the smallest deployable units of computing that you can create and manage in Kubernetes. A Pod (as in a pod of whales or pea pod) is a group of one or more containers, with shared storage and network resources, and a specification for how to run the containers.

 ![download](https://github.com/KRIISHSHARMA/AWS/assets/86760658/1bf8d1eb-e0b6-4674-bd98-fbcf383135d3)

- daemon sets : works on nodes where pods are running , can manage all your agents eg if we are runninf 5 ec2 instances behind the k8s cluster then we can run 1 daemon set and that daemon set wil take care of all the agents 

## CLOUD 9
- cloud based IDE (vscode , pycharm etc)
- provides IDE on browsers

![Screenshot from 2023-12-02 16-01-33](https://github.com/KRIISHSHARMA/AWS/assets/86760658/9208cded-f435-451a-a192-c4a254244e75)
![Screenshot from 2023-12-02 16-12-26](https://github.com/KRIISHSHARMA/AWS/assets/86760658/9efd1bc2-5393-4ac1-9a28-0355a7961482)
![Screenshot from 2023-12-02 16-12-51](https://github.com/KRIISHSHARMA/AWS/assets/86760658/b7a5eecb-5d92-46af-a9ad-7ba6db2a5391)


- after confiugring aws cli on cloud 9 (scroll up) 
-  configure EKS ctl and kubectl [link for installation](https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/setting-up-eksctl.html)
  
![Screenshot from 2023-12-02 16-35-44](https://github.com/KRIISHSHARMA/AWS/assets/86760658/e128f431-c888-4cc3-b8fa-2f7a0a3835a1)
![Screenshot from 2023-12-02 16-55-57](https://github.com/KRIISHSHARMA/AWS/assets/86760658/79d1bb3c-b8b3-49af-bd3f-b7552ab700da)
![Screenshot from 2023-12-02 16-56-13](https://github.com/KRIISHSHARMA/AWS/assets/86760658/9e89cf9d-7dbc-419e-8f0b-f35c8b830198)
![Screenshot from 2023-12-02 16-57-22](https://github.com/KRIISHSHARMA/AWS/assets/86760658/7bd6650b-e499-414d-baef-5f7a5bdc8799)

- launching a cluster
  ```bash
  eksctl create cluster --name test --version 1.28 --nodegroup-name ng.default --node-type t3.micro --nodes 2 --managed
  ```
  ![Screenshot from 2023-12-02 17-05-19](https://github.com/KRIISHSHARMA/AWS/assets/86760658/460b3b95-798a-439f-9611-95c419fa1064)

- yaml file for nginx container launched with official nginx image
  ``` bash
     apiVersion: apps/v1
  kind: Deployment
  metadata:
      labels:
          environment: test
      name: test
  spec:
      replicas: 1
      selector:
          matchLabels:
               environment: test
      template:
          metadata:
              labels:
                  environment: test
          spec:
              containers:
              - image: nginx:1.16
                name: nginx

  ```
``` bash
  nano nginx-deployment.yaml
```
- kubectl is the thing using which we will be creating , launching the resources , creating pods , troubleshooting cluster using kubectl
- we will apply this file using kubectl
  ``` bash
    kubectl apply -f nginx-deployment.yaml
  ```
![Screenshot from 2023-12-02 17-51-03](https://github.com/KRIISHSHARMA/AWS/assets/86760658/1d1e3352-8c71-4714-91f4-b94a25168230)

- to see pods used by kubectl
![Screenshot from 2023-12-02 17-58-35](https://github.com/KRIISHSHARMA/AWS/assets/86760658/4621853e-23ea-4d95-be42-986136776895)

- autoscaler used by eks
![Screenshot from 2023-12-02 18-00-51](https://github.com/KRIISHSHARMA/AWS/assets/86760658/e926f3b6-ec65-43a1-854d-6c809c6680f4)

- can scale it 
![Screenshot from 2023-12-02 18-03-17](https://github.com/KRIISHSHARMA/AWS/assets/86760658/533bd710-6456-47ed-8235-266d641d31a9)

- install matrix server , will continue to moniter the cpu matrix ,without this will not show how much resources are utilised 
``` bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

- creating php-apache autoscaling yaml file for horizontal pod autoscaling
  ``` bash
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: php-apache
  spec:
    selector:
      matchLabels:
        run: php-apache
    template:
      metadata:
        labels:
          run: php-apache
      spec:
        containers:
        - name: php-apache
          image: registry.k8s.io/hpa-example
          ports:
          - containerPort: 80
          resources:
            limits:
              cpu: 500m
            requests:
              cpu: 200m
  ---
  apiVersion: v1
  kind: Service
  metadata:
    name: php-apache
    labels:
      run: php-apache
  spec:
    ports:
    - port: 80
    selector:
      run: php-apache
  ---
  
  apiVersion: autoscaling/v1
  kind: HorizontalPodAutoscaler
  metadata:
    name: php-apache
    namespace: default
  spec:
    scaleTargetRef:
       apiVersion: apps/v1
       kind: Deployment
       name: php-apache
    minReplicas: 1
    maxReplicas: 10
    targetCPUUtilizationPercentage: 50
  ```

```  bash
nano hpa.yaml
```
- deploying
  ``` bash
  kubectl apply -f hpa.yaml
  ```
![Screenshot from 2023-12-02 18-46-22](https://github.com/KRIISHSHARMA/AWS/assets/86760658/95757273-91db-4065-9265-fbebcbe59cc2)
![Screenshot from 2023-12-02 19-07-14](https://github.com/KRIISHSHARMA/AWS/assets/86760658/a99730d8-96b4-4915-b27e-53264933f50a)

- artificial load
  ``` bash
  kubectl run -i --tty load-generator --rm --image=busybox:1.28 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
  ```

- creating a load balancer type service 
![Screenshot from 2023-12-02 19-20-07](https://github.com/KRIISHSHARMA/AWS/assets/86760658/a815b33d-e2e0-4ade-b6e4-da263e14ad14)
- https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/

- creating nodeport service
  ![Screenshot from 2023-12-02 19-26-13](https://github.com/KRIISHSHARMA/AWS/assets/86760658/57ca24cb-0985-4df1-89b0-14e87e1269df)
![Screenshot from 2023-12-02 19-34-42](https://github.com/KRIISHSHARMA/AWS/assets/86760658/4da03506-cefb-4e4e-9b32-e81743bb4d6e)

![Screenshot from 2023-12-02 19-33-13](https://github.com/KRIISHSHARMA/AWS/assets/86760658/63a123b8-95fb-46ce-a57d-b9098359d1ef)


## EKS 
![Screenshot from 2023-12-02 16-04-58](https://github.com/KRIISHSHARMA/AWS/assets/86760658/86c01036-bc68-4035-a38f-21a253b80f20)
![Screenshot from 2023-12-02 16-08-06](https://github.com/KRIISHSHARMA/AWS/assets/86760658/694af61d-a154-461c-a15c-33cf94787fe4)

