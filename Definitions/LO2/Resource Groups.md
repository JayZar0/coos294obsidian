Resource groups are fundamental elements of the Azure platform that holds resources such as VMs, Application Gateways, Cosmos DB instances, etc. Resources in the group have their settings inherited unless they have manually been changed.

Characteristics
---
- Logical Grouping
	- Provides order and organization to resources created in Azure
- Life Cycle
	- If the resource group is deleted, all resources in the container will also be deleted, this makes it easier to remove a set of resources
- Authorization
	- Can be used as a scope for creating role based access control permissions based on the selected resource group

Organization Methods
---
- By resource type
- By environment
- By department
- Combination
- For authorization
- For lifecycle
- For Billing