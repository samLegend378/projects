**AWS IAM Hands-on Lab: Creating an EC2 Group with ReadOnlyAccess
**
This repository documents my hands-on practice with **AWS Identity and Access Management (IAM)**.  
I created a new IAM **Group** specifically for **EC2 users** and attached the **ReadOnlyAccess** AWS managed policy.

---

##  Steps I Followed

### 1. Create a New Group
- Open the **IAM Console**
- Go to **User groups** → **Create group**
- Name the group: `EC2-ReadOnly-Group`

### 2. Attach a Policy
- In the policy selection screen, search for **`ReadOnlyAccess`**
- Attach it to the group  
  This policy allows read-only access to **all AWS resources** (safe for auditors, security reviewers, or devs who only need visibility)

### 3. Add Users to the Group
- Either create new IAM users or add existing ones
- Assign them to the `EC2-ReadOnly-Group`

### 4. Test Permissions
- Log in as a user in this group
- Try viewing EC2 instances → Works
- Try starting/stopping/deleting an instance → Access denied

---

##  What I Learned
- IAM **Groups** make it easier to manage multiple users at once.
- AWS **Managed Policies** (like `ReadOnlyAccess`) are quick ways to enforce common permission sets.
- **Least Privilege Principle**: Give only the permissions needed, nothing more.
- Separation of duties is easier when groups are used effectively.

---

##  Key AWS Concepts Covered
- IAM **Groups**
- IAM **Policies**
- AWS Managed Policies
- **ReadOnlyAccess** (view-only permissions for all services)

---

##  Why This Matters
This is a fundamental step in learning AWS security.  
Understanding IAM groups and managed policies builds the foundation for:
- Secure multi-user environments
- Access control best practices
- Preparing for AWS certifications (e.g., SAA, Security Specialty)

---

 *This lab was part of my AWS Cloud Security learning journey.*  
