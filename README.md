<p align="center">
	<img width="600" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/c2adb7f2-3245-4654-bb88-0b7102f2ce55" alt="DevOps Q&A">
</p>

# DevOps Interview Questions for Juniors
> DevOps Interview Questions and Answers for Junior DevOps Engineers 

**Disclaimer:**
- You are welcome to edit and add Questions/answers through Pull Request
- These questions are for the Junior/beginner in the DevOps field
- These questions are not for specific companies/entities, this cover the most popular DevOps tools, and these tools may vary from one company to another based on the technology stack used by it .. so you need to check the job requirements for the position you are applying and focus on what is there.

<h3 align="left">Included Tools:</h3>
<p align="left"> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#aws-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#docker-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#linux-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="bash" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#kubernetes-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/jenkins/jenkins-icon.svg" alt="jenkins" width="40" height="40"/> </a> Terraform,</a> Ansible, </a> and more coming ... 



## AWS Questions:

1. **What’s EC2 Instance types?**

	- General-Purpose Instances
	- Memory-Optimized Instances
	- Compute-Optimized Instances
	- Storage Optimized Instances

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/f1cd6e00-8218-4d26-9f0e-066be57576e8)

	
 2. **What’s VPC?**
A VPC is a virtual network that closely resembles a traditional network that you'd operate in your own data center.

3. **What’s S3 bucket and what types of it?**
Amazon S3 is an object storage service that stores data as objects within buckets. An object is a file and any metadata that describes the file. A bucket is a container for objects.

	***Types(storage classes):***
	- S3 Standard: for frequently accessed data
	- S3 Intelligent-Tiering: for automatic cost savings for data with unknown or changing access patterns
	- S3 Standard-Infrequent Access (S3 Standard-IA) and S3 One Zone-Infrequent Access (S3 One Zone-IA) for less frequently accessed data,
	- S3 Glacier

4. **Is there a difference between SG and NACL?**
Security groups are associated with an instance of a service. It can be associated with one or more security groups that have been created by the user. (Stateful)
A security group can be understood as a firewall to protect EC2 instances.
NACL can be understood as the firewall or protection for the subnet. (stateless)

5. **What’s the difference between Public Subnet and Private Subnet?**
The instances in the public subnet can send outbound traffic directly to the internet.(Via Internet Gatway).
Whereas the instances in the private subnet can't. Instead, the instances in the private subnet can access the internet by using a network address translation (NAT) gateway that resides in the public subnet.

6. **How can an application access Internet without receiving requests from the internet?**
Using NAT configured in the Routing Table.
The database servers can connect to the internet for software updates using the NAT gateway, but the internet cannot establish connections to the database servers.

  
7. **Design Architecture for web application contains 3 tiers: Frontend, Backend, and Database?**

  ![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/cc5d5560-885f-42a0-8a9c-371baff370ac)


  

8. **How you can cost optimize  your infrastructure?**
obtaining the best pricing and terms for IT purchases, standardizing, simplifying, and rationalizing assets such as platforms and applications, as well as processes and services, automating and digitalizing both the IT and business operations. Monitor billing · Reduce manual processes

  

	**On AWS** : 
	- stop guessing capacity (use Autoscaling Group).
	- Choose the right pricing models.
	- Use Reserved Instances (RI) to reduce RDS, Redshift, ElastiCache, and Elasticsearch costs.
	- Match Capacity with Demand.
	- Identify Amazon EC2 instances with low utilization and reduce cost by stopping or rightsizing.
	- Implement processes to identify resource waste.

  

9. **What are the types of Database engines on AWS?**
	- Amazon RDS is available on several database instance types - optimized for memory, performance, or I/O – and provides you with **six familiar database engines** to choose from, including: 
Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle Database, and SQL Server.
	- Ledger: Amazon Quantum Ledger Database (Amazon QLDB)
	- Document: Amazon DocumentDB (with MongoDB compatibility)
	- No SQL: DynamoDB
	- In-memory: Amazon ElastiCache
	- Graph: Amazon Neptune

  

