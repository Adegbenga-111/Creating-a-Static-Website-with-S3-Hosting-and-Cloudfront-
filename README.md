# Static Website Hosting with Amazon S3 and CloudFront

## Project Summary

This project demonstrates how to design, deploy, and secure a globally distributed static website using **Amazon S3** for object storage and **Amazon CloudFront** as a Content Delivery Network (CDN). The goal was to move beyond theory and gain hands-on experience with real-world cloud hosting, access control, and performance optimization.

The result is a secure static CV website served over HTTPS, with direct S3 access blocked and all traffic routed through CloudFront using Origin Access Control (OAC).

---

## Architecture Overview

The architecture consists of end users accessing a CloudFront distribution, which securely retrieves content from a private S3 bucket acting as the origin.

![Architecture Diagram](https://github.com/Adegbenga-111/Creating-a-Static-Website-with-S3-Hosting-and-Cloudfront-/blob/main/Static%20S3%20site.png)

**Key Components:**

* Amazon S3 (static website content storage)
* Amazon CloudFront (global CDN)
* Origin Access Control (OAC)
* HTTPS delivery

---

## Skills Demonstrated

* Static website hosting with Amazon S3
* Content delivery using CloudFront
* Securing S3 origins with Origin Access Control (OAC)
* HTTPS content delivery
* Basic web development (HTML & CSS)
* Cloud security and access control concepts

---

## Implementation Steps

### Step 1: Build Static Website Files

A simple single-page website (CV) was created using **HTML** for structure and **CSS** for styling. These files serve as the static content for the site.

* `index.html` — page structure and content
* `styles.css` — layout and visual styling

---

### Step 2: Create an Amazon S3 Bucket

An S3 bucket was created to store the static website files. Default settings were used initially, with public access restricted to ensure security.

---

### Step 3: Upload Website Files to S3

The HTML and CSS files were uploaded to the S3 bucket, forming the origin content for the CloudFront distribution.

---

### Step 4: Create a CloudFront Distribution

A CloudFront distribution was created with the S3 bucket configured as the origin.

* HTTPS enabled by default
* Global edge locations used for low-latency delivery
* Origin Access Control (OAC) enabled to restrict direct S3 access

---

### Step 5: Configure S3 Bucket Policy

The S3 bucket policy was updated to allow **only CloudFront** to access the bucket contents. This prevents users from bypassing CloudFront and accessing the bucket directly.

---

### Step 6: Testing and Validation

The CloudFront distribution URL was accessed over HTTPS to confirm:

* Successful content delivery
* Secure access through CloudFront
* Correct rendering of the static website

The test confirmed that the website was accessible globally and functioning as expected.

---

## Detailed Build Documentation
Step-by-step implementation, configuration screenshots, and troubleshooting notes are documented in  
➡️ [`steps.md`](/blob/main/steps%20.md)


## Conclusion

This project successfully demonstrates a secure and scalable approach to hosting static content on AWS using Amazon S3 and CloudFront. By integrating Origin Access Control, the solution enforces best practices by blocking public S3 access while leveraging CloudFront for performance and global distribution.

Through this project, I strengthened my understanding of cloud storage, CDN behavior, IAM-based access control, and real-world static web hosting architectures. This setup serves as a strong foundation for future enhancements such as CI/CD automation, multi-page websites, custom domains, and edge-based dynamic features using AWS Lambda or API Gateway.
