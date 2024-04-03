<h1 align="center">AWS- Build our own Network-Lab.</h1>

Building my own network in AWS environment  my objective is to get familiar with AWS platform and its environment as well as improve my  technical skills. AWS has many different types of technologies that we can utilize to building our skillset such as:

- Amazon EC2 instance 
- Building Virtual private Cloud (VPC) 
- Building storage buckets using Amazon S3 to store files. 
- AWS offers security features like Security Groups and Network Access Control Lists (NACLs) to help protect your resources and much more. 

##

<h3 align="center"> AWS setting Newtok Steps:</h3>

  
- Setup an Amazon Web Service Account
- Setup AWS IAM user with MFA
- Build a VPC with a Single Public Subnet
- Create a Security Group that allows either RDP or ssh from your home IP
- Then Build a Microsoft Windows Server 2022 server.
- Show how to access your server through RDP or ssh.

 ##
 
<h3 align="center"> Build a VPC with a single subnet.</h3> 

Here, I will create a VCP for my home lab that will give me the ability to separate environment for certain task and remove those I don’t need without affecting others. (by default, AWS account comes with a VPC in every region)
![Screenshot 2024-04-02 003940](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/ee13b376-eed8-4aa4-bee6-6842aef580e9)

In this step we should had define our subnet for our AWS home Network. The IPv4 CIDR block is the allowed block range for your entire VPC. The subnet CIDR is the range that will be used for resources within your VPC.

![Screenshot 2024-04-02 004006](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/7d8cd508-5f14-47c9-a114-94f0384bf24d)
##
![Screenshot 2024-04-02 004216](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/df0ee44d-3d94-4c2e-b92f-d8f869da83fd)
##
![Screenshot 2024-04-02 013551](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/74e79153-2e90-407b-9a8f-6689a564fef7)

##

<h3 align="center"> Setting Access to VPC Home Network.</h3> 

 When creating a Virtual Private Cloud (VPC), it automatically comes with a default security group. This default group typically allows unrestricted access within the VPC, which might not be suitable for all environments, especially those used for home labs where security is a concern. To modify the scope of access, navigate to the VPC dashboard and look for the 'Security Groups' section. Here, you can select the default security group associated with your VPC and adjust its settings. It's recommended to restrict inbound and outbound traffic to only necessary ports and IP addresses to enhance the security of your Network environment.
![Screenshot 2024-04-02 233646](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/f584f971-a08d-440f-99e3-07f44ffbfc53)


##

<h3 align="center">Building a windows server for own Network.</h3> 

Here are the steps I did follow to create a windows server:
- In the AWS services search bar search for EC2.
- Click on Instances and select Launch Instance.
- In AWS marketplace search for windows 
- Then choose the t2.micro image. The instance types may change but it should say free tier eligible.
- Under the instance details change the Network to our newly created VPC and leave everything else default
- Keep the storage the same but more can be added depending on our project needs.
- Tags can be assigned to resources to better keep track of services across AWS.
- Then select the security group that we edited to allow ssh and RDP.
- Last step from this part we will need to create a new key pair that we will need to login to our instance.
![key pair](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/e033051a-4527-4f23-b268-6f6d76e7c4c0)

##
<h3 align="center">Connecting to our  EC2 Network  Server.</h3> 

- In the picture below we can see the home lab windows  server is running.
![2024-04-03 00_29_09-Screenshot 2024-04-02 013613](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/4b1b4704-7995-4160-83fa-a96e290174ca)

- Take the keypair you created and go to the instances tab and select your new instance and connect.
![connented](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/a374c88b-e2c1-40da-9d64-73f9883b5c4e)


- Choose the RDP client tab and download the remote desktop file.
- Use the key file to get the password for the instance.
- Click on the RDP file and enter your username and password.
![windows-server](https://github.com/luzritacco/AWS-Own-Nework-lab/assets/151267325/e9bca64d-af37-4570-9dd0-2719fe320ff4)

##

<h1 align="center"> Conclusion </h1>
In conclusion, building a network in the AWS environment is a valuable learning experience that can provide insights into cloud networking principles and best practices. By starting with a solid foundation, leveraging automation tools, and utilizing AWS services for connectivity and management, one can create a robust and efficient network that meets the demands of modern cloud computing.
