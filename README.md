# Hosting-Resume-on-AWS-S3
Hosting Resume on AWS S3.
<br />

- <b>Athean</b> 
- <b>SQL</b>
- <b>Amazon S3</b>
- <b>Amazon Glue</b> 

<h2>Environments Used </h2>
- <b>AWS</b> 
<h2>Architecture Diagram:</h2>
<p align="center">
<br/>
<img src="https://imgur.com/bIs9YQw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h1>Step by Step:</h1>
<h2>Task 1: Sign in to AWS Management Console:</h2>
 Once Signed In to the AWS Management Console, make the default AWS Region as US East (N. Virginia) us-east-1.
<p align="center">
<br/>
<img src="https://imgur.com/BmKYyNr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


Great plan! It's well-organized, and you've broken down the tasks into manageable sprints. Here's a brief overview of each sprint:

### Sprint 1 - Week 1
- **HTML & CSS**: Create your resume using HTML and style it with CSS.
- **Static Website**: Deploy your HTML resume as an Amazon S3 static website.
- **HTTPS & DNS**: Use Amazon CloudFront for HTTPS and Amazon Route 53 for DNS.
- **JavaScript**: Add a visitor counter using JavaScript.
<p align="center"><br/><img src="https://imgur.com/H3tzHdZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br /><br />

### Sprint 2 - Week 2
- **Database**: Set up a DynamoDB database for the visitor counter.
- **API**: Create an API using AWS API Gateway and Lambda to interact with DynamoDB.
- **Python**: Write Lambda functions in Python for API operations.
- **Tests**: Include tests for your Python code.

### Sprint 3 - Week 3
- **Infrastructure as Code (IaC)**: Define API resources in an AWS SAM template and deploy them using the AWS SAM CLI.

### Sprint 4 - Week 4
- **Source Control**: Create GitHub repositories for backend and frontend code.
- **CI/CD (Backend)**: Set up GitHub Actions for backend code to run tests, package, and deploy to AWS.
- **CI/CD (Frontend)**: Set up GitHub Actions for frontend code to automatically update the S3 bucket (invalidate CloudFront cache if needed).
- **Blog Post**: Document your process and experience in a blog post.



### Sprint 1 - Week 1
<p align="center"><br/><img src="https://imgur.com/H3tzHdZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br /><br />

Sprint 1 - Week 1
Planning
HTML & CSS: Create your resume using HTML and style it with CSS.

Tasks:

Create one HTML file (index.html)
Style the resume with CSS for basic formatting and create one CSS file (styles.css)
Navigate to Route 53 to purchase a domain name if you done have available.
Navigate to S3 and create an S3 bucket ( g5up.icloud) make sure the bucket name matches the domain name.
Create bucket in us-east-1
Make sure to uncheck Block Public Access settings for this bucket
Enable Versioning
Create bucket
Upload your 4 files
Go to Properties
Scroll all the way down to Static website hosting and click edit
Enable Static website hosting, for Hosting type select Host a static website and type index.html for index document
Go to Permissions and click on Edit Bucket Policy
You can bring in your own policy or use the policy generator use this policy below( Just make sure you replace you-bucket-name with your own bucket name.

{
    "Version": "2012-10-17",
    "Id": "Policy1702527714612",
    "Statement": [
        {
            "Sid": "Stmt1702527682654",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}




Static Website: Deploy your HTML resume as an Amazon S3 static website.


Tasks:
Create an S3 bucket for hosting.
Upload HTML and CSS files to the bucket.
Configure S3 for static website hosting.
Test the website using the S3 endpoint.
Estimated Time: 1 day
HTTPS & DNS: Use Amazon CloudFront for HTTPS and Amazon Route 53 for DNS.

Tasks:
Set up an SSL/TLS certificate using ACM.
Create a CloudFront distribution linked to the S3 bucket.
Configure CloudFront to use the ACM certificate.
Update DNS settings in Route 53.
Test the website with the custom domain and HTTPS.
Estimated Time: 2 days
JavaScript: Add a visitor counter using JavaScript.

Tasks:
Write JavaScript code for a visitor counter.
Include the code in the HTML file.
Test the visitor counter functionality.
Ensure the counter persists and increments correctly.
Estimated Time: 2 days
Retrospective
What Went Well:

Successful creation and styling of the HTML resume.
Deployment of the static website on S3.
HTTPS and DNS configuration using CloudFront and Route 53.
Implementation of a visitor counter using JavaScript.
Challenges:

Any difficulties faced during the tasks.
Adjustments for Next Sprint:

Identify areas for improvement.
Plan for optimizing tasks or addressing challenges.
Execution
Daily Stand-ups:

Discuss progress and challenges.
Ensure team members are on track.
Task Completion:

Regularly check off completed tasks.
Test functionality at each step.
Documentation:

Update documentation as tasks are completed.
Ensure clarity for future reference.
Continuous Improvement:

Adapt the plan based on daily progress.
Encourage collaboration and knowledge sharing.
