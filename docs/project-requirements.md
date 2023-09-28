# Requirements for the backend solution
This doc will house the requirements that the backend solution should eventually hit.

[] [Auditable]
[] [Authenticated]
[] [Containerized]
[] [Encrypted at rest]
[] [Encrypted in transit]
[] [Versioned]

## Auditable
The changes made to the state file should be logged in a way that allows a user to see what has happened to the file. This should include which identity made the change and what the change was.

## Authenticated
Access to the state file should not be given unless the user can verify their identity and that identity is allowed to preform the requested action on the state file.

## Containerized
If the solution is containerized it will make it easier to deploy to multiple environments as it will be a more self contained solution. It will also make it easier to do development work with if it can be spun up and down quickly.

## Encrypted at rest <a name="EAR"></a>
State files can contain sensitive data in them so they should not be written to disk in an unencrypted form. 

## Encrypted in transit <a name="EIT"></a>
State files can contain sensitive information in them and the backend storing them is not necessarily inside a secure network so the data should be encrypted while it is in flight.

## Versioned
Sometimes your state files can get corrupted or your infrastructure can change in a way that you didn't want. If you have versioned state files you can go back through the history of your state and see how your infrastructure has changed over time.