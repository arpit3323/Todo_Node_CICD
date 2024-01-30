                                Complete Step-by-Step Jenkins CICD with GitHub Integration

**Overview:**

CI/CD is a way to introduce automation during app development stages and deliver apps to customers in bulk. The basic concepts of CI/CD are continuous integration, continuous delivery, and continuous deployment.

Thus, CI/CD has become an integral part of the software development cycle, with many frameworks and tools available. We will use Amazon Web Services (AWS) as a cloud platform, GitHub for code repositories, Jenkins for Continuous Integration (CI), and Continuous Delivery (CD).


**Requirements:**

AWS account.
Jenkins and Docker are to be installed on the AWS EC2 Instance
GitHub repo (code)

**Step 1: Setup AWS EC2 Instance**

We will first create an AWS Instance (Ubuntu) free-tier eligible using the AWS console.

Steps To launch the EC2 instance:
1. Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.
2. Choose Launch Instance.

![EC2 Lanch](Images/image.png)


3. Once the Launch an instance window opens, provide the name of your EC2 Instance:

![Alt text](Images/image-1.png)


4. Choose the Ubuntu Image (AMI):

![Alt text](Images/image-2.png)

5. Choose an Instance Type. Select t2.micro for our use case which is also free-tier eligible.

![Alt text](Images/image-3.png)

6. Select an already existing key pair or create a new key pair. In my case, I will select an existing key pair.

![Alt text](Images/image-4.png)

7. Edit Network Settings, create a new Security Group, and select the default VPC with Auto-assign public IP in enable   mode. Name your security group and allow ssh traffic, HTTPS, and HTTP everywhere (we can change the rules later).
![Alt text](Images/image-5.png)

8. Leave the rest of the options as default and click on the Launch instance button:

![Alt text](Images/image-6.png)

9. On the screen you can see a success message after the successful creation of the EC2 instance, click on Connect to instance button:

![Alt text](Images/image-7.png)

10. Now connect to instance wizard will open, go to EC2 Instance connect tab and click on it :

![Alt text](Images/image-8.png)

11. New Window tab will open with EC2 Intance terminal 

![Alt text](Images/image-9.png)


**Step 2: Install Jenkins on EC2 Instance:**

Jenkins installation is straightforward:

1. First Update your Server with the command

                                            $  sudo apt-get update 


2. Install Java

                                            $ sudo apt install openjdk-11-jre

3. Verify Java Installation:

                                            $ java -version

![Alt text](Image/image-10.png)








[def]: image.png