10. **What’s the difference between AWS Shield vs AWS WAF vs AWS Guard-Duty?**

	**Shield** is DDoS protection and is also located "at the edge".

	**AWS WAF** focuses on Layer 7 protection(Application Layer)
Your subscription to Shield Advanced covers the basic AWS WAF fees for web ACLs, rules, and web requests.

	**GuardDuty** is intelligent threat detection. That means without much configuration, it reads your CloudTrail, Config, and VPC FlowLogs and notifies you if something unexpected happened.

	**Amazon Inspector** is more for applications. It's an automated security assessment service that helps improve the security and compliance of applications.

  

11. **What’s the difference between S3 vs EBS vs EFS?**
**S3**: Object Storage
**EBS**: File System Storage (Connected to one EC2) scalable network file storage
**EFS**: scalable network file storage (Can be connected to many EC2)

  
12. **Is it possible to host an application on S3?**
Only one can host a static website on Amazon S3.
by configuring your bucket for website hosting and then uploading your content to the bucket.

  

13. **What’s SSM ?**
Amazon EC2 Simple Systems Manager (SSM) is a tool that allows an IT professional to automatically configure virtual servers in a cloud or in an on-premises data center. Need to install an agent.

  

14. **What is the difference between Latency Based Routing and Geo DNS in Route53?**
Amazon maps out typical latency between IP addresses and AWS regions.
	- Choose Latency-based Routing to have the fastest response.
	- Geolocation maps the IP addresses to geographic locations. This permits rules like "send all users from Côte d'Ivoire to the website in France", so they see a language-specific version.

  

15. **What is RTO and RPO in AWS?**
**RTO** (Recovery Time Objective): is a measure of how quickly can your application recover after an outage
**RPO** (Recovery Point Objective): is a measure of the maximum amount of data loss that your application can tolerate.

  
16. ** What are DevOps tools on AWS?**
	- AWS CodePipeline: Software Release Workflows
	- AWS CodeBuild: Build and Test Code
	- AWS CodeDeploy: Deployment Automation
	- AWS CodeStar: Unified CI/CD Projects
	- AWS CodeCommit: Private Git Hosting
	- Lambda, Amazon Elastic Container Registry (ECR), Amazon Elastic Kubernetes Service (EKS)



## Docker Questions:

  

17. **What’s the difference between container vs VM?**

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e5eb4f75-82d4-4b39-8ac7-e5c5a428fb0d)

**VM**: uses separate OS for each VM
**Containers**:
- Use the Host OS
- Less utilization
- Your app is backed in a container and shared between environments: DEV, TEST, OPERATION
- Less size
- Fast boot up
containers abstract application layer, vm abstract os

  

18. **What are Docker Image layers?**
Layers are a result of the way Docker images are built. Each step in a Dockerfile creates a new “layer” that’s essentially a diff of the filesystem changes since the last step.
Metadata instructions such as LABEL and MAINTAINER do not create layers because they don’t affect the filesystem.

  

19. **What’s the difference between Entrypoint and CMD?**
**CMD** describes the default container parameters or commands. The user can easily override the default command when you use this.

	**ENTRYPOINT** - A container with an ENTRYPOINT is preferred when you want to define an executable.
You can only override it if you use the --entrypoint flag
entrypoint not override, CMD overwrite with before actions

	**RUN** - To run this command you will need a separate new layer and this command is mainly used to build images, and install packages and applications.

	CMD commands are ignored by Daemon when there are parameters stated within the docker run command while ENTRYPOINT instructions are not ignored but instead are appended as command line parameters by treating those as arguments of the command

  

20. **What are multiple base images on Dockerfile?**
	It allows you to create multiple image layers on top of the previous layers and the **AS** command provides a virtual name to the intermediate image layer. The last FROM command in the dockerfile creates the actual final image
