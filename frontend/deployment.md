# Deployment
Just serve index.html under "dist" folder to every URL. You maybe use whatever web servers or CDNs to do so.

In our case, we use S3 + Cloudfront. To deploy, navigate to project root directory and run the command below.

### Prerequisite
aws-cli 1.11.13+
```bash
❯ ./tools/sync staging #if you want to deploy staging
❯ ./tools/sync production #if you want to deploy production
```