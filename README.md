#Script to provision server users in the CloudPassage API
This script allows you to provision users on managed nodes using the CloudPassage API.  It accepts arguments for the following: username, groupname, server group name.  Username and groupname are for the account to be provisioned across the server group that you name.  Those values override the variables set in config.conf.  If the user already exists, the script will request a password reset for that account.
When invoked, the script rolls through all active servers in the specified group, provisioning accounts or resetting passwords as appropriate.

##Before We Begin
Please have a look at the config.conf file.  You will need to set your clientid and clientsecret or the script simply won't work.
Command line execution looks like this: 
provisionusers.py -u USER -g GROUP -s SERVERGROUP
You can omit anything here as long as it's configured in the config.conf file.

###Step by Step
Download all the files here into the same location and make sure that provisionusers.py is executable.
Edit config.conf to set your API key and secret, as well as any other values you need.  Username, groups, and server groups are overridden by command line arguments


####Here’s a breakdown of the files you see here:

* **provisionusers.py**            			Run this one.

* **server.py**		                        Contains Server object definition 

* **api.py**		                        Contains functions that hit the API 

* **config.conf**                           Contains configuration variables

* **fn.py**                                 Contains general functions

* **README.md**                             This file 

