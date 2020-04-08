## Kata Level 1

### Objective:
Our main goal of this Kata is to use terraform and ansible for installing a webserver  and run a node application.

### History
In the old days, you needed to create a server in your cloud provider via clicks and then install needed packages and finally you had your application ready to run.

#### Terraform Process
For this, you will need to use terraform and aws provider for launching a new EC2 instance. For this Kata, you don't need to worry about creating a VPC, you can use AWS Default VPC and Subnets. You will need to be able to access the new EC2 you created. Remember to configure a PEM key. A security group is needed, with ports 22 and 5000 open


#### Ansible
You will need to configure an ansible role for configuring the server. For doing this you will to:

 - Download the application from GitHub: [https://github.com/abkunal/Chat-App-using-Socket.io](https://github.com/abkunal/Chat-App-using-Socket.io)
 - Install NodeJS and npm
 - Install pm2
	 - for pm2, these are the commands you're going to need:
			 - pm2 start app.js
			 - pm2 save
			 - pm2 startup
