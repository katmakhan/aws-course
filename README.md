# aws-free-course
This contains the basic tutorials for starting your own AWS project

#Free Tier- AWS CLOUD
In your first year includes 750 hours of t2.micro (or t3.micro in the Regions in which t2.micro is unavailable) instance usage on free tier AMIs per month, 30 GiB of EBS storage, 2 million IOs, 1 GB of snapshots, and 100 GB of bandwidth to the internet


#Steps

Choose whichever that shows "Eligble for FREE TIER"
Create a key pair name it <somekey> and download as .ppk - For putty login and .pem for SSH

https://us-west-2.console.aws.amazon.com/ is the Instance (There will be other instances like this)
https://ap-south-1.console.aws.amazon.com/ec2/v2/home?region=ap-south-1#Instances: (This will be the Indian Server)


Right click on instance and choose CONNECT, That will contains the code for connecting the server

chmod 400 openvpn_serverkey.pem to change the permission (If needed)
and also works in C drive only, Dont know why


ssh -i "vpn-aws-mumbai.pem" root@ec2-15-206-151-54.ap-south-1.compute.amazonaws.com to access it 


After that, Agree the terms
After sucess, the root will be changed

--------------------------------------------------------------------------------
Initial Configuration Complete!

You can now continue configuring OpenVPN Access Server by
directing your Web browser to this URL:

https://15.206.151.54:943/admin
Login as "openvpn" with the same password used to authenticate
to this UNIX host.

During normal operation, OpenVPN AS can be accessed via these URLs:
Admin  UI: https://15.206.151.54:943/admin
Client UI: https://15.206.151.54:943/

See the Release Notes for this release at:
   https://openvpn.net/vpn-server-resources/release-notes/

Please login as the user "openvpnas" rather than the user "root".

Connection to ec2-15-206-151-54.ap-south-1.compute.amazonaws.com closed.
---------------------------------------------------------------------------------

so run this instead

ssh -i "vpn-aws-mumbai.pem" openvpnas@ec2-15-206-151-54.ap-south-1.compute.amazonaws.com to access it 



Change the password by
sudo passwd openvpn

[btechadmin]


Then login to Admin  UI: https://15.206.151.54:943/admin with ID as openvpn and changed password

Then go to configuration > VPN Settings > Routing >
Should client Internet traffic be routed through the VPN? To YES
Click Save
Click Update running server on the top

------------------------------------------------------------------------------------------
https://15.206.151.54:943/

To Download the software after LOGIN


Add new user by
Going to USER MANAGERMENT > User Permissions, Allow new user, allow autologin, then set a new password (BY CLICKING EDIT BUTTON)
THen Save and Restart the machine

-------------------------------------------------------------------------------------------
PUTY GENERATOR 

Loads > .pem
Generates >.ppk file


TO user login via PUTTY and not via SSH

Open PUTTY 
Host name is : the public IP


Login : root 
If Like we changed using openvpn
the Changed vpn will be openvpnas


Connection >SSH>AUth > Upload the .ppk file
--------------------------------------------------------------------------------------------
