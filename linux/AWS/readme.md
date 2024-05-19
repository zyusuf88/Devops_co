
# Root Account vs. IAM User:

An AWS **root user account** has complete access to all AWS services and resources in the account.

> **_NOTE:_**  However it is important to **NOT** use the root user for your everyday tasks. To safegaurd the root user credentials. Therefore creating IAM users

 An IAM user by default, a new IAM user has no permission to do anything. They are not authorized to perform any AWS operations or to access any AWS resources.
- An advantage of using individual IAM Users is that you can assign the permissions individually. You can even assign  administrative permissions, who can administer your AWS resources and also administer other IAM Users.
- The user's permissions are set to AWS tasks and resources, i.e., the job assigned to the IAM User. 
- For example, you create an IAM User whose name is Anita, you create a password for the user and set the permissions that let her start Amazon EC2 instances and read the data from Amazon RDS database.

#### On the IAM navigation panel, click on Users. The screen appears which is shown below. Click Create user.
<img width="704" alt="image" src="https://github.com/zyusuf88/Devops_co/assets/97973445/ff9c52f9-b025-42d0-881e-d11892d616fd">

### Follow the steps on the screen once created you should get this message below. 

<img width="886" alt="image" src="https://github.com/zyusuf88/Devops_co/assets/97973445/75c9fe9b-f06d-4a7f-9945-38e2c197b92e">


## 10 Best practices for IAM

  1. **Principle of Least Privilege** - Only give a user access to the folders they need to do their job.
   
  2. **Use Strong Authentication Methods** - Adds an extra layer of security beyond just a password.
  3. **Regularly Review and Update Permissions** - Ensures users don’t retain unnecessary access over time.
  4. **Implement Role-Based Access Control (RBAC)** - Assign roles like "Admin," "Editor," and "Viewer" with predefined permissions 
  5. **Monitor and Audit User Activity** - Helps detect unusual activity that could indicate a security issue.
  6. **Automate IAM Processes** -  Reduces human error and ensures timely updates to access controls.
  7. **Use Federated Identity Management** - Allow employees to log in to different services with their corporate credentials. This improves security by centralising identity management.
  8. **Regularly Backup IAM Configuration** -  Ensures quick recovery in case of misconfigurations or breaches.
  9.  **Provide Training and Awareness**- Conduct regular security training sessions on how to recognize phishing attacks.
  10. **Apply Network Segmentation** - for example separate the HR department’s network from the rest of the company’s network. <br>


 # Implementing Multi-Factor Authentication (MFA)
 
 - Multi-factor authentication (MFA) adds an extra layer of security by requiring users to provide a second form of verification beyond just a password.
- This second factor, such as a code sent to a phone or a fingerprint scan, ensures that even if a password is compromised, unauthorized access is still prevented.
- By adding this additional step, MFA significantly reduces the risk of phishing attacks and unauthorized logins, as attackers would need access to the second form of authentication to gain entry.
-  This layered approach enhances overall security and protects sensitive information more effectively.

<img width="677" alt="image" src="https://github.com/zyusuf88/Devops_co/assets/97973445/f8de1fc2-7cd0-43c9-8ed2-63945f9c3ba2">


AWS allows you to choose between a Authenticator app, Security Key or Hardware TOTP token

# Creating Custom IAM Policies

- IAM policies define permissions for an action regardless of the method that you use to perform the operation
- You manage access in AWS by creating policies and attaching them to IAM identities (users, groups of users, or roles) or AWS resources.
- Custom policies allow administrators to specify exact permissions tailored to the specific needs of their organization.

<img width="650" alt="image" src="https://github.com/zyusuf88/Devops_co/assets/97973445/b5892209-6996-497b-9f72-85bf94892408"> 


#### The principle of least privilege (POLP)

The principle of least privilege (POLP) is essential in DevOps to secure cloud infrastructure without hindering innovation. DevOps involves many users and tools across multiple cloud services, creating security challenges. Enforcing POLP in AWS involves restricting access to only what is necessary, reducing the risk of breaches.


- Implementing least privilege helps decrease cybersecurity risks and prevent data breaches, irrespective of user reliability or technical skills. 
-  It restricts access rights to the minimum necessary for users, processes, or applications to perform their jobs. 
-  This cybersecurity concept protects high-value data and assets by minimising the attack surface, enhancing operational performance, simplifying audits, and reducing the impact of human error. 

#### POLP in AWS
1. Grant Least Privilege Permissions: Use IAM policies to specify minimal required permissions.
2. Use AWS Managed Policies: Transition to least privilege with prepackaged policies as a starting point.
3. Utilise IAM Access Analyzer: Analyze and fine-tune permissions based on user activity.
4. Review and Remove Unused Access: Regularly eliminate inactive users, roles, and permissions.

<img width="514" alt="image" src="https://github.com/zyusuf88/Devops_co/assets/97973445/db9d6c5e-30a8-47c2-9889-5bf0b10f297b">




# Setting Up AWS Budgets

As AWS Budgets helps to improve planning and manage costs with flexible budgeting and forecasting, it allows users to:

- Create a custom budget to track costs, usage, and coverage across their AWS account.
- Stay informed on forecasted spending and resource use with alerts. 
- Respond quickly when thresholds are exceeded and create custom actions to define and initiate cost-saving responses. 
  
<img width="472" alt="image" src="https://github.com/zyusuf88/test/assets/97973445/c9577d88-5250-409b-a549-507fb83bb6bc">