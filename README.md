# Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront

## Objective
The objective of this project is to strengthen already known theory on CLOUD BLOB STRORAGE , WEB HOSTING , and Content Delivery Network (CDN) through practical apllication in this project, and also enfroce deeper understanding of these computing theory and their apllication in real life cloud architecture.  

## Architecture Diagram 
This diagram give an overview of how these different component ( users , the S3 storage bucket and Cloudfront(CDN) ) come together to host a static site .
![Alt asw](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Static%20S3%20site.png)


Image 1 : Architecture Diagram .

## Skills Learned
-Cloud storage hosting

-CDN

-security

-global distribution

## Steps To Build 
The following are the steps and procedure taken to configure and set up the defferent component to make this project possible . 

### Step 1 : 
Creating The a simple website file in html and CSS for styling of the web page . The images below shows the contain of the html and CSS in VS code. 
  ![Alt VS code](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(55).png)

  Image 2 : The contain of the Index.html file.
               
  ![Alt VS code](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(56).png)
     Image 3 : The contain of the styles.css file.
     
  The static site is a simple single page of my cv showing the some differnt skill i have , the Index.html file contain's the codes for the structure for the site and the css file contain's the code for styling. 

### Step 2 :
 Creating the S3 bucket as shown in the image below ;
 ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(40).png)
   Image 4 : The UI page on AWS for creating S3 bucket.
   
The image above Shows the name of the S3 bucket, at this point the remaining seting of the S3 bucket is is left on defualt.

### Step 3 : 
 Uploading the static web site file into the S3 bucket. 
 ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(42).png)
    Image 5 : Before uploading the files.
    
![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(44).png)
   Image 6 : After uploading the files into the S3 bucket.

### Step 4 :
Creating the CND distribution with Origin Access Control (OAC)  for AWS S3, As shown in the Images below :

  ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(41).png)
   Image 7 .

![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(47).png)
  Image 8 : This image shows the overview of the configuration done when creating the distribution. 
  
To set up of OAC for the CND distribution , i went to Origin --> Edit Origin , and then Create an OAC , as shown in the image below :
    ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(48).png)
   Image 9 .

  ### Step 5 :
  Updating the bucket policy to allow access from the cloudfront. To do this , i want to the S3 Permission page and paste  the policy that i copied from the Origin page.

   ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(50).png)
   Image 10 .
The Image above shows the new policy of the bucket .

### Step 6 : Testing 

I send an Https request to the Infrastructure. 

  ![Alt AWS](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Screenshot%20(53).png)
   Image 11 .
 The image above show that every thing is working. 

### Conclusion
 This project demonstrates the process of deploying a secure and scalable static website using Amazon S3 and CloudFront. By leveraging CloudFront as a global CDN and restricting direct access to the S3 bucket, the solution ensures improved performance while maintaining strong security controls. This deployment reflects practical experience with AWS cloud infrastructure, content distribution networks (CDNs), and IAM access configuration. Future enhancements may include CI/CD automation for continuous deployment, support for multiple pages, and integration with AWS Lambda or API Gateway for dynamic features.
