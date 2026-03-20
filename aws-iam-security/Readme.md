<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Muhammad Abdullah Dilshad  
**Email:** abdullahdilshad111@gmail.com

---

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate... I'm doing this project to learn...the Identity access Management and How The Aws Controlls Different Identities.I Already know that what IAM is and in this project We gonna have a hand on it.

### Tools and concepts

Services I used were Ec2, IAM, Key concepts I learnt include Creating a minimal Ec2 Instance , How to create an IAM policy and then how to create an IAM group and attaching a policy to it. I also learned how to create an IAM user and add it to the group. 
After that i also learned how we can check the IAM user permissions from the Iam policy Simulator.

### Project reflection

This project took me approximately an hour .Nothing was challenging . Everything was way too easy and well explained .

---

## Tags

### What I did in this step

We are going to Launch two brand new Ec2 Instances i guess.

### Understanding tags

Tags are a way from which we can identify our differenet Rresources. I mean they help us to Find debug and Look through the Resources if we have to jump up to something quickly. Just a way of organizing.

### My tag configuration

The tag I’ve used on my EC2 instances is called Env The value I’ve assigned for my instances are are production and development.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy and a attach it to a newly created Iam user for an intern because i want to give that intern the Permission of the Development Instance but not the production instance.

### Understanding IAM policies

IAM Policies are basically the json rules that we define to give or grant access to the resources or deny access to some of the resources.

### The policy I set up

For this project, I’ve set up a policy using JSON

### Policy effect

I’ve created a policy that the person whom i will stick this policy can only have acces to the instance with the tag development and Everyone can see the contents of the instances ... and no user has the access to change or delete tags of the instances.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means Allow or deny, Action is basically Service:"Action" and the resource literally mean the thing that we want this Policy on. for example name of the ec2 Instance or the s3 Bucket Name.

---

## My JSON Policy

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will create an account alias because i want this easy and not a headache for the interns to see which account they are on.

### Understanding account aliases

An account alias is basically an easy way to call out your Account instead of calling it through the digits.

### Setting up my account alias

Creating an account alias took me like 2 minute Now, my new AWS console sign-in URL is https://abdullahsaatraining.signin.aws.amazon.com/console

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will make a new IAM group and an Iam user because By creating the Iam user we are going to give our new intern his account and By using the Aws groups we are going to give that users a specific group with permissions.

### Understanding user groups

IAM user groups are a way to group people or users together and then assign all those users a single level of the permission as a whole.

### Attaching policies to user groups

I attached the policy I created to this user group, which means every user in this group will inherit those permissions defind in that policy.

### Understanding IAM users

IAM users are identities that we can create in Aws and Add them to groups and give them permissions which the Real people can take the role off.

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is giving them the sign in link and the second way is giving them the username and the password that was created.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that this user do not have any access to the cost and usage and the billing section also the security tab is showing denied access too, this was because we only explicitely Described that this iam user will have the Ec2 Instance Access with the keyword development.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will login to the Aws management Console through the newly created sign in details that i made for the NextWork intern. After signing in I will check if the interns do have a development Ec2 instance permission and not the Production Environment.

### Testing policy actions

I tested my JSON IAM policy by stopping the development instance of the Ec2 and yes it did work and the instance got stopped. So basically what we explained or wrote code in the json that Allows this Policy holder to just have access to the Development Instance of the Ec2.

### Stopping the production instance

When I tried to stop the production instance , a long banner like a chinese Festival that NO, you cannot Delete this or stop this production Instance, This was because the person who sent you this link to sign in (Your Lead ) didnt thought of you worthy enough to have this permission.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance, it did stop this was because this new user(Internee) was allowed to perform all the actions to the Development Instance of ec2.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to use a special IAM tool called as the IAM policy simulator . I'm doing this because i have to check the permission of the new user and i cant do it every time by deleting the instance or making something. i can look at it on the top level by just using this tool.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is usefull to basically see all the permissions that the user has. It's useful for watching every single permission without ever the need of hit and trial of stopping and creating something.

### How I used the simulator

I set up a simulation for the Ec2 Instance having the keyWord as development The results were showing all denied because in this policy check AWS was checking that this user group is having All the permissions to all the Ec2 instances ( * ) but in realit the permisssion was given this user group for the all instance who had the instace tag (development) attached to them. I had to adjust it by Applying the filter of adding the tag value as development .

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-security-iam_069d8a621)

---

---
