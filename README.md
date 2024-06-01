# IronHack-Lab11-AWS-Cloud-Architectures
## Part 1: Designing Cloud Infrastructure

- **Task**:
  - Design a cloud infrastructure for a scalable web application.
  - Include components like compute instances, storage, and network configurations.
  - Use AWS EC2, S3, and VPC to build the basic architecture.

- **Solution**:

  We can use the Three-Tier Architecture wich is a popular approach to building web applications that separates the application into three distinct layers: presentation, business logic, and data storage. This architecture is designed to enhance scalability, security, and performance, making it a preferred choice for modern web applications.

![web-architecture](https://github.com/LiMonC/IronHack-Lab11-AWS-Cloud-Architectures/assets/6668834/f93cabe8-ce97-43e9-81fd-b1764232d32a)

## Part 2: IAM Configuration

- **Task**:
  - Define IAM roles and policies for different components of the architecture, such as developers, admins, and application servers.
  - Ensure that each role adheres to the principle of least privilege.

- **Solution**:
  - Developers:
    - EC2 specific development environment.
    - Launch new EC2 instances.
    - Access to S3 to upload and download files.
    - Access to RDS to perform database tasks.

  - Administrators:
    - Full access to all resources for management and maintenance.
    - Access to IAM, EC2, S3, RDS and VPC management.

  - Application Servers
    - Policies that allow access to S3 for reading and writing


## Part 3: Resource Management Strategy

- **Task**:

  - Develop a strategy for managing resources that includes auto-scaling, load balancing, and cost optimization using AWS Auto Scaling, ELB, and AWS Budgets.

- **Solution**:
  1. Rightsize the Resources:
      - Rightsizing the infrastructure. Analyze the application's actual resource needs and adjust the cloud instances accordingly. This not only optimizes performance but also prevents unnecessary expenses associated with over-provisioning.

  2. Leverage AWS Auto Scaling:
     - Implement AWS Auto Scaling to automatically adjust the number of compute resources based on demand. This ensures optimal performance during peak   times and cost savings during periods of lower activity.

  3. Monitor and Analyze Usage Patterns
     - Continuous monitoring and analysis of resource usage patterns provide valuable insights. 

  4. Embrace Serverless Architectures
      - With AWS Lambda we pay only for the actual computing resources consumed during the execution of the functions. This not only reduces costs but also simplifies resource management.

  5. Implement Cost Controls
      - Configure AWS Budgets, utilize alerts for cost thresholds, and regularly review and optimize the spending. 

## Part 4: Theoretical Implementation

Using the AWS services identified, outline the architecture for the web application. Describe how each component interacts with others, focusing on the flow of data and control between services. This description should detail the role of each service in the architecture, ensuring a clear understanding of their interactions and dependencies.

- **Description**:
  
  - **AWS WAF:** can be attached to a load balancer to filter malicious traffic. This service applies rules to prevent common attacks like cross-site scripting and SQL injections.
    
  - **AWS Shield** can be utilized to safeguard infrastructure against network and transport layer DDoS attacks. This service is designed to detect and mitigate against these types of attacks.
    
  - **AWS IAM** can be used to apply fine-grained permissions to AWS resources and services. This ensures that only authorized users can access specific resources.
    
  - **Access Control List (ACL)** at the subnet level, which can be used to manage inbound and outbound traffic. These options allow for more granular control over network traffic and can help prevent unauthorized access.
 
  - **AWS Route 53** can be leveraged to provide DNS services and simplify domain management. It can also be used for active-passive or active-active failover between regions by conducting health checks.

  - **EC2** auto-scaling groups can be utilized to scale policies, activities, and processes, ensuring that resources are available as needed.

  - **AWS CloudFormation** can be employed to quickly create a stack and deploy resources with just one click. Alternatives like the Serverless Framework, Terraform, or CDK can also be considered.

  - **AMIs (Amazon Machine Images)** can be stored in S3 for easy and quick launching of new EC2 instances across regions.

  - **RDS** with backup configured and cross-region read replicas can help ensure high availability of databases.

  - **Load balancers** can be used to distribute load across multiple availability zones (AZs), and AWS scaling groups can provide redundancy and decoupling of services.



## Part 5: Discussion and Evaluation

- Discussion Points:
  - Explain the choice of services and how they interact to provide a resilient and secure infrastructure.
  - Discuss how the designed IAM policies contribute to overall security.
  - Review the resource management strategy to ensure it meets the scalability and cost-efficiency needs.

- **Conclusion**:
  - The adoption of a three-tier architecture on AWS brings about multiple advantages for developing web applications that are both scalable and secure. By dividing an application into separate layers, developers can ensure it is easy to maintain and upgrade.
  - By implementing security measures on AWS, organizations can protect their infrastructure and applications against potential security threats.
  - By implementing reliable solutions on AWS, organizations can ensure that their resources are highly available and can handle fluctuations in demand.
  - By implementing performance-boosting solutions on AWS, organizations can optimize their applications and services to deliver faster, more responsive experiences to their users.



