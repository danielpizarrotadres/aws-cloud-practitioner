---

## Table of Contents

### Topics of Study

- [Getting Started](#getting-started)
- [Accesing and Using AWS Services](#different-ways-of-accessing-aws)
- [Account Security, Permissions & The IAM Service (Identity & Access Management)](#data-structures)
- [Getting Started with Compute Services and EC2](#more-knowledge)
    - [What are remote machines](#binary-search)
    - [Some other topic in here](#bitwise-operations)
- [Managing Cloud Networks via VPCs (Virtual Private Cloud)](#trees)

### Getting Started
- Amazon Web Services (AWS) is a subsidiary of Amazon (amazon.com) and it is a Cloud Computing Services Provider

- ### What is "Cloud Computing"
    - [ ] Cloud Computing is the on-demand delivery of IT resources over the Internet 

### Accesing and Using AWS Services
- Nothing to implement here, we just have to sign in into the AWS Services

- ### Different Ways of Accessing AWS
    - [ ] Management Console
        - Easy to access & navigate (Graphical user interface)
        - Perfect for exploring services & features
        - Complex, repeatd or large-scale setups can become cumbersome
        - Perfect tool for getting started on AWS

    - [ ] AWS CLI
        - Command-driven access (It gives us command-drive acces to AWS instead a Graphical user Interace, install CLI from AWS CLI website)
        - Perfect for well-known complex, repeatd or large-scale setups and tasks
        - Prior installation and configuration needed
        - Can simpify complex, repeated or large-scale setups
       
    - [ ] SDKs (Available in many programming lenguages)
        - Programmatic access
        - Infrastructure as code
        - Perfect for automating tasks
        - Can simplify setups and allows for building (automated) tools
        
    - [ ] API Calls
        - Use services via HTTP requests
        - Request configuration can be challenging
        - Typically, we'd go for one other solutions
        
    - [ ] Behind the scenes the three ways described before send commands, API HTTP requests.
    - [ ] AWS in the end exposes an API (a server) and we can send requests to the AWS API to make AWS do something

- ### AWS Pricing and Cost Management
    - [ ] AWS offers a variety of pricing and payment models (depending on the actual service used)

    - [ ] On Demand
        - Most common pricing model
        - Only pay for the resources used
        - Which resources and factores are charged depends on the actual services used
        
    - [ ] In Advance
        - Pay for reserved capaciy or min. usage
        - Discounted price
        - Only offered for some services or service features
        
    - [ ] Subscription
        - Pay a flat monthly / yearly fee
        
- ### Cost Management and Working with Budgets

    - [ ] Where to look up pricing information?
        - Log into the AWS account
        - Go to "Billing Dashboard"

    - [ ] Budges
    
- ### Accesing and Using AWS Services Summary
    - [ ] Which method of accesing AWS is NOT a valid option?
       - AWS CLI (Yes, i can do it)
       - AWS Management Console (Yes, i can do it)
       - AWS Desktop Client ✅ (This is the correct answer. There is no such thing as a "AWS Desktop Client")
       - AWS API (Yes, i can do it)
    - [ ] What do all AWS access methods have in common?
       - They require programming experience
       - They send a request to the AWS API ✅ (Everything's an API call behing the scenes)
       - They have nothing in common
    - [ ] What's NOT true about AWS pricing?
       - You find service pricing details on the AWS pricing pages (on their website)
       - All AWS services are free within the first 12 months ✅ (Whilst there is a free tier, only SOME services are part of it. Not ALL services.)
       - Some services offer a monthly free usage volume
    - [ ] How can you efficiently control your costs?
       - Use cost management tools (e.g., cost explorer) and budgets ✅ (The best way of monitoring and controlling cost)
       - Check your monthly bill at the end of every month
       - AWS automatically alerts you about unexpected spending, use the cost explorer to dive deeper
    - [ ] Which statement about cost management is NOT true?
       - You can set budgets (with alerts) to be notified about excess spendings (This statement is true)
       - You can use the AWS Cost Protection Tool to set a maximum cost barrier ✅ (There is no AWS Cost Protection Tool and we can't set a fixed, maximum amount of costs)
       - You can explore basic cost details via daily updated monthly bills
       - You can explore cost details via Cost Explorer
    - [ ] What are AWS Support plans all about?
       - You have to pick a paid plan in order to use AWS for production workloads
       - You can pick different levels of support, based on your business requirements ✅✅
       - All support plan levels are paid levels
      
### Account Security, Permissions & The IAM Service
- Being able to acces AWS is of course important but it's super important to do that in a secure way. For that we will take a look at the AWS security model and manage our AWS account and authentiation also for various access methods

- ### AWS Security Model (Share Responsibility Model)
    - Security is a shared responsibility by AWS and you.
    - [ ] AWS
        - Secure the infrasructure and physical machines
        - Protect their internal systems and processes
        - Secure managed services and everything we can't configure or control
    - [ ] You
        - Secure your apps and workloads
        - Protect your account and control account access
        - Secure everything you are able to control and configure
       
- ### Protecting Your Account
    - [ ] Secure Credential
    - [ ] Multi-Factor Authentication
        - Enable MFA
        - Use a digital or physical solution
    - [ ] Utilize IAM users (Identity and Access Management)
        - IAM users are simply users that you can create inside your account, which then can be used for logging into that account (We can create this users instead share password with multiple people)
        - Create IAM users for accessing your acccount
        - Every person (e.g. colleague) should use a separate user
        
- ### What is IAM ?
    - As mentioned, it stands for Identity and Access Management, and it its for managing identities and access.
    - [ ] Identities
        - Identities are siple the entities that can do something in your account, the who so to say, for example
        - The entity for which access rights / permissions are controlled
        - Who is allowed (or not allowed) to do something?
        - Users, User Groups & Roles
    - [ ] Access Management
        - The permissons that are granted (or not granted) to an entity
        - What is an entity allowed to do (with a given service)?
        - Permissions, managed via Policies
        - So Permissions, managed via Policies. These are terms you will hear a lot when working with AWS
        
- ### Users, User Groups and Roles
    - [ ] Users
        - Typically assigned to humans that should be able to access that account
        - Every person that should be able to access the AWS account gets a user
    - [ ] User Groups
        - Group users to share permissions
        - Avoid unnecessary permission copying or tedious per-user access management
    - [ ] Roles
        - A bit more advanced
        - Typically used by services
        - The idea here simply is that you often have services that need to work with each other. For example, you could have a service that actually should perform certain taks related to another service. By default, this would not be allowed because, and that's important, by default nothing is allowed in an AWS account. When logging into the account, you can do everything. But when you create an identity like a user or a role, by default that identity is not able to do anything. And if you use a service and runs an application on top of a service and that application wants to interact with another service, by default it would fail. Now if you create such a role and you assign it to that service on which you are running your application, that role can hold the permissions required by your application so that your application all of a suddenis able do something with another service, and that's the idea behind roles. 

- ### Account Security, Permissions & The IAM Service Summary
    - [ ] Which feature can add an extra layer of protection to your AWS account?
       - Choosing a unique email address.
       - Enabling MFA (Multi-Factor Authentication) ✅ (Adding a second factor besides the password, greatly enhances security.)
       - Restricting unanthenticated users permissions.
    - [ ] What is a key concept of the Shared Responsibility Model?
       - Every party is only responsible for things it controls. ✅ (That is the main principle behind this model.)
       - AWS is only responsible for securing its infrasturcture.
       - AWS customers are only responsible for protecthing their account.
    - [ ] What's NOT one of your responsibilities under the Shared Responsibility Model?
       - Protect access to your AWS account.
       - Securely set up operating systems used by managed AWS services ✅
       - Securely set up extra software you install on top of AWS services
    - [ ] What is the IAM service all about ?
       - About managing identities (users, user groups, roles) and their permissions. ✅ (That is what the service is all about)
       - About managing user responsibilities and duties.
       - About managing identities (users, user groups, roles) and their responsibilities and duties.
    - [ ] What is the idea behind "Roles"?
       - Roles are like users: they are assigned to humans and can be used to log into an AWS account.
       - Roles can be assigned to services which can assume them in order to gain certain permissions. ✅✅ (Roles allow AWS services and the worloads running on top of them to work together.)
       - Roles can be used to prevent a service from interacting with other services.
    - [ ] Which statement about IAM permissions is NOT true?
       - By default, all identities (users, users groups, roles) have no permission to do anything.
       - AN explicit "Allow" overwrites an explicit "Deny" ✅ An explicit "Deny" overwrites always an explicit "Allow"
       - If multiple permissions / policies add different permissions, the identity gains the combination of acces rights
       
### Getting Started with Compute Services and EC2

- Time to live the configuration and security sections, no matter how important they might be. Because in the end you use AWS to run your products applications, or workloads, on top of the AWS. You use AWS because you wanna outsource IT tasks, or build a product on top of AWS.

- We are going to start most diving into one of the most important category of services and one of the most important AWS Service.


- ### AWS Compute Services (Compute Category)
    - [ ] EC2 (Elastic Compute Cloud)
        - One of the most important and popular services!
        - Rent a (virtual) remote server / computer. So you can rent one of those machines owned and operate by AWS in its datacenters.
        - Fully configurable. You can decide wich operatyng system install of top them. You can install any other extra software, you can realyy configure them as if they stand of your room.
        - Run any kind of workload in the cloud.
        
    - [ ] ECS / EKS (Elastic Container Service) / (Elastic Kubernetes Service)
        - What are "Containers"?
        - Containers in the end are packages of code + the code's dependencies (e.g, OS, required software). So in the end it is a package that contains everything to run an application, so to say.
        - Containers allow developers to distribute and deploy reproducible code enviroments (includuing the code itself). This package can be built with extra software like "Docker".
        - No server configuration required (since the container already includes the operating system, software, configurations etc.)
        - This are servicices that give you preconfigured environments where you can deploy your containers into, so that you don't need to install this Docker software manually anywhere and configure it, but instead you can use ECS or EKS to have a prefigured environment for you to run your containers in.
        - What are ECS / EKS concepts about?
        - An alternative to EC2 - for containerized workloads
        - Run clusters of containers in the cloud
        - Managed (with vas amount of configuration options)
        - Run any kind of containerized workload
        
    - [ ] Lambda (Serverless Code Execution)
        - What are "Serverless" Services?
        - The idea behind serverless services, like Lambda (note that there are more serverless services like Lambda), simply is that you have some workload which would typically run on top of a server, so on some computer where you set up some software, install an operatyng system and so one, but with serverless services like "Lambda" you can run your code without doing that setup work.
        - You can run that code without installing or configuring any underlying software, any operating system.
        - Serverless services allow you can to run code without configuring or controlling any servers.
        - You can perform tasks in response to events by just providing the code that should be executed.
        
    - [ ] Understanding EC2
        - Rent a (virtual) remote machine
        - "A computer in the cloud"
        - It's actually (typically) not an entire machine. Instead you have those AWS Datacenters  with those physical machines, physical computers inside of them. Those computers are pretty powerful machines. AWS is not putting standard computers in its datacenters. therefore whilst you can technically rent an entire computer if you really want to. Typically you rent a slice of a computer. You rent a "virtual server". To be precise, AWS calls it an EC2 Instance. When using this EC2 Service, you can start EC2 Instances. So you start renting slices off those computers in the AWS data centers.
        - A slice of the physical machine. Fully isolated from other slices (other EC2 Instances), with its own dedicated hardware which can be used by other instances
        - A slice of the physical machine Fully isolated from other slices (other instances) with its own dedicated hardware.
