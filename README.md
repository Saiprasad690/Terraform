# What is statefile in Terraform?
Statefile is a heart of Terraform! Using a state file will record or store the Infrastructure created and the drawbacks are it will store sensitive information like passwords, and secrets, and these drawbacks can be fixed by the remote backend.
```
terraform show
```

# What is the remote backend?
you can store the state file in the backend instead of the state file created on a VM or laptop. The state file would be hosted in the s3 bucket by restricting access of s3 bucket. when changes are made it automatically updates the s3 buckets
