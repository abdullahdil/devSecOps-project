<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Muhammad Abdullah Dilshad  
**Email:** abdullahdilshad111@gmail.com

---

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate that how we can host our own Website on the Internet using the Amazon S3 Service. I'm doing this project to learn the basics of how S3 works and the underlying architecture.

### Tools and concepts

Service I used is Amazon S3 Key concepts I learnt include Creating an S3 bucket and creating Objects in it. Pusing a whole website in it.making those website public. Maintaining access to these. then i made policy that no one can delete my index.html through bucket policies

### Time, challenges, and wins

This project took me approximatel 40 minutes. The most challenging part was making the bucket policies myself. It was most rewarding to myself because i wrote the JSON myself and it made it fresh again :|

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will make a bucket( basically a storage space to store Websites resources or contents ) because before hosting and making our website live, we have to store our resources of the websites somewhere.

### How long it took to create the bucket

Creating an S3 bucket took me 5 minutes to be very exact.

### Region selection

The Region I picked for my S3 bucket wa United States (Ohio)  because It was nearest to me at the time of the creation of this bucket.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means that S3 is not a regional service and is a global service(it does not operate at a single region rather operate at a global level) so the name of that bucket should be such that no other bucket Name of any Account on the Aws should match this.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload my website Contents into the s3 bucket as Objects because I want to host this Application on the Cloud using the Amazon S3 Service.

### Files I uploaded

I uploaded two files to my S3 bucket - they were index.html and the whole folder that contains the Websties Contents and stuff.

### How the files work together

Both files are necessary for this project as index.html is the main structure of this Project and The other Folder contains assets and other stuff like CSS or assets that help keep the Websites running and all.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure my static website hosting using the Amazon S3  because I want to make my application to the Public via a link.

### Understanding website hosting

Website hosting means making the website public to the user.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I uploaded my website files and contents on the S3 as objects and made them public through permissions.

### Access Control Lists (ACLs)

An ACL is basically just the set of rules of who can access your  bucket objects outside of this Aws Account and yes I Enbaled the ACLs because later on i may use it.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is basically a way that we can access our Bucket Objects (in this case the website Content or the index.html)

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw a 403 forbidden error The reason for this error was the bucket Objects were not permissioned for the public access.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make my S3 Objects ( my Static Websit's content public from Private because these objects are private my default.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I changed the permissions for the S3 bucket objects and made them public. Earlier i was getting a 403 because the bucket objects were not Public.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to change the bucket policies so that no one can delete my index.html file. I'm doing this so that my bucket remains secure and also i am testing the policies here.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are used to control the access to the buckets.The benefit of using bucket policies is like complex access management and are resource based while ACLs are useful for simpler legacy mechanism for the access management.The bucket policy is JSON while the other is not apparently.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policyworked I tested this by deleting the iindex.html because its the most important file and saw that the bucket policies did not let me delete this index.html because there was some policy attached  to it that no one can delete this.

---

---