- the idea that you have two images, the first one you build your binaries files and copy them to the second one, and the second image is the final image which from it you run your container. the first image helped you to build the second one.
- The benefits you get from this are that you built your app on a large image and the final result is a lightweight image that is on your containers.  

<img width="306" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/2736c1b5-540a-40a4-833d-d38efaf2dc0e">


  

21. **What are types of Docker volumes?**
**Named volumes** have a specific source from outside the container, for example, awesome:/bar.

	**Anonymous volumes** have no specific source, therefore, when the container is deleted, you can instruct the Docker Engine daemon to remove them.
	
	bind volumes, tmpfs volumes

	 **Types of Mount** : 
	1. Volumes
	2. Bind mounts
	3. tmpfsmounts
	4. named pipes

  

22. **What are the types of Docker networks?**
bridge, overlay, host, none

  

23. **What’s the difference between COPY and ADD?**

	**COPY** takes in a source and destination. It only lets you copy in a local or directory from your host (the machine building the Docker image) into the Docker image itself.
	
	**ADD** does the same but in addition, it also supports 2 other sources:
A URL instead of a local file/directory. &&&& Extract tar from the source directory into the destination.

  

24. **How could you secure your Dockerfile?**
	- Run the container as a non-root user. ...
	- Remove unnecessary packages/software from the image. ...

	Enable Docker Content Trust (DCT) ... Content trust is disabled by default in the Docker Client. To enable it, set the DOCKER\_CONTENT\_TRUST environment variable to 1. This prevents users from working with tagged images unless they contain a signature.
	- Use COPY instead of ADD in Dockerfile. ...
	- Do not store any secrets in Dockerfile. ...
	- Install verified packages and use trusted base images.
\-----

	1. Continuous Approach. ...
	2. Image Vulnerabilities. ...
	3. Policy Enforcement. ...
	4. Create a User for the Container Image. ...
	5. Use Trusted Base Images for Container Images. ...
	6. Do Not Install Unnecessary Packages in the Container. ...
	7. Add the HEALTHCHECK Instruction to the Container Image.

25. **What are the Stages of DevSecOps?**
To adapt, software development, maintenance, and upgrading must incorporate security awareness into each stage.

	- Plan. The planning phases of DevSecOps are the least automated with the involvement of collaboration, discussion, review, and a strategy for security analysis. ...
	- Code. ...
	- Build. ...
	- Test. ...
	- Release. ...
	- Deploy. ...
	- Operation. ...
	- Monitor.

  
<img width="460" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/57c095a5-d0d5-4315-9854-17fb10b08706">
  

## Linux Questions:

  

26. **What’s the difference between Reverse Proxy and Web Server?**

	**A web server** listens for HTTP requests and reacts to them by sending back an HTTP response.
	
	**A reverse proxy** is a web server that determines what response to make by also implementing an HTTP client. Client A makes an HTTP request to the reverse proxy. The reverse proxy makes an HTTP request to Server B.

Reverse proxies are typically implemented to help increase security, performance, and reliability.

  

<img width="353" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/bc363971-d20d-423e-9382-20d2b11ccfd0">



27. **How can optimize performance for Nginx?**

	**7 Tips for NGINX Performance Tuning**:
	Tip 1 – Adjust Worker Processors & Worker Connections.
	Tip 2 – Enabling Gzip Compression.
	 Tip 3 – Change static content caching duration on Nginx.
	Tip 4 – Change the size of the Buffers.
	Tip 5 – Reducing Timeouts.
	Tip 6 – Disabling access logs (If required)
Tip 7 – Configure HTTP/2 Support.

28. **How can list all processes?**

		ps
		ps -A
		ps -e

	There is `top` also not for all

29. **How can list live processes?**

	    ps -aux | less

30. **How could you check memory space?**

	    cat /proc/meminfo

	  `	free` >>> checks memory and SWAP memory


31. **How could you check storage space?**	
		
    df -H

  
