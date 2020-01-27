# appstream-bastian
Replace your bastians with appstream

This solution seeks to create an out of the box baseline for deploying the solution mentioned in the AWS blog here 
https://aws.amazon.com/blogs/security/how-to-use-amazon-appstream-2-0-to-reduce-your-bastion-host-attack-surface/

The blog states the pre-reqs to be:
1. A Virtual Private Cloud (VPC) with a dedicated subnet for AppStream 2.0.
2. An existing Active Directory (AD) domain. This may be on premises, on AWS EC2 for Windows, or AWS Directory Service or Microsoft Active Directory used as a user directory.
3. Active Directory Federation Services (ADFS).
4. A Linux or Windows instance for which AppStream 2.0 will be acting as a bastion host.

We will be taking this and creating the following:
1. A permanent VPC for the Appstream Bastian fleet to operate in
2. A security group for you to nest with your App/Workload servers
3. Replacing ADFS with AWS SSO
4. Your pre-existing app/workload servers

# Setup Instructions
To set this up do the following:
