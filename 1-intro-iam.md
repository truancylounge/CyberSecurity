# Fundamentals of Identity and Access Management (IAM)
1. Common protocols that handle Token Based Authentication are:
   1. **OAuth 2.0**, is the Authorization framework (what user is allowed to do), but not Authentication framework (proving who user is)
   2. **OpenId Connect (OIDC)**, adds critical identity layer that verifies user identity and confirms who the user is. \
       - Authentication is performed by authorization server, and also retrieves basic information about end user \
       - Uses OAuth 2.0 for Authorization.
2. Common Authentication patterns 
   - Passwords or One-time Passwords
   - Fingerprint Scan
   - Multi-Factor Authentication
3. Authorization is usually strongly coupled with access controls which define rules to access resources
   - ACL's (Access Control Lists)
   - RBAC (Role Based Access Control)
   - ABAC (Attribute Based Access Control)
4. 

# IAM Architecture elements/roles
1. Database (Directory)
   - IAM systems usually keep records of identities in their own data structures. 
   - Relational, Object, Graph databases can be used to store identity data.
   - **Hierarchical databases** are particularly suitable for handling identity storage. The tree data model makes them a good fit to store identity data.
   - Interactions with Hierarchical databases is done using LDAP protocol. 
   - Examples; Active Directory, OpenLDAP 
2. te

## Amazon Cognito
   - Provides Authentication, Authorization and User Management
   - It is a Customer Identity and Access Management (CIAM) service. 
   - It acts as an **Identity provider (IDP)** and **Identity broker** to handle **user registration, authentication (login/signup) and authorization** for mobile and web applications. \

Cognito handles identity management through two main components:
   - **User Pools** are user directories that provide sign-up and sign-in options for all users.
     - Facilitates users to sign in to application via Amazon Cognito or federate through third-party identity providers like Apple, Google, Facebook etc
     - User pool have a directory profile that can be accessed via an SDK to manage pools programmatically
   - Identity Pools, provides functionality to grant users access to other AWS services.
     - Users can obtain temporary AWS credentials to access AWS services, S3, Dynamo etc. 
     - Identity pools can be used without User Pools to support anonymous guest users
![Amazon Cognito Arch Pattern](./docs/content/imgs/architecture/amazon-cognito-arch-pattern.png)

> [] Read up on SRP protocol (Secure Remote Password)

# Secure design principles



