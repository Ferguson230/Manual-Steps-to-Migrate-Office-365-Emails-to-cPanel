# Manual Steps to Migrate Office 365 Emails or Google Workspace Email accounts to cPanel
 Manual Steps to Migrate Office 365 Emails to cPanel

 # In this guide, we will discuss Office 365 or Google Workspace Email account to cPanel migration process.

To start with the process, you first need your account details below:

    Office 365 mail account or Google Workspace Email account, username and password.
    cPanel mail user account and password.

If you don’t have imapsync tool, please install it with the below command:

    sudo yum install imapsync

You can start with the migration process from Office 365 to cPanel inside the terminal by using the command.

Note: Run the command on cPanel server.

    imapsync --host1 outlook.office365.com --port1 993 --ssl1 --user1 test@cool.com --passfile1 /etc/secret1 --host2 map.cool.net --port2 993 --ssl2 --user2 test@cool.com --passfile2 /etc/secret2
    

Example:
 
    imapsync –host1 outlook.office365.com –port1 993 –ssl1 –user1 test@cool.com –passfile1 /home/cpaneluseraccount/pass1 – Store your outlook or gmail account password in this file –host2 map.cool.net –port2 993 –ssl2 –user2 test@cool.com –passfile2 /home/cpaneluseraccount/pass2


Here, Replace:
outlook.office365.com with Google workspace hostname if you have a Google Workspace Email account.
test@cool.com with your actual email account.
map.cool.net with your hostname of your cPanel server or WHM.
cpaneluseraccount with your cPanel account username.

/home/cpaneluseraccount/pass1 – Store your Office 365 email account or gmail account password in this file

/home/cpaneluseraccount/pass2 – Store your cpanel account password in this file

This is how you can migrate Office 365 email account or Google workspace account to cPanel server.