32. **What’s file management in Linux?**
	In Linux, most of the operations are performed on files. And to handle these files Linux has directories also known as folders which are maintained in a tree-like structure. Though, these directories are also a type of file themselves

  
33. **What’s LVM and how can using it?**
	Logical volume management (LVM) is a form of storage virtualization that offers system administrators a more flexible approach to managing disk storage space than traditional partitioning.

  

34. **How could you mount a volume in Linux?**
	1. Identify the USB drive using the `lsblk` command.
	2. Create a directory to mount the USB drive into. 
	3. Check if it formatted or not
	4. Mount the USB drive to the /media/pendrive directory using the `mount` command. 
	5. Check the drive has been mounted by re-running lsblk.

  


35. **What are Linux bootstrap processes?**
Bootstrapping in computer science is **the technique for producing a self-compiling compiler**. That is compiler/assembler written in the source programming

  

	**The booting process takes the following 4 steps that we will discuss in greater detail:**
	1. BIOS Integrity check (POST)
	1. Loading of the Boot loader (GRUB2)
	1. Kernel initialization.
	1. Starting systemd, the parent of all processes.

	  

36. **Tell me about Linux file systems.**

	  The Linux filesystem unifies all physical hard drives and partitions into a single directory structure, this is how you sort your data inside the storage.

<img width="275" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/c38ac75e-00ce-4d18-8f03-90ee27605f3e">



  

37. **What’s WAF in Linux ?**
	a firewall specifically designed to handle "web" traffic; that is, traffic using the HTTP protocol. Generally speaking, the role of a WAF is to inspect all HTTP traffic destined for a web server, discard "bad" requests, and pass "good" traffic on

	  

38. **What’s Selinux and how can use it?**
SELinux defines access controls for the applications, processes, and files on a system. It uses security policies, which are a set of rules that tell SELinux what can or can't be accessed, to enforce the access allowed by a policy

  


39. **What’s the /dev/null directory?**
The null device is typically used for disposing of unwanted output streams of a process, or as a convenient empty file for input streams. This is usually done by redirection. The /dev/null device is **a special file, not a directory, so one cannot move a whole file or directory into it with the Unix mv command**.

  
  
  
  
  

## Kubernetes Questions:

  

40. **What are Kubernetes architecture components and explain them?**
The main componehnts of a Kubernetes cluster include: **Nodes, Image Registry, Pods**
\-------------------------------------------
**Kubernetes Core Components: Control Plane(Master Node):**
	-  **kube-apiserver**. Provides an API that serves as the front end of a Kubernetes control plane. ...
	-  **etcd**: The key-value store where all data relating to the cluster is stored
	-  **kube-scheduler**. When a new Pod is created, this component assigns it to a node for execution based on resource requirements, policies, and ‘affinity’ specifications regarding geolocation and interference with other workloads.
	-  **kube-controller-manager**. Although a Kubernetes cluster has several controller functions, they are all compiled into a single binary known as kube-controller-manager.
\-----------------------------------------------
	**Node components include: (Worker Node)**
	- **kubelet**: Every node has an agent called kubelet. It ensures that the container described in PodSpecs is up and running properly.
	- **kube-proxy**: A network proxy on each node that maintains network nodes that allow for the communication from Pods to network sessions, whether inside or outside the cluster, using operating system (OS) packet filtering if available.
	- **container runtime**: Software responsible for running the containerized applications. Although Docker is the most popular, Kubernetes supports any runtime that adheres to the Kubernetes CRI (Container Runtime Interface).

41. **What’s the difference between Master and Worker Node?** 
**Worker Node**:
	- Do all the Work
	- Responsible for running the containers and doing any work assigned to them by the master node
	- Many nodes
	- Consist of **3** components: kubelet, kube-proxy, container runtime

	**Master Node**:
	- Create the control plane
	- Looks after scheduling and scaling applications. maintaining the state of the cluster.
	- 1 or two nodes
	- Consist of **4** components: etcd, kube controller manager, kube-API-server, kube-schedular

  

