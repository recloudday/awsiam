<h1>Introduction to AWS Identity and Access Management (IAM)</h1>

<h2>Description</h2>
In this lab, I successfully managed user permissions using AWS Identity and Access Management (IAM). I created three users: user1, user2, and user3, and assigned varying levels of permissions to each. User1 and user2 were given limited permissions, while user3 was granted full admin permissions. 
By logging in as each user, I demonstrated how their ability to perform certain actions was restricted based on their permissions. For instance, user1 and user2 were unable to stop an EC2 instance due to their limited permissions. 
When logged in as user3, with admin privileges, I successfully stopped the EC2 instance. This lab provided a clear understanding of how to manage and enforce user permissions in AWS IAM, highlighting the importance of proper access control in cloud environments.
<br />


<h2>Concepts and Utilities Used</h2>

- <b>AWS - IAM</b>
- <b>Managing User Permissions</b>
- <b>Access Control</b>

<h2>Environments Used </h2>

- <b>AWS</b>
- <b>S3 Buckets, EC2, IAM</b>

<h2>Environment walk-through:</h2>

<p align="center">
In IAM -> User Groups -> S3-Support -> Users, add user1 to the group <br/>
<img src="https://imgur.com/zWiX1zD.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
<br />
In IAM -> User Groups -> EC2-Support -> Users, add user2 to the group  <br/>
<img src="https://imgur.com/2yXzzxA.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
<br />
In IAM -> User Groups -> EC2-Admin -> Users, add user3 to the group
<img src="https://imgur.com/sDfZ61H.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
<br />
Sign in as user1 and try to create a bucket. This fails because this user only has support access to S3 instances. (Read-Only)  <br/>
<img src="https://imgur.com/VLKpHiU.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
<br />
Sign in as user2 and try to stop the EC2 instance. This fails because this user only has support access to EC2 instances. (Read Only) <br/>
<img src="https://imgur.com/54qONor.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
<br />
Sign in as user3 and try to stop the EC2 instance again. This is successful because this user has admin access.:  <br/>
<img src="https://imgur.com/6hvt2Gd.png" height="80%" width="80%" alt="IAM Steps"/>
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
