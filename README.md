# AzureCustomRoleScript
Creating custom IAM role is frequent need in Azure world to limit the resource access and follow the best practice of "least privilege" access.

Above script Power Shell script helps Azure users create custom IAM role within their account.

# Actions
Use role.Actions to define the resources custom role can assume. 
For example:
$role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
Above "action" statement gives "virtual machine" start capability to the custom script.

#Scopes
$role.AssignableScopes.Add("/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx")
Above statement defines the subscriptions to which this role is assigned to. 
Replace xxxxxx with "subscription id".
Repeat the above statement with different subscription id to support multiple subscriptions.


Have a suggestion to improve the code? Please submit a pull request or reach us at **info at invoke dot cloud**
