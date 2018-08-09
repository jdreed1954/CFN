# CFN
AWS CloudFormation Templates

## Development and Production Directories

Templates in the **dev** directory have **NOT** been fully vetted.  These are works in progress.

Templates in the **prod** directory **HAVE** been tested in one or more regions.  In any case use these at your own risk.

### Note, Remanent Resources after Delete Stack

There may be remanent resources remaining in your account after your stack is deleted.  Resources that **may** remain in your account:

1. **Snapshots** - both EC2 and RDS snapshots are NOT removed with the stack.  The purpose is to use snapshots to rebuild services from a known-good state.  Of course, the user may remove these at anytime after the stack has been deleted.

2. **Security Groups** - these are resources that are often used by multiple stacks and, once standardized, should remain until a new version is developed.  SGs can be removed manually as long as there is no resource dependent on it.

3. **Additional Resources** Please watch this space.  If additional resources are found to require retaining on a stack delete, they will be added to this list.  The user of these templates is responsible for the charges incurred on his or her account.

Jim Reed
August 9, 2018
