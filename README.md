# AWS Static Website Deployment Example

This repository demonstrates how to deploy a static website to AWS using S3, Route 53, CloudFront, and ACM.

## Overview

![Deployment Diagram](diagram.png)

1. **Static Website Content**: Your website content (HTML, CSS, JavaScript, images, etc.) is stored in an S3 bucket configured for static website hosting.

2. **Amazon CloudFront**: CloudFront is used as a content delivery network (CDN) to cache and serve your website content globally, reducing latency and improving performance.

3. **Amazon Route 53**: Route 53 is used for DNS management. If you have a custom domain, Route 53 handles DNS resolution and routes traffic to your CloudFront distribution.

4. **AWS Certificate Manager (ACM)**: ACM provides SSL/TLS certificates for your custom domain, ensuring secure HTTPS connections to your website.

## Deployment Steps

### Prerequisites
- An AWS account with appropriate permissions to create and manage S3 buckets, CloudFront distributions, Route 53 hosted zones, and ACM certificates.
- AWS CLI installed and configured with appropriate credentials.

### Steps

1. **Set up S3 Bucket**:
   - Create an S3 bucket and enable static website hosting.
   - Upload your website content to the bucket.

2. **Configure CloudFront Distribution**:
   - Create a CloudFront distribution with your S3 bucket as the origin.
   - Configure caching behavior and other settings as needed.

3. **Obtain ACM Certificate**:
   - Request an SSL/TLS certificate from ACM for your custom domain (if applicable).
   - Validate domain ownership (if using a custom domain).

4. **Set up Route 53** (if using a custom domain):
   - Create a hosted zone in Route 53.
   - Add DNS records to route traffic to your CloudFront distribution.

5. **Deploy Website**:
   - Update your website code as needed.
   - Use AWS CLI or deployment scripts to sync the updated content to your S3 bucket.
   - Invalidate CloudFront cache if necessary.


## Feedback and Contributions

If you have any feedback or suggestions for improvement, feel free to open an issue or submit a pull request.

Happy deploying!
"# Deploy-a-Static-Website-on-AWS" 
