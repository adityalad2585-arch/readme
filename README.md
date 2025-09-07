# my facebook- website 

## introduction

### This project is a simple demo of a *Facebook clone web page* created using basic HTML .It is not the real Facebook, but just a practice project to learn and understand how to build web pages with styling, text, and images.The project displays a *facebook message* along with the *Facebook logo*, giving a look similar to the original site.

##  Features  
- Simple HTML structure for easy understanding  
- Styled text with headings and welcome message  
- Facebook logo image added to the page  
-  Clean and minimal design  
-  Beginner-friendly project for practicing web development  

## prerequisites
- active aws account 
- A running linux Ec2 instance
- SSH access with facebook.pem
- Basic knowledge of Linux commands
- Nginx installed on the server
- Project files (HTML) ready to upload
- Security Group with port (81) open
- website will be accessible at
- http://18.234.117.81

##
## steps for deployment

<img width="1920" height="976" alt="Screenshot2 (12)" src="https://github.com/user-attachments/assets/0f8ddba5-71f2-4cd0-a81e-505beb43e51b" />



##
### step 1 :  connect to ec2 instance using SSH key
    
### 1.copy the SSh key

##

<img width="1904" height="861" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/a0db476b-13b9-47b2-b157-09284948274f" />

##
### 2. go to SSh key folder and open git bash and paste the command

##
<img width="1914" height="1019" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/3f8da64d-4d9a-4bb3-8983-6a6fb42fb961" />


### step2: install nginx web server

* sudo yum update 

<img width="1918" height="1031" alt="Screenshot2 (3)" src="https://github.com/user-attachments/assets/11c292f1-9237-419e-8a12-c5eca8de5b6a" />


##
### install nginx web server

* sudo yum update nginx -y
##
<img width="1918" height="1027" alt="Screenshot2 (4)" src="https://github.com/user-attachments/assets/55554915-136c-40ba-9813-b04684ca8fa2" />

##
### step 3: start enable and check status of the web server
*  sudo systemctl start nginx
* sudo systemctl  enable nginx
* sudo systemctl status nginx
##
<img width="1920" height="1021" alt="Screenshot2 (5)" src="https://github.com/user-attachments/assets/e73767e6-d552-49e9-95aa-4b3bd2b1c300" />

##
## step 4. go to the default directory (/usr/share/nginx/html/)
* cd//usr/share/nginx/html/

<img width="1920" height="1015" alt="Screenshot2 (6)" src="https://github.com/user-attachments/assets/c9b93c9f-8040-475d-bdcb-64c7af8fa995" />



## step 5. create directory(facebook) and go inside that directory
* sudo mkdir facebook 

<img width="1920" height="1015" alt="Screenshot2 (7)" src="https://github.com/user-attachments/assets/04a4c67a-2a8d-4c63-aed4-1bc912cf1b10" />



## step 6 . download the image to be insert in the website
* image download for index page

##
<img width="1916" height="1017" alt="Screenshot2 (9)" src="https://github.com/user-attachments/assets/0ce4f1ab-ba55-4f47-b7cb-dda107b9c64c" />


##
## step 7 . create index.html page
* sudo vim index.html

* insert code in index.html 
##
<img width="1920" height="1031" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/6ddab2c9-3d44-475d-ae8c-9e2d9414af97" />


##
## step 8. configuring nginx root directory
* sudo vim /etc/nginx/nginx.conf


<img width="1920" height="1017" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/f56df08e-eb1b-47ea-a0e9-98d94015d7a8" />


##
* find the server and change the root directory and restart nginx
* sudo systemctl restart  nginx



##
## step 9. go to security groups and add rule on port no 81 and save it

##

<img width="1920" height="919" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/0adbf87f-5c29-48b3-ba0d-7e4215848120" />



##
<img width="1920" height="1024" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/5c3b8397-3196-414e-ae36-08e99d683a26" />

##
## step 10. copy public IP and paste to any browser
##

<img width="1919" height="992" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/7c5bd1bf-fe29-4772-94ae-7c53531f97ce" />


##
## step 11. see your website on browser
##

<img width="1920" height="973" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/ee6f5339-cd15-4310-bca7-fbc164f72f36" />




##

## summary

Install Nginx, place your website files in the web directory, set proper file permissions test the configuration, restart Nginx, allow web traffic through the firewall, and optionally secure the site with SSL using Let’s Encrypt.
##
