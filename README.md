# My Website with AWS (S3, CloudFront, Route 53, CI/CD)

## Project Description

This project demonstrates a simple static website hosted on AWS using:
- **Amazon S3**: to host static HTML files.
- **Amazon CloudFront**: as a CDN (Content Delivery Network) for faster content delivery with HTTPS.
- **Route 53**: for managing DNS (if using a custom domain).
- **AWS CodePipeline**: to automate the deployment process using CI/CD.

The goal is to create a scalable, cloud-based infrastructure with full automation of deployments.

## Technologies Used

- **Amazon S3**: For hosting static files like `index.html` and `error.html`.
- **Amazon CloudFront**: To distribute content globally via CDN with HTTPS support.
- **Route 53**: (Optional) For custom domain management and DNS routing.
- **AWS CodePipeline**: Automates deployments from GitHub to Amazon S3.



## Project Setup

### Step 1: Configure Amazon S3
1. Create an S3 bucket with static website hosting enabled.
2. Add the `index.html` and `error.html` files.
3. Attach the bucket policy as outlined in `bucket-policy.json` to allow public access.

### Step 2: Configure CloudFront
1. Create a CloudFront distribution that points to the S3 bucket.
2. Enable HTTP to HTTPS redirection for better security.

### Step 3: (Optional) Configure Route 53
1. If you have a custom domain, create a hosted zone in Route 53.
2. Add A/AAAA or CNAME records pointing to your CloudFront distribution.

### Step 4: Setup CI/CD Pipeline
1. Set up AWS CodePipeline to pull changes from the GitHub repository and automatically deploy them to the S3 bucket.

### Step 5: Testing the Setup
1. Make a change to the `index.html` file in GitHub.
2. The change will automatically deploy to the website via the CI/CD pipeline.

![Cloud Architecture](https://github.com/user-attachments/assets/685c4443-fc50-456d-9e78-0c82fa1399f5)

