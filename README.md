---

## Table of Contents

### Topics of Study

- [Accesing and Using AWS Services](#different-ways-of-accessing-aws)
- [Account Security, Permissions & The IAM Service (Identity & Access Management)](#data-structures)
- [Getting Started with Compute Services & EC2](#more-knowledge)
    - [What are remote machines](#binary-search)
    - [Some other topic in here](#bitwise-operations)
- [Managing Cloud Networks via VPCs (Virtual Private Cloud)](#trees)

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
        - The idea here simply is that you often have services that need to work with each other. For example, you could have a service that actually should perform certain taks related to another service. By default, this would not be allowed because, and that's important, by default nothin is allowed in an AWS account. When logging into the account, you can do everything. But when you create an identity like a user or a role, by default that identity is not able to do anything. And if you use a service and runs an application on top of a service and that application wants to interact with another service, by default it would fail. Now if you create such a role and you assign it tothat service on which you are running your application, that role can hold the permissions required by your application sothat your application all of a suddenis able do something with another service, and that's the idea behind roles. 

        
    
        

        
