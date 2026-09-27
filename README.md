# Youth Pathways SA

A beginner-friendly project about **youth unemployment in South Africa**. The solution is a small web app that gives young people a starting plan for work, training, or a small business and points to established support sites.

## Problem and outcome

Statistics South Africa reported a 47.4% unemployment rate for youth aged 15–34 in Q2 2026. Source: https://www.statssa.gov.za/?p=19804

**Outcome:** A visitor answers two questions and receives practical next steps. The prototype does not promise a job, scrape vacancies, collect personal information, or require an account.

## Try it on your computer

Download this folder and double-click `index.html`. No installation is needed. Select a goal and internet access level, then click **Show my plan**.

## Use AWS

The app is a static HTML file. Amazon S3 can host static websites. For a secure public production site, use CloudFront with an S3 origin access control and keep S3 public access blocked. AWS guide: https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/getting-started-secure-static-website-cloudformation-template.html

For a quick learning demonstration in the AWS console:

1. Open **S3** in your chosen AWS Region and create a bucket with a globally unique name. Check your account's pricing before creating resources.
2. Under **Properties**, enable **Static website hosting** and set the index document to `index.html`.
3. Upload `index.html` into the bucket.
4. To make the S3 website endpoint public, follow AWS's official bucket access and policy instructions exactly: https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html . This route exposes the website publicly over HTTP; for HTTPS use CloudFront.
5. Copy the **Bucket website endpoint** from Properties and test the form.
6. When finished, delete the bucket contents and bucket if you do not need hosting anymore.

No EC2 instance, terminal, GitHub permission grant, or Amplify connection is needed for this route. AWS S3 static hosting guide: https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html

## Upload to your existing GitHub repository

Open https://github.com/ThandoUnqobile/youth-pathways-sa . Choose **Add file → Upload files**, then drag `index.html` and `README.md` from this folder onto the page. Add a commit message and choose **Commit changes**. If replacing an existing README, GitHub will update it in the commit. Do not upload the ZIP itself as the only project file.

## Future improvements

With permission and a clear privacy notice, an optional AWS Lambda + API Gateway service could accept feedback, and a database could hold curated resources. The present version works without these services or ongoing server costs.

## Sources and links

- Statistics South Africa Q2 2026: https://www.statssa.gov.za/?p=19804
- SA Youth: https://sayouth.mobi/
- NSFAS: https://www.nsfas.org.za/content/how-to-apply.html
- NYDA: https://www.nyda.gov.za/
