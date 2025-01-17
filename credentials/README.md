# Credentials Folder

**Server URL:** http://ec2-54-215-173-150.us-west-1.compute.amazonaws.com/

**SSH Username:** ubuntu

**SSH Hostname:** `ec2-54-215-173-150.us-west-1.compute.amazonaws.com`

**SSH Password:** (NO PASSWORD SET FOR NOW) Key can be found at credentials/csc648Summer.pem

**Database Username:** root

**Public ip:** 54.215.173.150 on port 22

**Database Password:** admin

**Database Name:** team5app

## Instructions
### SSH from Terminal
1. First download the `csc648Summer.pem` key loacated in `csc648-su19-Team05/credentials` and place it in an accessiable location.
2. Open terminal and type `chmod 400 /location of csc648Summer.pem`
3. Then type `ssh -i /location of csc648Summer.pem ubuntu@ec2-54-215-173-150.us-west-1.compute.amazonaws.com` and you're in!

### Using FileZilla (SFTP)
1. First download the `csc648Summer.pem` key loacated in `csc648-su19-Team05/credentials` and place it in an accessiable location. 
2. Open FileZilla
3. Go to settings. On Mac click FileZilla->Settings. On Windows click Edit->Settings.
4. Click on SFTP from the selections on left
5. Click add key file and upload the `csc648Summer.pem`
6. Click ok to finalize settings
7. At the top in the host box type "http://ec2-54-215-173-150.us-west-1.compute.amazonaws.com/"
8. Username is `ubuntu`
9. Password is left empty 
10. Port: 22
11. Click quick connect and you're in!
12. Traverse to `/home/ubuntu/application/public` to view webpage

### Connecting to Database using MySQL Workbench
1. Open MySQL Workbench and add a new connection
2. Set connection name to `CSC 648 AWS` (this can be anything)
3. Change connection method to `Standard TCP/IP over SSH`
4. Change SSH Hostname to `54.215.173.150:22`
5. Change SSH Username to `ubuntu`. There is no password
6. Set the SSH Key File path to the `csc648Summer.pem` file located in the credentials directory
7. Leave MySQL Hostname as `127.0.0.1`
8. Leave MySQL Server Port as `3306`
9. Leave Username as `root`
10. Connect to the Database using `admin` as the password

### Connecting to Database from Command-Line
1. Enter `mysql -u root -p`
2. Enter `admin` as the password

## The purpose of this folder is to store all credentials needed to log into your server and databases. This is important for many reasons. But the two most important reasons is
    1. Grading , servers and databases will be logged into to check code and functionality of application. Not changes will be unless directed and coordinated with the team.
    2. Help. If a class TA or class CTO needs to help a team with an issue, this folder will help facilitate this giving the TA or CTO all needed info AND instructions for logging into your team's server. 


# Below is a list of items required. Missing items will causes points to be deducted from multiple milestone submissions.

1. Server URL or IP
2. SSH username
3. SSH password or key.
    <br> If a ssh key is used please upload the key to the credentials folder.
4. Database URL or IP and port used.
    <br><strong> NOTE THIS DOES NOT MEAN YOUR DATABASE NEEDS A PUBLIC FACING PORT.</strong> But knowing the IP and port number will help with SSH tunneling into the database. The default port is more than sufficient for this class.
5. Database username
6. Database password
7. Database name (basically the name that contains all your tables)
8. Instructions on how to use the above information.

# Most important things to Remember
## These values need to kept update to date throughout the semester. <br>
## <strong>Failure to do so will result it points be deducted from milestone submissions.</strong><br>
## You may store the most of the above in this README.md file. DO NOT Store the SSH key or any keys in this README.md file.
