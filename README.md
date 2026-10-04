# AWS Internship – Week 2

AWS Cloud Basics internship (Skill Nexis), Week 2: EC2 web server deployment and S3 static website hosting.

## What I did
- Launched an EC2 Ubuntu instance (t3.micro, free-tier eligible) and connected to it using EC2 Instance Connect
- Installed and configured Nginx as a web server, replacing the default page with custom content
- Created a new S3 bucket and enabled Static Website Hosting
- Deployed a multi-section personal portfolio website (summary, skills, projects, experience, education) to the bucket
- Configured a bucket policy for public read access and verified the site loads via the S3 website endpoint
- Troubleshot an account-level IAM permissions boundary error that blocked EC2 resource creation for a scoped IAM user, and resolved it by using the root account

## Files
- `Week_2_Assignment_mini_Project.pdf` – full walkthrough with screenshots, bucket policy, and learning outcome
- `screenshots/` – supporting screenshots for each step

## Live Website
My portfolio site, deployed entirely on AWS S3:
**http://pragati-port-2026.s3-website.ap-south-1.amazonaws.com**

*(Note: S3 static website hosting only supports HTTP, not HTTPS. Use the link exactly as written above.)*

## Key learning
Compared two different ways of serving content on AWS — a self-managed EC2 server running Nginx versus 
fully-managed S3 static website hosting. Learned that S3 static sites use a dedicated "website endpoint," 
separate from a regular object URL, and that the same two layers of access control from Week 1 (Block Public 
Access + bucket policy) apply here too. Also practiced troubleshooting an unexpected account-level IAM 
restriction by testing with the root account to isolate the cause.
