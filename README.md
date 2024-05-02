# Cloud_resume

**Part 1** -- Build a statis website on S3 1) Create HTML, CSS and javascript code for resume(Chatgpt) 2)Upload files to S3 3) Configure S3 for a static website with public access
 
- [ ] create S3 bucket
- [ ] interms of naming the bucket it should match the domain name of the site 
- [ ]  enable static website hosting
- [ ]  policy to allow the contents that should be publicky available
 
- [ ] Code snippet:

This allows everyone to read/view everything in the bucket.  Be sure to update the Bucket-Name.

<img width="320" alt="image" src="https://github.com/Akash051198/Cloud_resume/assets/63510805/4718420c-514b-46ab-b21d-104f7670555c">

Code snippet link: https://docs.google.com/document/d/1Y9Vjom6lbdKdfbw672FWGJ0WVO8gbemFUMsE72LqDac/edit


 
**Part 2** -- Make it work with a custom domain nae 1) Register a domain name with route 53 2) Update records to point to the s3 website endpoint

- [ ] Route53
Create a hosted zone 
type the domain name
type: public hosted zone
take the name servers and create a domain in the third party sites like go daddy
LinkedIn article if you need help using a domain name from an external provider like GoDaddy
￼
 / pointing-third-party-registrar-aws-route-5...

<img width="648" alt="image" src="https://github.com/Akash051198/Cloud_resume/assets/63510805/d067fff6-9b53-4ee3-aaa5-e3bd6e2a5f9e">


￼
 
**Part 3** -- Incoporate Cloudfront & SSl/HTTPS 1)Setp SSL/HTTPS with Aws cert manager 2) Create a CLoudfront distribution

check for steps for DNS validation

<img width="769" alt="image" src="https://github.com/Akash051198/Cloud_resume/assets/63510805/8d060db4-ed83-4a50-99f2-5dd295b814cc">

 
create cloud front distribution - make as website endpoint rather than s3endpoint
redirect Http to https 


The domain name will be in cloud front distribution but its req to have domain  name in the FQDN

make update in route53
update the A record
current setup is routing to S3 endpoint	
change it to the cloud front endpoint 

<img width="727" alt="image" src="https://github.com/Akash051198/Cloud_resume/assets/63510805/57b281fd-fc34-4fb1-8180-ad22b43123cc">


￼