42. **What are service types?**
	-  **ClusterIP** (default): Internal clients send requests to a stable internal IP address.

	-  **NodePort**: Clients send requests to the IP address of a node on one or more nodePort values that are specified by the Service.

	-  **LoadBalancer:** Clients send requests to the IP address of a network load balancer.

	-  **ExternalName**: Internal clients use the DNS name of a Service as an alias for an external DNS name.

	-  **Headless**: when you want a Pod grouping, but don't need a stable IP address.

  
	The **NodePort** type is an extension of the **ClusterIP** type. So a Service of the type NodePort has a cluster IP address.

	  

	The **LoadBalancer** type is an extension of the **NodePort** type. So a Service of type **LoadBalancer** has a cluster IP address and one or more **nodePort** values.

  
![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e4e43c46-7a7d-4e2f-9bd8-5b20aff34df5)

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e43b8466-69ab-48fa-a5b9-d22adaf53c3f)


43. **What’s the difference between deployment vs DaemonSet vs StatfulSet?**
- **Deployments** and ReplicationControllers are meant for stateless usage and are rather lightweight.
- **Statefulsets**: is used for Stateful applications (DB), each replica of the pod will have its own state, and will be using its own Volume.
- **DaemonSet**: is a controller similar to **ReplicaSet** that ensures that the pod runs on all the nodes of the cluster.

  

	**A Daemonset will not run more than one replica per node**. Another advantage of using a Daemonset is that, if you add a node to the cluster, then the Daemonset will automatically spawn a pod on that node, which a deployment will not do

  
![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/aac25788-f74c-4d3e-9a15-7d0174fb3980)


![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/67c1aaa1-18e8-4384-ab7e-41f2a65aa832)


![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/df977628-dd54-481b-9b88-95a573f47be3)


  

44. **What’s the difference between ReplicaController and ReplicaSet?**
The rolling-update command works with Replication Controllers, but won't work with a Replica Set.

  

45. **What is the difference between ReplicaSet and Deployment?**
	- **A ReplicaSet** ensures that a specified number of pod replicas are running at any given time.
	- **Deployment** is a higher-level concept that manages ReplicaSets and provides declarative updates to Pods along with a lot of other useful features.

  
  

46. **How can create a variable for your deployment and how can secure it?**

	  **Secrets** can be mounted as data volumes or exposed as environment variables to be used by a container in a Pod.
Secrets can also be used by other parts of the system, without being directly exposed to the Pod.

  

47. **Is it possible to create multiple containers in one pod?**
YES – but better be one container/Pod
because each container should do one task so if you have 2 containers in a pod and you are near to increase one container because its service/task has a lot of traffic ... then k8s will create a new pod with two containers that the second is not doing anything so you are wasting your compute capacity.


48. **What’s a Sidecar container?**
	- Sidecar containers are containers that run along with the main container in a pod. You can define any number of sidecar containers to run alongside the main container
	- The sidecar containers can also share storage volumes with the main containers, allowing the main containers to access the data in the sidecars.
	- The primary application can run independently in one container while the sidecar hosts complementary processes and tools

  

49. **What’s CustomResourcesDefination (CRD)?**
API resource allows you to define custom resources. Defining a CRD object creates a new custom resource with a name and schema that you specify. The Kubernetes API serves and handles the storage of your custom resource. The name of a CRD object must be a valid DNS subdomain name

  

50. **What’s kube-proxy?**
a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept. kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster

  

51. **What’s the difference between liveness vs readiness vs startup probes?**
**liveness**:
  **Liveness Probe**: Checks if a container is running properly and restarts it if the probe fails.
**Readiness Probe**: Checks if a container is ready to receive network traffic and delays routing until it becomes ready.
**Startup Prob**e: Checks the initial startup readiness of a container, helping differentiate slow starts from unresponsive containers.

