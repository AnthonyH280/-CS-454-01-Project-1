# -CS-454-01-Project-1
Part-A:
Started by connecting to the instance via the AWS website
Then made sure that a custum TCP address that allowed 8080 to connect in the security settings.

	1)- Configured AWS in the amazon linux using the CLI " aws configure " and inputting, also had to create an access key and copy the secret key in a text file.
		1.) AWS Access Key:
		2.) AWS Secret Access Key: 
		3.) Domain region name: us-east-2b
		4.) Default output format: text
		 also had to create an access key and copy the secret key in a text file.
			
	2)- After that replace the placeholder info in the CLI example with appropriate info.
		Then run in Amazon Linux terminal which should result in getting the IP addresses.

Part-B:
 Input the CLI text in part-B the terminal after replacing placeholder text.
 Ran just fine for me. Make sure to use the appropriate CLI commands as
 part B contains commands for both amazon linux and Ubuntu.

Part-C:
 After inputting the provided CLI into the terminal. Was able to get it to say
	that it was " listening on 8080 ". Afterwards I put in the "http://<PUBLIC_IP>:8080/convert?lbs=150"
	into my web browser, with the correct public ip of course, and was able to get it to work just fine.
	
Part-D:  
1.) Use the CLI " sudo nano /etc/systemd/system/p1.service " in Amazon Linux

2.) When a menu pops up copy and paste :
"
[Unit]
Description=CS454 Project 1 Node.js Service
After=network.target

[Service]
Type=simple
User=ec2-user
WorkingDirectory=/home/ec2-user/p1
ExecStart=/usr/bin/node /home/ec2-user/p1/server.js
Restart=on-failure

[Install]
WantedBy=multi-user.target
"
into the menu. Obviously without the quotaion marks.

3.) Then save it by pressing Ctrl+O to save, then Enter to confirm, and Ctrl+X to exit the editor. 
After that it should be working

part-E:

test cases: 1 Happy path: /convert?lbs=0     → 0.000 kg
2 Typical: /convert?lbs=150                  → 68.039 kg
3 Edge: /convert?lbs=0.1                     → 0.045 kg
4 Error: /convert (missing param)            → 400
5 Error: /convert?lbs=-5                     → 422
6 Error: /convert?lbs=NaN                    → 400

 All test cases were able to go through the Localhost8080, and gave appropriate output.
 All test case entered through the web browser gave appropriate outputs as well.
