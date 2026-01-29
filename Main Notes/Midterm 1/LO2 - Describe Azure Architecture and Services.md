Describe the Core Architectural Components of Azure
---
- Subscriptions are required to use Azure services
- An Azure account must be created to access Azure and a subscription is linked to the account
	- There can be multiple subscriptions
- Azure Free accounts have access to popular Azure products for 12 months
- Azure free student accounts have access to certain services for 12 months and 100$ in credits to use in the 12 months
- Core architecture of Azure can be broken into 2 separate groupings
	- Physical infrastructure
		- [[Regions]]
		- [[Availability Zones]] 
		- [[Region Pairs]]
		- [[Sovereign Regions]] 
	- Management infrastructure
		- [[Azure resources]] 
		- [[Resource Groups]] 
		- [[Subscriptions]] 
		- [[Accounts]] 
- When creating a resource it is required that they are placed in a resource group
	- A resource group can contain many resources while a resource can only be in one resource group
	- Can't place a resource group in a resource group
- Subscriptions allow for logical organization of resources groups and their resources
	- An account can have multiple subscriptions
- Management groups organize subscriptions
	- subscriptions can group resource groups where resources are grouped in resource groups

Describe Principles of Resource Groups
---
- Resource groups are fundamental elements of the Azure platform that holds resources such as VMs, Application Gateways, Cosmos DB instances, etc.
- Each resource must be assigned into a resource group and may be moved between resource groups.

Azure Resource Manager
---
- An application infrastructure that is made up of many components. Components going to be related parts to a single entity
- **Resource Group Rules**
	1. Resources can only exist in one resource group
	2. Resource groups can't be renamed
	3. Resource groups can have resources of many different types
	4. Resource groups can have resources from many different regions
- **Resource Group Factors**
	- Resources in a group should share the same lifecycle
	- Each resource can only exist in one group
	- Can add, remove, move at any time
	- Resource groups can contain resources that reside in different regions
	- Can be used to scope access control for administrative actions
	- Resources in a group can interact with other resource groups
- **Azure Resource Manager Locks**
	- Prevents Accidental deletion of resources
	- *Lock Types*
		- Read-only locks, prevents any changes to the resource
		- Delete locks, prevents deletion
- **Reorganizing Azure Resources**
	- Resources can be moved across groups and subscriptions
	- During the move the source and target groups are locked during the process
	- The resources are still accessible during the move however
- **Resource Limits**
	- There are resource limits
	- Limits are based on the subscription

Configure Azure Resources with Tools
---
- **Azure Cloud Shell**
	- Azure has an interactive cloud shell on the web portal for managing Azure resources
	- Linux users can opt for the bash shell if that is what they prefer
- **Infrastructure as code**
	- Infrastructure as code describes through code, the infrastructure that you need for an application
	- Can maintain both application code and everything needed to deploy an application in a central code repository
	- Advantages are
		- consistent configurations
		- improved scalability
		- Faster Deployments
		- Better traceability
	- Arm Templates
		- Can automate deployments and use the practice of infrastructure as code
		- template code becomes part of your infrastructure and development projects
		- Resource managers orchestrates deploying the resources so they're create in the correct order
		- Can be stored in a repository for versioning
		- Can nest templates inside other templates