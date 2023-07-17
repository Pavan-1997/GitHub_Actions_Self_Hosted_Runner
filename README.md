# GitHub Actions on a Self-Hosted Runner

- With self-hosted runners, we can set up and manage the runner infrastructure ourselves.

- Self-hosted runners can be deployed on virtual machines, physical machines, or in cloud providers like AWS, Azure, or Google Cloud.

- They provide more flexibility regarding available resources, dependencies, and network access.

- We can use self-hosted runners for repositories hosted on GitHub.com or GitHub Enterprise Server.

- They are beneficial when we need to run workflows that require specialized hardware, software configurations, or access to on-premises resources.

- We use this since if we have a private project, security concerns handling FinTech clients and also have large and scalable resources

---
# Deploying a simple Python app on the Self Hosted Runner (EC2 Instance) using GitHub Actions

1. Launch an EC2 instance with Ubuntu 


2. Open the ports in Security tab of the instance created 

    Inbound Rule & Outbound Rule
    
    80, 443


3. Now go to the GitHub repo -> Settings -> Actions -> Runners -> Click on New self-hosted runner -> Select Linux and use x64 as Architecture

    Perform execution of the commands listed on the instance

![image](https://github.com/Pavan-1997/GitHub_Actions_Self_Hosted_Runner/assets/32020205/df6954ad-3694-4055-a15c-40c78bdf3fd8)

- To secure sensitive info we use Secrets and variables 


4. In the github config file change the parameter below

    runs-on: self-hosted 
    
    Commit the code, the job must be triggered to run on the instance
