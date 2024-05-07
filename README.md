# Deploying a Web Application on AWS EC2

### Set up an AWS EC2 instance

1. Create an IAM user & login to your AWS Console
    - Access Type - Password
    - Permissions - Admin
2. Create an EC2 instance
    - Select an OS image - Ubuntu
    - Create a new key pair & download `.pem` file
    - Instance type - t2.micro
3. Connecting to the instance using ssh
```
ssh -i instance.pem ubunutu@<IP_ADDRESS>
```

Updating the outdated packages and dependencies
```
sudo apt update
```

### Deploying the project on AWS

1. Clone this project in the remote VM
```
git clone https://github.com/<owner>/repo.git
```

2. Navigate to the folder
   ```
   cd <repo>
   ```

3. Install Nginx
   ```
   sudo apt install nginx -y
   ```
   ```
   sudo systemctl enable nginx
   sudo systemctl start nginx
   sudo systemctl status nginx
   ```

**Now copy the <public-ip-add> of ec2 instance and paste in browser**

**Successfully Deployed Web-application on AWS EC2 Instance**



