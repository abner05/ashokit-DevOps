## Step-1 : Setup Linux VM (Amazon Linux AMI)

1) Login into AWS Cloud account
2) Launch Linux VM using EC2 service
   
     - AMI : Amazon Linux
     - Instance Type : t2.medium
       
4) Connect to VM using MobaXterm

## Step-2 : Install Docker In Linux VM

```
$ sudo yum update -y 
$ sudo yum install docker -y
$ sudo service docker start
```
## Step-3 : Add ec2-user to docker group by executing below command

```
$ sudo usermod -aG docker ec2-user
```

## Step-4 : Restart the session
$ exit

## Step-5 : Then press 'R' to restart the session (This is in MobaXterm)

## Step-6 :  Verify docker installation
$ docker -v

## Step-7 : Run SonarQube using docker image
```
$ docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube:lts-community
```