52. **What’s the operator of the Database?**
The DB Operator eases the pain of managing PostgreSQL and MySQL instances for applications running in Kubernetes. The Operator creates databases and makes them available in the cluster via Custom Resource. It is designed to support the on-demand creation of test environments in CI/CD pipelines.

  

53. **What are the static pods?**
Static Pods are managed directly by the kubelet daemon on a specific node, without the API server observing them

  

54. **What are helm and helm charts?**
Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application. Charts are easy to create, version, share, and publish — so start using Helm and stop the copy-and-paste.
Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources

  

55. **What’s custom resources in K8s?**
A custom resource is an **extension of the Kubernetes API** that is not necessarily available in a default Kubernetes installation. It represents a customization of a particular Kubernetes installation. However, many core Kubernetes functions are now built using custom resources, making Kubernetes more modular

  

56. **What’s the difference between Ingress and IngressPolicy?**
**Ingress Resource**: an object with a set of routing rules.
The Ingress concept lets you map traffic to different backends based on rules you define via the Kubernetes API.
**IngressPolicy** (Ingress rules) allows connections to all pods in the "default" namespace with the label "role=db" on TCP port 6379 from: any pod in the "default" namespace with the label "role=frontend" and any pod in a namespace with the label "project=myproject"

  

## **General Questions:**

  

57. **What’s CICD?**
CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development.
continuous integration, continuous delivery, and continuous deployment.

  
  

58. **What’s Jenkins pipeline?**

  

a suite of plugins that supports implementing and integrating continuous delivery pipelines into Jenkins. A continuous delivery pipeline is an automated expression of your process for getting software from version control right through to your users and customers.

  

59. **What’s Jenkins Master and Slave?**

  

The Jenkins master acts to schedule the jobs, assign slaves, and send builds to slaves to execute the jobs. It will also monitor the slave state (offline or online) and get back the build result responses from slaves and display build results on the console output.

  

60. **What’s Jenkins Shared Library?**
It is a feature that allows you to define reusable code in a version-controlled repository and share it across Jenkins pipelines. It promotes code reuse, and consistency, and simplifies pipeline maintenance.
 A shared library in Jenkins is a collection of Groovy scripts shared between different Jenkins jobs
Each shared library requires users to define a name and a method of retrieving source code.

61. **What’s Java Spring Boot?**
Java Spring Boot (Spring Boot) is a tool that makes developing web applications and microservices with Spring Framework faster and easier through three core capabilities: Autoconfiguration. An opinionated approach to configuration. The ability to create standalone applications.

  

62. **What’s the difference between Rolling Strategy and Blue-Green Strategy?**
**Rolling deployments** follow a staggered delivery pattern that gradually replaces instances of the existing environment with updated versions. 
**Blue-green deployments** involve creating a rigorously-tested second environment before completely shifting the current instance to the new environment.

63. **What’s SonarQube?**
empowers all developers to write cleaner and safer code
Code Quality Assurance tool that collects and analyzes source code, and provides reports for the code quality of your project

64. **What’s API?**
a set of functions and procedures allowing the creation of applications that access the features or data of an operating system, application, or another service

  

65. **How can writing a bash script?**
	1. create a file using a vi editor(or any other editor). Name script file with extension.sh.
	2. Start the script with #! /bin/sh.
	3. Write some code.
	4. Save the script file as filename.sh.
	5. For executing the script type bash filename.sh.

  
  

66. **What’s the difference between `awk` vs `sed`?**
**`sed`** is a command utility that works with streams of characters for searching, filtering and text processing
**`awk`** is more powerful and robust than sed with sophisticated programming constructs such as ifelse, while, do/while

  

67. **How can create variables in Ansible?**
 define a variable dynamically when you run a playbook, **use the --extra-vars option along with the key and value of the variable you want to define**. In this example, the key is my\_var because that's the string referenced in the playbook, and the value is any string you want the variable to contain

68. **What are modules and tasks in Ansible playbook?**
Ansible Playbooks are **lists of tasks that automatically execute against hosts**. Groups of hosts form your Ansible inventory. Each module within an Ansible Playbook performs a specific task
  
