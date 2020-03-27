## Kata Level 1

### Objective:
Our main goal of this Kata is to use terraform and ansible for installing a webserver  and run a node application.

### History
In the old days, you needed to create a server in your cloud provider via clicks and then install needed packages and finally you had your application ready to run.

#### Terraform Process
For this, you will need to use terraform and aws provide for launching a new EC2 instances. For this Kata, you don't need to worry about creating a VPC, you can use AWS Default VPC and Subnets. You will need to be able to access to the new EC2 you created so you will need to configure a PEM key. Also remember that you will need to configure the security group for accessing via SSH and for seeing the application in a browser. Hint, the application runs in port 5000.

#### Ansible
You will need to configure a ansible role for:

 -  download the application from git hub: [https://github.com/abkunal/Chat-App-using-Socket.io](https://github.com/abkunal/Chat-App-using-Socket.io)
 - install nodejs and npm
 - install pm2
	 - for pm2, these are the commands you're going to need:
			 - pm2 start app.js
			 - pm2 save
			 - pm2 startup
