# Social Media System

## Project Description

This is the second project from Revature training.

This entails a social media site where users can create accounts and posts and edit their account information. Users can also see and like the posts of other people that have also accessed the website.

## Technologies Used

* Spring MVC
* Spring ORM with Hibernate
* Spring AOP
* AWS PostGreSQL RDS
* AWS S3 Bucket
* React.js
* Email.js-com
* React-Spring


## Features

* Single page application built with React with animations
* Reset password with email sending and hashed passwords
* Connected backend that persists all front end changes

## Getting Started

Use the command below in git bash to download all of the files
git clone https://github.com/juuse/SocialMedia.git

### Importing the project
Download spring tool suite(sts).
Open sts on your local machine.
Create or select a folder to use as your workspace.
In the top navbar go to File -> Import -> "Existing Maven Projects".
Select the cloned repo directory by clicking the browse button.
Check the pom.xml and click finish.
Right click the project and go to Maven -> Update Project
Find the window labeled "Boot Dashboard" and right click the project name and click (Re)start

### Setting up the AWS Database
Create an AWS free tier account.
Search Security Group and click on the one labeled VPC feature.
Click on create security group, name it whatever you want, and click on Add Rule under Inbound Rules.
For type, just do All Traffic and for Source use Anywhere or My Ip and then click create security group.
Go to the RDS module in AWS and click on Create Database.
Engine Type -> PostGreSQL, Templates -> Free Tier, Public Access -> Yes, VPC security group -> The one just created that allows either only your IP or everyone.
Set the master username and master password (NOTE: Make sure to remember what these are because these are how you will access the database).
Once the status becomes available click on the database and copy the endpoint and port.

Now navigate to the src->main->webapp->WEB-INF->applicationContext.xml.
Find the bean with the id "dataSource" and replace the systemEnvironment calls with your credentials.
username will be your database username, password will be your master password, and in the url only replace the system.get env section with your endpoint.

## Usage

After running the project, open your desired browser and type localhost:<port number>/project1 (i.e. http://localhost:9005/Project2/).
The login screen should appear at this point. Create an account and it will log you into the site.
There will be options to change your information including your password. You can also make posts with up to one image to be displayed. 

