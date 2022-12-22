---

## Table of Contents

### Topics of Study

- [Accesing and Using AWS Services](#algorithmic-complexity--big-o--asymptotic-analysis)
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
       - AWS Desktop Client (This is the correct answer. There is no such thing as a "AWS Desktop Client") ✅
       - AWS API (Yes, i can do it)
    - [ ] What do all AWS access methods have in common?
       - They require programming experience
       - They send a request to the AWS API ✅
       - They have nothing in common

        
        