**Modules**: Standalone code units in Ansible for specific tasks on managed hosts.

**Tasks**: Actions in Ansible playbooks defining desired system state using modules.
  
  

69. **Difference between Dynamic Inventory and Multiple Inventory?**
**Dynamic Inventory**: Retrieves inventory information dynamically from external sources.
**Multiple Inventory**: Allows the use of multiple static inventory files for organizing and managing inventory across different environments or projects.
Using inventory directories and multiple inventory sources. Static groups of dynamic groups. If your Ansible inventory fluctuates over time with hosts spinning up and shutting down in response to business demands, the static inventory solutions will not serve your needs.
Multiple Inventory:You may need to track hosts from multiple sources: cloud providers, LDAP, Cobbler, and/or enterprise CMDB systems.

  

71. **What’s the path of ansible configuration?**
/etc/ansible/ansible. cfg

  

72. **What’s the difference between ansible and chef?**
Ansible: uses YAML (easy), Agentless
Chef and Puppet: uses Ruby (Difficult), needs an agent and updates are a headache.

  

73. **What’s privilege escalation in Ansible?**
Ansible uses existing privilege escalation systems to execute tasks with root privileges or with another user’s permissions. Because this feature allows you to ‘become’ another user, different from the user that logged into the machine (remote user), we call it become. The become keyword uses existing privilege escalation tools like *sudo*, *su*, *pfexec*, *doas*, *pbrun*, *dzdo*, *ksu*, *runas*, *machinectl* and others.


74. **What’s Azure DevOps?**
Azure DevOps supports a collaborative culture and set of processes that bring together developers, project managers, and contributors to develop

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/d18bb3ef-b8c2-4fbc-a400-1a62fafde352)

74. **What’s Git forking?**
Forking is a git clone operation executed on a server copy of a project's repo.
A fork in Git is simply a copy of an existing repository in which the new owner disconnects the codebase from previous committers. A fork often occurs when a developer becomes dissatisfied or disillusioned with the direction of a project and wants to detach their work from that of the original project.

  

75. **Is it better to fork or clone in Git?**
If you would like to make changes directly to a repository you have permission to contribute to, then **cloning** will be the first step before we implement the actual changes and push.
If you don't have permission to contribute to the repository but would like to implement changes anyway, a **fork** is the way to go.

  

76. **What’s the difference between stateful vs stateless?**
**stateless** system sends a request to the server and relays the response (or the state) back without storing any information.
**Stateful** systems expect a response, track information, and resend the request if no response is received.
- Stateless Protocol is a network protocol in which the Client sends a request to the server and the server responds back as per the given state.
- Stateful Protocol is a network protocol in which if a client sends a request to the server then it expects some kind of response, in case of no response then it resends the request.

  

77. **What’s a message broker? Or message queue (MQ)**
Way of how the microservices communicate
A message broker is a software that enables applications, systems, and services to communicate with each other and exchange information. EX: redis, Rabbit MQ

  

78. **What’s CDN?**
A content delivery network (CDN) refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content. Ex: Amazon CloudFront.


79. **What are types of API?**
Five types of APIs are:
1) Open API
2) Partner API 4) High-level
3) Internal API 5) Low-level API

  

80. **What is Web APIs ?**
- Open APIs. Open APIs, also known as external or public APIs, are available to developers and other users with minimal restrictions. ...
- Internal APIs. In contrast to open APIs, internal APIs are designed to be hidden from external users. ...
- Partner APIs. ...
- Composite APIs. ...
- REST. ...
- JSON-RPC and XML-RPC. ...
- SOAP.

  
81. **What’s the terraform state?**
Terraform must store state about your managed infrastructure and configuration. This state is used by Terraform to map real world resources to your configuration, keep track of metadata, and to improve performance for large infrastructures. This state is stored by default in a local file named **"terraform.tfstate”**
but it can also be stored remotely, which works better in a team environment.
