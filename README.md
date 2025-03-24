# AWS-IAM-User-Group-Policy-Role-and-MFA-Implementation
Implemented AWS Identity and Access Management (IAM) to manage user access and permissions securely. The project involved creating IAM users, groups, and policies, setting up IAM roles for service-to-service communication, and enabling Multi-Factor Authentication (MFA) for enhanced security.

Project Details
1. IAM User Management

Created IAM users with unique usernames and temporary passwords.
Shared login credentials with users for initial authentication.
Configured IAM users to change their passwords upon first login for security.
Assigned custom permissions to IAM users based on organizational roles.
Allowed IAM users to access AWS services based on permissions granted by the root user.
Logged in as IAM user and tested succesfully.

2. IAM Group Implementation
Created IAM groups to simplify user management.
Added users to specific groups based on their roles (e.g., Developers, Admins, Support).
Attached predefined and custom policies to groups to apply consistent permissions.
Ensured all users within a group inherited the same access control policies.

3. IAM Policy Creation and Management
Created custom IAM policies with granular access controls.
Used AWS Managed Policies and Custom Policies for fine-tuned permissions.
Attached policies to both users and groups to enforce role-based access control (RBAC).
Verified policy assignments by testing user access to specific AWS services.

4. IAM Roles for Service-to-Service Communication
Created an IAM Role for EC2 to Access S3
Go to AWS IAM Console → Roles → Create Role
Choosed AWS Service → EC2
Attached AmazonS3FullAccess (or a custom policy with required permissions)
Named the role ( EC2-S3-Access) and create it.

6. Enabling Multi-Factor Authentication (MFA)
Enabled MFA for IAM users to enhance security.
Configured Google Authenticator as the MFA device for user authentication.
Tested the MFA setup by logging in with an IAM user and verifying the second authentication factor.
Enforced MFA policies for privileged users to ensure secure account access.

7. Configure AWS CLI for the IAM User
Command : aws configure

Follow the commands
AWS Access Key ID [None]: YOUR_ACCESS_KEY
AWS Secret Access Key [None]: YOUR_SECRET_KEY
Default region name [None]: us-east-1  # (or your preferred AWS region)
Default output format [None]: json     # (or text / table)
Note: The IAM user must have necessary permissions to use AWS services.

Verify AWS Configuration Check if AWS CLI is configured correctly:

aws s3 ls      # List all accessible S3 buckets

Outcome and Impact

Enhanced security by enforcing role-based access control (RBAC) through IAM groups and policies.
Reduced manual user management efforts by implementing IAM groups with predefined permissions.
Improved service security by enabling IAM roles for EC2-S3 integration, eliminating the need for static credentials.
Strengthened authentication security by enforcing MFA for sensitive user accounts.

This project demonstrates a strong understanding of AWS IAM, access control, and security best practices, making it a valuable addition to your cloud computing experience. 
