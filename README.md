# What is statefile in Terraform?
Statefile is a heart of Terraform! Using a state file will record or store the Infrastructure created and the drawbacks are it will store sensitive information like passwords, and secrets, and these drawbacks can be fixed by the remote backend.
```
terraform show
```

# What is the remote backend?
you can store the state file in the backend instead of the state file created on a VM or laptop. The state file would be hosted in the s3 bucket by restricting access to the S3 bucket. when changes are made it automatically updates the s3 buckets

# What is a lock?
The locking mechanism is important so that multiple people are trying to execute the same project only one person can execute it at a time and the locking mechanism can be implemented using Dynamo DB.
# What are provisioners?
provisioners are a kind of resource we can execute actions and implement during the creation and also during destruction.
local exec is used to copy the output to a particular file.
remote exec is where you can connect to the resource and execute commands like installing Python and Java.

File provisioner to copy a file from local to the remote EC2 instance. The file provisioner is used to copy files or directories from the local machine to a remote machine. This is useful for deploying configuration files, scripts, or other assets to a provisioned instance.

# Terraform workspaces?
it maintains the state file for a different environment like staging, pre-prod, production, etc. if we don't use the workspaces then the particular environment state file will update/override or it will delete the resource and re-create the resource.

```
terraform workspace new dev
```
